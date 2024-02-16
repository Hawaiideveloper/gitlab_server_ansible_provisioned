


Run this:
 ansible-playbook -i inventory.ini install_gitlab_ce.yml


 Then edit the file

 sudo editor /etc/gitlab/gitlab.rb

Replace 'http://gitlab.example.com' with your server's actual external URL. If you're just testing GitLab and don't have a domain name set up, you can use the server's IP address, but make sure to include the http:// prefix, like http://192.168.1.58.



Then run this to take in the changes

sudo gitlab-ctl reconfigure



finally print out the /etc/gitlab/initial_root_password file and use that along with the username root to login for the first time

sudo cat /etc/gitlab/initial_root_password

# gitlab_server_ansible_provisioned
# gitlab_server_ansible_provisioned
