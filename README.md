# Portainer
WebUI for Containers

### Clone this git repository
```
echo -n "Enter directory name: "; read NAME; mkdir -p "$NAME"; cd "$NAME" \
&& git clone https://vdarkobar:2211620c9da5dab0c7bb77e9aeb02087d293b293@github.com/vdarkobar/Portainer.git .
```
  
##### Add passwords and change premissions, *adjust folder name*
```
echo | openssl rand -base64 20 > secrets/portainer_admin_password.secret
sudo chown -R root:root secrets/
```  
##### Start
```
sudo docker-compose up -d
```
