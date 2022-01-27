# Portainer
  
<p align="left">
  <a href="https://github.com/vdarkobar/Home_Cloud#small-home-cloud">Home</a> |
  <a href="https://github.com/vdarkobar/Portainer">Portainer</a> |
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
