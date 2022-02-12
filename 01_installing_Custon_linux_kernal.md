# Install Custom linux kernal
## Installing dependencies 

```bash
  sudo apt install build-essential vim fakeroot bison flex ccache kernel-package ghex libncurses5-dev libssl-dev
```
- Downloading the linux kernal:
  - [kernal.org](https://kernel.org/)
  - Install the kernal version like
  ```bash 
  wget https://cdn.kernel.org/pub/linux/kernel/v5.x/linux-5.16.9.tar.xz
  ```
  - Make a new file `linux` copy the kernal file 
  ```bash 
  mkdir linux
  cd linux\
  # Move the file 
  mv ../linux-5/16.8.tar.xz .
  # Unzip it 
  tar xf linux-5/16.8.tar.xz
  ```
## Compile the kernal 
### Approch Im going with 
- Copy out the system `config` file for the install ubuntu system and use that as starting point 
- The config file will be in boot directory
```bash 
 # so copy the file 
 cp /boot/config-5.14.0-kali4-amd64 .config
 # To check 
 ls .config
 # make config file compatible 
 yes ''  | make olddefconfig    
 make clean
 # or
 make nconfig 
 # To check number of cups avalible 
  echo $(nproc)
# To Compile 
make -j4 deb-pkg LOCALVERSION=-rootkit

 
 
