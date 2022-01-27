# Portainer
  
<p align="left">
  <a href="https://github.com/vdarkobar/Home_Lab">Home</a>
</p>  
  
### Clone this git repository
```
echo -n "Enter directory name: "; read NAME; mkdir -p "$NAME"; cd "$NAME" \
&& git clone https://vdarkobar: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@github.com/vdarkobar/Portainer.git .
```
  
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
