### initialize the repository run
`docker compose exec borgmatic-mailcow borgmatic init --encryption repokey-blake2`

### manual backup
`docker compose exec borgmatic-mailcow borgmatic -v 2`

### restore backup
`docker compose exec borgmatic-mailcow borgmatic extract --path mnt/data --archive latest`

### restart docker container after restore
`sudo docker compose down && sudo docker compose up -d`
