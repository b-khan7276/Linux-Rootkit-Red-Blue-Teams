# Linux RootKit
## what is rootkil ?
 - Protect malicious code or software like a backdoor
 -  Its purpose is to give root level access to an attacker 
 -  the most important thing about this is it  hides itself 
 
## Checking rootkit in kali linux 
- By default kali linux comes with root checker 
    - chkroot kit - is pre-install 
      - If not 
      ```bash 
      apt-get install chkrootkit
      ```
    - To get help  
    ```bash 
    chkrootkit -h 
    ```
    - To run the chkroot 
    ```bash 
    chkrootkit 
    ```
 ## Installing rkhunter
 
- To install rkhunter
```bash
apt-get install rkhunter
```
   - Basic check of rkhunter
   ```bash
      rkhunter -c
```
