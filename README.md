# dokcer-tools
````
apt-get update && apt-get upgrade -y
apt  install docker.io docker-compose -y

sudo apt install curl
sudo curl -L "https://github.com/docker/compose/releases/download/1.26.0/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
sudo docker–compose --version


git clone https://github.com/falconsoft3d/jamfnow-api
cd jamfnow-api
npm i
docker-compose build
docker-compose up -d
````

# Abrir un docker
````
docker exec -it 4302d9c7b44b  bash
````

# Install nano
````
apk update
apk add nano
````

# Portainer
````
docker pull portainer/portainer
docker run -d -p 9000:9000 -p 8000:8000 --name portainer --restart always -v /var/run/docker.sock:/var/run/docker.sock -v /path/on/host/data:/data portainer/portainer
````


# NetData
````
git clone git@github.com:falconsoft3d/docker-tools.git

cd docker-tools/monitore/netdata

docker run -d --name=netdata \
  -p 19999:19999 \
  -v /etc/passwd:/host/etc/passwd:ro \
  -v /etc/group:/host/etc/group:ro \
  -v /proc:/host/proc:ro \
  -v /sys:/host/sys:ro \
  -v /var/run/docker.sock:/var/run/docker.sock:ro \
  --cap-add SYS_PTRACE \
  --security-opt apparmor=unconfined \
  netdata/netdata
````
