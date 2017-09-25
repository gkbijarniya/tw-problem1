# tw-problem1

### Prerequisite

Need to install VirtualBox & Vagrant on the local box.

### Create the environment

It will create the VM and setup for docker containerization.  
```
git clone https://github.com/gkbijarniya/tw-problem1.git  
vagrant up
```

### Create the Training environment

#### Build the environment

```
vagrant ssh -c "cd /vagrant/train && sudo docker-compose build"
```

#### Run the environment

```
vagrant ssh -c "cd /vagrant/train && sudo docker-compose up -d"
```

#### Test the environment

Access the url http://localhost:8080 from the localhost/host


#### Scale the environment

```
vagrant ssh -c "cd /vagrant/train && sudo docker-compose scale web=2"
```

#### Shutdown the environment

```
vagrant ssh -c "cd /vagrant/train && sudo docker-compose down"
```


### Create the Production environment

#### Build the environment

```
vagrant ssh -c "cd /vagrant/prod && sudo docker-compose build"
```

#### Run the environment

```
vagrant ssh -c "cd /vagrant/prod && sudo docker-compose up -d"
```

#### Test the environment

Access the url http://localhost:8080 from the localhost/host


#### Scale the environment

```
vagrant ssh -c "cd /vagrant/prod && sudo docker-compose scale web=2"
```

#### Shutdown the environment

```
vagrant ssh -c "cd /vagrant/prod && sudo docker-compose down"
```

