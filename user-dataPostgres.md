#!/bin/bash

sudo dnf update
sudo dnf install postgresql15.x86_64 postgresql15-server -y
sudo postgresql-setup --initdb
sudo systemctl start postgresql
sudo systemctl enable postgresql
sudo systemctl status postgresql