all: check up

check:
	@sudo ./scripts/pre-requisitions.sh

up:
	./scripts/setup-k3d.sh
	./scripts/setup-argocd.sh

clean:
	k3d cluster delete $(USER)
	docker volume prune -f
	docker network prune -f
	docker image prune -a -f

fclean: clean
	@sudo ./scripts/uninstall_prereqs.sh

re: clean up

.PHONY: all check up clean fclean re