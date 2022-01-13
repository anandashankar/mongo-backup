# mongo-backup
use node-cron for taking mongo backups in specified intervals 
npm i node-cron
Currently, the app backup cron schedule: At 22:00 on every day-of-week from Monday through Friday

use mongo-dump for taking backup. The has to be a dump folder in the app directory:
mongodump --db=dbname --archive=./dbname.gzip --gzip

using mongo-restore to mount db from backup:
mongorestore --db=dbname --archive=dbname.gzip --gzip
