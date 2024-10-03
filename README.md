Install SSH on Ubuntu OpenSSH is not pre-installed on the system, so let's install it manually. To do this, type in the terminal: sudo apt install openssh-server The installation of all the necessary components will begin. Answer "Yes" to all the system prompts. After the installation is complete, go to the next step to start the service.
(https://github.com/Dyairza/Irza-Dya-Tyasna_09011282328090_sistem-operasi-tugas-7/blob/main/1.png)
Start SSH Now you need to enable the service you just installed using the command below: sudo systemctl enable --now ssh
(https://github.com/Dyairza/Irza-Dya-Tyasna_09011282328090_sistem-operasi-tugas-7/blob/main/2.png)
On successful startup, you will see the following system message. The --now key helps you launch the service and simultaneously set it to start when the system boots. To verify that the service is enabled and running successfully, type: sudo systemctl status ssh The output should contain the Active: active (running) line, which indicates that the service is successfully running. If you want to disable the service, execute:
(https://github.com/Dyairza/Irza-Dya-Tyasna_09011282328090_sistem-operasi-tugas-7/blob/main/3.png)
sudo systemctl disable ssh It disables the service and prevents it from starting at boot.
(https://github.com/Dyairza/Irza-Dya-Tyasna_09011282328090_sistem-operasi-tugas-7/blob/main/4.png)
(https://github.com/Dyairza/Irza-Dya-Tyasna_09011282328090_sistem-operasi-tugas-7/blob/main/5.png)
Configure the firewall Before connecting to the server via SSH, check the firewall to ensure it is configured correctly. In our case, we have the UFW installed, so we will use the following command: sudo ufw status In the output, you should see that SSH traffic is allowed. If you don't have it listed, you need to allow incoming SSH connections. This command will help with this: sudo ufw allow ssh

Configure the firewall Before connecting to the server via SSH, check the firewall to ensure it is configured correctly. In our case, we have the UFW installed, so we will use the following command: sudo ufw status In the output, you should see that SSH traffic is allowed. If you don't have it listed, you need to allow incoming SSH connections. This command will help with this: sudo ufw allow ssh

