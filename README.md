# Rubystrap

Rubystrap makes it easier to take a server from OS to Chef'd. 

## Usage

There are three core parts of rubystrap. Bootstrapping for Chef, copying
the require chef-solo files to the system, and then running Chef.

```bash
# Start by setting your target as an environment variable.
export RUBYSTRAP_TARGET=root@192.168.1.10

# setup will install the specified ruby version on the remote system. 
# If no version is specified it will install whatever the current rubystrap 
# default is.
rubystrap setup 1.9.2-p290

# copy will copy the specified chef-solo files to the remote system. If no 
# folder is specified it will default to your current working directory.
rubystrap copy /path/to/chef-solo/files

# provison will run chef-solo on the target with the specified config.
rubystrap provsion webserver
```
