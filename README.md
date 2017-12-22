## DOCKERIZED REDIS BACKUP

> This  is a dockerized data backup application for Redis ( open source in-memory data structure store).
> It have a two docker container  linked  through docker-compose util.
> The Main container "redis-main" created only for example, and not need in real backup operations.
> If you want to schedule backup, then you must use cron in docker host or  add it in the backup container.


- How to run 
 - Change docker-compose.yml file. Remove the redis-main service,  and add or change vars.
 - If  you had two or  more regions in Amazon Glacier Service  you must check file  redis-backup/backup.sh and add(change)  your regions. Vars in .env file will be  ignored.
 - Run container used command
  ```
   docker-compose run redis-backup
  ```
 - Add in your cron like program schedule
   ```
   
   ```
 
 
- [x] Work with containers :whale:
- [x] Send Slack notifications :fire:
- [x] Send arhive to glacier :vhs:
- [] Rewrite program (go,python,etc.) :rabbit:
- [] Migration to kubernetes (for sheduled operations)

