# Gitea installation on Raspberry pi

**Note: Work in progress**

Primary information was taken from ([here]https://pimylifeup.com/raspberry-pi-gitea/). Original installation guide is on Gitea docs ([webpage]https://docs.gitea.com/next/installation/install-from-binary)




Notes to add to text above:
1  sudo apt update
    2  sudo raspi-config 
    3  sudo apt upgrade
    4  sudo reboot
    5  sudo apt install git mariadb-server -y
    6  sudo adduser --disabled-login --gecos 'Gitea' git
    7  sudo mysql_secure_installation
    8  sudo mysql -u root

   17  sudo -u git -s
cd ~
mkdir gitea
cd gitea/
wget https://dl.gitea.com/gitea/1.21.0/gitea-1.21.0-linux-arm64 -O gitea
chmod +x gitea
ls -la
exit

   18  sudo nano /etc/systemd/system/gitea.service
   19  sudo systemctl enable gitea.service
   20  sudo systemctl start gitea.service
