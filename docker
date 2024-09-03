#!
clear
echo is this an upgrade?
read upgrade
echo
echo

if [ $upgrade == "yes" ]

then
	echo yum is an alias for the dnf utility.
        echo
        echo
        sudo yum remove docker \
                  docker-client \
                  docker-client-latest \
                  docker-common \
                  docker-latest \
                  docker-latest-logrotate \
                  docker-logrotate \
                  docker-engine \
                  podman \
                  runc
        echo
        echo
        echo setting up repo
        echo
        echo
	sudo yum upgrade -y yum-utils
        sudo yum-config-manager --add-repo https://download.docker.com/linux/rhel/docker-ce.repo
        echo
        echo
        echo installing docker engine
        echo
        echo
        sudo yum upgrade -y docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
        sudo systemctl start docker
        echo
        echo
	
else
	echo yum is an alias for the dnf utility. 
	echo
	echo
	sudo yum remove docker \
                  docker-client \
                  docker-client-latest \
                  docker-common \
                  docker-latest \
                  docker-latest-logrotate \
                  docker-logrotate \
                  docker-engine \
                  podman \
                  runc
	echo
	echo
	echo setting up repo
	echo
	echo
	sudo yum install -y yum-utils
	sudo yum-config-manager --add-repo https://download.docker.com/linux/rhel/docker-ce.repo
	echo
	echo
	echo installing docker engine
	echo
	echo
	sudo yum install -y docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin 
	sudo systemctl start docker
	echo
	echo
fi

