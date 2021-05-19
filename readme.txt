First, you need to install Ansible on your master computer. To do so, follow these steps:

1. Open your terminal.

2. Make sure that you are the root user.

3. Enter these commands in this order: 

	apt install docker.io

	systemctl enable docker 

	apt install curl 

	curl -L "https://github.com/docker/compose/releases/download/1.23.1/docker-compose-$(uname -	s)-$(uname -m)" -o /usr/local/bin/docker-compose

	apt update

	echo "deb http://ppa.launchpad.net/ansible/ansible/ubuntu trusty main" >> 	/etc/apt/sources.list

	apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 93C4A3FD7BB9C367

	apt update

	apt install ansible 

	apt install nodejs npm

	npm install npm --global 

	apt install python3-pip git pwgen vim

	pip3 install docker-compose==1.23.1

	wget https://github.com/ansible/awx/archive/refs/tags/17.1.0.zip

	apt install unzip 

	unzip 17.1.0.zip

	rm 17.1.0.zip 

	cd awx-17.1.0/installer

4. Then open the inventory file and uncomment "password".

5. Run the command:

	pwgen -N 1 -s 30

6. Add the resulting pwgen key to the inventory file.

7. Next, run the command:

	ansible-playbook -i inventory install.yml

8. Finally, run the same command but replace "install.yml with the following playbooks from the repository:

	lamp.yml
	laravel.yml
	awx.yml
	