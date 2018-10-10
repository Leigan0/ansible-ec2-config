# ansible-ec2-config

Basic ansible script to build a ec2 instance webserver. 

Script spins up an instance, tags instance then waits for SSH to be active. 

Ansible then installs python dev tools and httpd - and starts httpd service

Script can also terminate instance. 

To run 

`$ ansible-playbook -i hosts -v --ask-vault-pass build-ec2.yml`

To Terminate 

`$ ansible-playbook -i hosts -v --ask-vault-pass ec2-down.yml` 

Add IAM user keys: 

`$ansible-vault create aws_keys.yml`

And add following: 

aws_access_key: XXXX
aws_secret_key: XXXX

Add path to KeyPair within ansible.cfg



