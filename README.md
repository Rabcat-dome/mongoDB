# mongoDB
จัดทำรูปแบบ Persistent Storage
จัดทำ version docker และแบบ swarm

# script Authen
docker exec -it mongo mongo

use admin
db.createUser({
  user: "admin",
  pwd: "password",
  roles: [ { role: "root", db: "admin" } ]
})

mongo -u "admin" -p "password" --authenticationDatabase "admin"
