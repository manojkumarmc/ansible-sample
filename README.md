#### Install ansible
```
dnf install -y ansible

```
#### To check version
```
  ansible --version
```
#### To ping localhost
```
 ansible all -i 'localhost,' -c local -m ping

```
#### Bypass all unwanted stuff
```
touch inventory
echo localhost >> inventory
echo localhost ansible_connection=local >> inventory

```
#### Run playbook
```
touch pb.yml

- hosts: all
  tasks:
      - shell: echo "hello world"
     
ansible-playbook -i 'localhost,' -c local pb.yml     
```


