* Problem Statement
```
Host a static website on one of target server, content of static website is available at the git repository
```
* Inputs
  * You will need to install below softwares
    * git
    * nginx
  * You have to get the code available in the git repository(https://github.com/opstree-ansible/ansible-training/blob/master/attendees/exercise/website/index.html) at  /usr/share/nginx/html
  * Owner of /usr/share/nginx/html and it's sub folders should be nginx user.
* Validations
  * On server itself
  ```
  curl localhost
  ```
  * If target server is public access it using browser
