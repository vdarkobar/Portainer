# Portainer
  
<p align="left">
  <a href="https://github.com/vdarkobar/Home_Cloud#small-home-cloud">Home</a> |
  <a href="https://github.com/vdarkobar/NextCloud#nextcloud">NextCloud</a> |
  <a href="https://github.com/vdarkobar/Bitwarden#bitwarden">Bitwarden</a> |
  <a href="https://github.com/vdarkobar/WordPress#wordpress">WordPress</a> |
  <a href="https://github.com/vdarkobar/Ghost-blog#ghost-blog">Ghost-blog</a>
  <br><br>
</p>   
  
### Clone this git repository
```
echo -n "Enter directory name: "; read NAME; mkdir -p "$NAME"; cd "$NAME" \
&& git clone https://github.com/vdarkobar/Portainer.git .
```
<!-- If repo is private then add auth token-->
<!-- https://vdarkobar:<access-token>@github.com/vdarkobar/Portainer.git . -->
  
##### Add passwords and change premissions
```
echo | openssl rand -base64 20 > secrets/portainer_admin_password.secret
sudo chown -R root:root secrets/
```  
##### Start
```
sudo docker-compose up -d
```
##### Login (username: admin), pass:
```
cat secrets/portainer_admin_password.secret
```
##### Go to: Environments > primary > Public IP, and add local IP address of the VM.
  
#####  Copy of original links, if using cusstom templates (settings page): 
```
App Templates
URL > https://raw.githubusercontent.com/portainer/templates/master/templates-2.0.json
  
Helm Repository
URL > https://charts.bitnami.com/bitnami
```
  
<p align="center">
<a href="https://github.com/vdarkobar/Portainer">top of the page</a>
</p>

