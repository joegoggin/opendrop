# Open Drop

opendrop is a script I made to automate opening ssh sessions to access
digital ocean droplets

* note that this script assumes that you have already set up an ssh key with 
digital ocean and stored your private key inside ~/.ssh/digital-ocean-key

* Also note that in order to use the syntax below you need to add a path to 
your project directory into your .bashrc file. This video does a good job of 
explaining it: https://www.youtube.com/watch?v=abN6bvyPRxQ&ab_channel=Linode
You can also just run it from within this directory by adding bash infront of
the command


example: bash opendrop -n name open 


Usage: 
```
opendrop [options] command 
```

Commands:

open - opens an ssh session for a digital ocean droplet
list - list all saved droplets
add  - add a new droplets


# open 

Usage: 
```
opendrop [-i | -n] open 
```

Options:
    -i : open droplet with ip address
    -n : open droplet by name

example 1: 
```
opendrop -i 1.1.1.1 open
```

example 2: 
```
opendrop -n name open
```

# list

Usage: 
```
opendrop [-a | -i | -n] list 
```

Options:
    -a  : lists all stored names and ip addresses
    -i : lists all stored ip addresses
    -n : lists all stored names

example:
```
opendrop -a list
```

# add 

Usage: 
```
opendrop [-i | -n] add
```

Options:
    -i : add droplet ip address
    -n : add droplet name
   
example: 
```
opendrop -i 1.1.1.1 -n name add
```


