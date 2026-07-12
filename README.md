## ArgoCD Demo App:



### Useful commands:

_Login:_
```
agrocd login <ip:port> --insecure

argocd login 10.1.1.21:31470 --insecure


Or,
argocd login 10.1.1.21:31470 --insecure --username admin --password <PASSWORD>

'admin:login' logged in successfully
Context '10.1.1.21:31470' updated
```


_User Information:_
```
argocd account get-user-info
```




_Change the password:_
```
argocd account update-password

*** Enter password of currently logged in user (admin):
*** Enter new password for user admin: admin123
*** Confirm new password for user admin:
Password updated
Context '10.1.1.21:31470' updated
```




_Logout:_
```
agrocd logout <ip:port>

agrocd logout 10.1.1.21:31470
```




_Common Commands_
```
-- Cluster lists: 
argocd cluster list


-- Add a Git Repository:
argocd repo add https://github.com/user/repository.git
argocd repo add https://github.com/user/repository.git --username USERNAME --password PASSWORD
argocd repo add git@github.com:user/repository.git --ssh-private-key-path ~/.ssh/id_rsa


-- List Repositories:
argocd repo list


-- Remove Repository: 
argocd repo rm https://github.com/user/repository.git


-- List projects:
argocd proj list


-- Get project:
argocd proj get default


-- Create project:
argocd proj create dev-project


-- Delete project:
argocd proj delete dev-project



-- List Applications
argocd app list


-- Sync an Application:
argocd app sync guestbook-app
argocd app sync --all


-- Refresh Application Status:
argocd app get guestbook-app --refresh


-- Delete an Application:
argocd app delete guestbook-app


-- Enable Auto Sync:
argocd app set guestbook-app --sync-policy automated


-- List deployment history:
argocd app history guestbook-app


-- Rollback:
argocd app rollback guestbook-app <ID>



-- Application Logs:
argocd app logs guestbook-app
```


---
---



