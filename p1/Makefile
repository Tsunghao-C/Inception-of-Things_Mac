all: up

up:
	vagrant up

down:
	vagrant destroy -f

clean:
	vagrant box prune
	rm -rf ~/.vagrant.d/tmp/*
	rm -rf ~/VirtualBox\ VMs/

s:
	vagrant ssh $(USER)S

sw:
	vagrant ssh $(USER)SW

re: down up

.PHONY: all up down clean re s sw
