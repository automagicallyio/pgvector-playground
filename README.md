# PostgreSQL + pgvector Dev Container / Codespace

This is a PostgreSQL dev container for use with VS Code Remote Containers or GitHub Codespaces.
The devcontainer.json uses a docker-compose.yaml to set up a local PostgreSQL server inside the container.

For use with the local PostgreSQL server,  copy `.env.devcontainer` into `.env`.

For use with an Azure PostgreSQL server,  copy `.env.azure` into `.env` and adjust the host name, user name, and password.

Then run one of the examples in the `examples` directory.

# Demo
1. cp .env.devcontainer .env
2. Use GitHub Copilot and ask "how do i restore database from video_backup.dump file using .env variables"
3. export $(grep -v '^#' .env | xargs)
4. pg_restore -h $DBHOST -U $DBUSER -d $DBNAME -W < video_backup.dump --verbose
5. Use SQL Tools extension to explore database
6. 