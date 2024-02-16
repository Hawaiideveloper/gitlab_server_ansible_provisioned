### First run this to gain control of your server
ansible-playbook -i inventory.ini bootstrap.yml --ask-become-pass



### Run this:
 ```ansible-playbook -i inventory.ini install_gitlab_ce.yml```


### Then edit the file
``` sudo editor /etc/gitlab/gitlab.rb```

_Replace 'http://gitlab.example.com' with your server's actual external URL. If you're just testing GitLab and don't have a domain name set up, you can use the server's IP address, but make sure to include the http:// prefix, like http://192.168.1.58._


### Then run this to take in the changes

```sudo gitlab-ctl reconfigure```



### Finally print out the /etc/gitlab/initial_root_password file and use that along with the username root to login for the first time

```sudo cat /etc/gitlab/initial_root_password```



Some possible improvements would be to make a template file and allow the user of this repo to make the one change of their ip so that they

do not need to login and do the manual changes above; however being that it is 2:19am I am tired and will not be doing anymore contributions to this project 

unless it breaks or someone pays me,
