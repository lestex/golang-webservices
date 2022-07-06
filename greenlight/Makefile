.PHONY: postgres

postgres: ## start postgres container
	@podman run --name postgres -e POSTGRES_PASSWORD=password -d -p 5432:5432 postgres:14

connect: ## connect to postgres
	@podman exec -it postgres psql -h localhost -U postgres

asuser: ## connect as greenlight to postgres
	@podman exec -it postgres psql -h localhost -U greenlight --dbname=greenlight