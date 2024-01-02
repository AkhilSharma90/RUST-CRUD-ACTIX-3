
# Rust CRUD with Actix Web 3

> Actix Web 3 has been superseeded by [Actix Web 4](https://github.com/actix/actix-web).

I also have the Actix web 4 example in one of my repos, do take a look.

1. Make sure you have apt-transport-https, ca-certificates, curl, software-properties-common
2. Make sure you run `apt install build-essential`
3. Make sure you run `apt install libssl-dev`
4. Make sure you run `apt install pkg-config`
5. Install docker, pull mysql image (make sure you don't use mysql server, just the regular mysql) from docker hub and run mysql container
6. Set your root user and password for mysql
7. `docker run --name mysql -e MYSQL_ROOT_PASSWORD=123 -d -p 3306:3306 mysql:latest
8. Use mysql in your docker container with this command `sudo docker exec -it mysql bash`
9. When you're in bash, type `mysql -u root -p`
10. `CREATE DATABASE actix_example;`

11. Modify the `DATABASE_URL` var in `.env` to point to your chosen database

12. Turn on the appropriate database feature for your chosen db in `Cargo.toml` (the `"sqlx-mysql",` line)

13. Execute `cargo run` to start the server

14. Visit [localhost:8000](http://localhost:8000) in browser

Run server with auto-reloading:

```bash
cargo install systemfd
systemfd --no-pid -s http::8000 -- cargo watch -x run
```
