# openvpn_as
 ## Installation of openvpn server
 ### Clone the repository
   git clone git clone https://github.com/Saurav66/openvpn_as.git
 ### Give the Execute permission of script file
   sudo chmod +x openvpn-install.sh
 ### Run the script file
    sudo bash openvpn-install.sh
 ### Check openvpn services
   #### For ubuntu/Debian
    sudo systemctl status openvpn
    sudo systemctl start openvpn
    sudo systemctl enable openvpn
   #### For RHEL/CentOS
    sudo service openvpn status
    sudo service openvpn start
    sudo service openvpn enable
    
    ![install](https://user-images.githubusercontent.com/50103349/152930229-1aba2bd1-eeda-4db2-bc97-ae74ccd15a60.png)
 ## Install openvpn on client server
    sudo apt install openvpn
   #### If openvpn install on Desktop system 
    sudo apt install network-manager-openvpn
 ### Check openvpn service
    sudo systemctl status openvpn
 ### Download the .ovpn client file form openvpn server 
     File location of client file: /etc/openvpn/
   #### Copy on client server using scp (secure copy) and ftp
     On openvpn server:
        sudo scp .ovpn hostname@ip_add:/file_location
     On openvpn client server:
        sudo scp hostname@ip_add:/file_location_of_ovpn .
 #### Start openvpn client service:
     sudo systemctl start openvpn@client.service

