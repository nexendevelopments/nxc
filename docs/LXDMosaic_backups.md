## Backing up your instace


- **You should regullary backup your containers & data**
- This is not backup advise for LXD, **only NEXENCloud**

There are a couple of ways to backup your NEXENCloud instance, if you have
deployed the NEXENCloud application in a container, you can just copy the container
to another LXD Host.

#### What needs backing up

 - MySQL database

The database is the only part of this application that needs to be backed up.
By backing it up your retain

 - Cloud-config information stored in NEXENCloud
 - Stats gathered about the fleets history (active containers, memory usage etc)
 - Deployments information & configurations

_The rest of the information is read directly from your LXD instances._

#### How to backup

The best way to backup would be to create a dump of the database like so:

`mysqldump -u NEXENCloud_DB_User -p NEXENCloud_DB_Password LXD_Manager > BACKUP_Name.sql`

**You should then move the BACKUP_Name.sql to an offsite server / secure location**
