# Mongodb for ubuntu 22.04 jammy

Reference docs: [Install MongoDB Community Edition on Ubuntu](https://www.mongodb.com/docs/manual/tutorial/install-mongodb-on-ubuntu/)

> MongoDB 6.0 Community Edition supports the ubuntu 22.04 LTS ("Jammy).


## Import the public key used by the package management system
`$ wget -qO - https://www.mongodb.org/static/pgp/server-6.0.asc | sudo apt-key add -`

## Create a list file for MongoDB
>To check os code name: `$ lsb_release -dc`

`$ echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu jammy/mongodb-org/6.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-6.0.list`

## Reload local package database
`$ sudo apt-get update`

## Install the MongoDB packages
`$ sudo apt-get install -y mongodb-org`

## Run MongoDB Community Edition
> To find system init: `$ ps --no-headers -o comm 1`

## Start MongoDB
`$ sudo systemctl start mongod`

## Verify that MongoDB has started successfully
`$ sudo systemctl status mongod`
