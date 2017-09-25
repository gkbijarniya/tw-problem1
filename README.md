# tw-problem1

### 1. Prerequisite

Need to install VirtualBox & Vagrant on the local box.

### 2. Create the Setup

It will create the VM and setup for docker containerization.  
```
git clone https://github.com/gkbijarniya/tw-problem1.git
cd tw-problem1.git
vagrant up
```

### 3. Create the Training environment

#### 3.1 Build the environment

```
vagrant ssh -c "cd /vagrant/train && sudo docker-compose build"
```

#### 3.2 Run the environment

```
vagrant ssh -c "cd /vagrant/train && sudo docker-compose up -d"
```

#### 3.3 Test the environment

Access the url http://localhost:8080 from the localhost/host


#### 3.4 Scale the environment

```
vagrant ssh -c "cd /vagrant/train && sudo docker-compose scale web=2"
```

#### 3.5 Shutdown the environment

```
vagrant ssh -c "cd /vagrant/train && sudo docker-compose down"
```


### 4. Create the Production environment

#### 4.1 Build the environment

```
vagrant ssh -c "cd /vagrant/prod && sudo docker-compose build"
```

#### 4.2 Run the environment

```
vagrant ssh -c "cd /vagrant/prod && sudo docker-compose up -d"
```

#### 4.3 Test the environment

Access the url http://localhost:8080 from the localhost/host


#### 4.4 Scale the environment

```
vagrant ssh -c "cd /vagrant/prod && sudo docker-compose scale web=2"
```

#### 4.5 Shutdown the environment

```
vagrant ssh -c "cd /vagrant/prod && sudo docker-compose down"
```

