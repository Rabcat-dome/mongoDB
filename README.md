# mongoDB
จัดทำรูปแบบ Persistent Storage
จัดทำ version docker และแบบ swarm

# script Authen
docker exec -it mongo mongosh

use admin
db.createUser({
  user: "admin",
  pwd: "Gumon#2024",
  roles: [ { role: "root", db: "admin" } ]
})

mongo -u "admin" -p "Gumon#2024" --authenticationDatabase "admin"