# vagrant-ansible-playbook
**Yaml:** 

https://iamvon.github.io/iamvon.github.io/2017/05/29/yaml/

**INI format:**

https://en.wikipedia.org/wiki/INI_file

https://github.com/SemaiCZE/inicpp/wiki/INI-format-specification

**jinja2:**

http://jinja.pocoo.org/docs/2.10/


**Create Directory Strucure**
* ├── inventory.ini
* ├── provisioning
* │   ├── groups_var
* │   │   └── all
* │   ├── playbook.yml
* │   └── roles
* │       └── general
* │           └── tasks
* │               └── main.yml
* ├── README.md
* └── Vagrantfile

**Comand**
* mkdir -p  provisioning/{groups_var,roles} 
* mkdir -p  provisioning/roles/general     
* mkdir -p  provisioning/roles/general/tasks
* touch  provisioning/roles/general/tasks/main.yml
* touch  provisioning/playbook.yml                
* touch  provisioning/groups_var/all

**Update main.yml, playbook.yml, all file like this repository**


**Run command**
* vagrant up
* vagrant ssh web1
* vagrant ssh web2
* vagrant ssh db

**Open in Browser**
* http://localhost:8080/
* http://localhost:8081/
* http://localhost:8082/
