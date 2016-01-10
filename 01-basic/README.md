Ansible Lab #01 - Basic
===

## 實習重點

### Ansible terminology

- control machine
- managed node
- inventory
- playbook
- module (See also: [總列表](http://docs.ansible.com/ansible/modules_by_category.html))


### Playbook 基本結構

- hosts
- vars
- tasks


### 用到的 module(s)

- File modules / [lineinfile](http://docs.ansible.com/ansible/lineinfile_module.html): Ensure a particular line is in a file, or replace an existing line using a back-referenced regular expression.


### Ansible 變數樣板系統

- Jinja2 (See also: [Using Variables: About Jinja2](http://docs.ansible.com/ansible/playbooks_variables.html#using-variables-about-jinja2))


### 執行

- `ansible-playbook`
- idempotent
  - 設定檔可以重複執行，他不會有怪怪的副作用


### 練習 by azole

```
vagrant up --no-provision

ansible-playbook -i .vagrant/provisioners/ansible/inventory/vagrant_ansible_inventory setup.yml 

> cat /etc/hosts
# 會看到多了一個 10.0.0.10  mywordpress

```

或是直接交由 vagrant 執行   
```
vagrant up --no-provision
```
Vagrantfile 有設定了 config.vm.provision   