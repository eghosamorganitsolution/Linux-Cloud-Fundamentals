# Lab 1: Create a Linux virtual machine with the Azure CLI

The objective of the lab is to get you familiar with Azure CLI.
There are guides under this lab to help you navigate through the tasks. 
Happy Learning.


1. Launch Azure Cloud Shell
answer:
a. https://portal.azure.com/
b.click cloud shell icon
c.it will actually ask for payment details but i already did it before
d i Launched Azure Cloud Shell lauched


2. Create a resource group
created a resource group with the command  az group create --name myResourceGroup --location eastus
3. Create virtual machine
created virtual machine  with command   
 az vm create \
  --resource-group myResourceGroup \
  --name myVM \
  --image Debian \
  --admin-username azureuser \
  --generate-ssh-keys
  note: my  "publicIpAddress": "20.228.195.169",
4. Open port 80 for web traffic
i did with this
az vm open-port --port 80 --resource-group myResourceGroup --name myVM

5. Connect to virtual machine
i connected the virual machine
6. Install web server
i did with the command 
az vm run-command invoke \
   -g myResourceGroup \
   -n myVM \
   --command-id RunShellScript \
   --scripts "sudo apt-get update && sudo apt-get install -y nginx"
7. View the web server in action
i viewed my web server successfully using my public ip 20.228.195.169



Notes:
Quickstart: Create a Linux VM

https://docs.microsoft.com/en-us/azure/virtual-machines/linux/quick-create-cli

Quickstart for Bash in Azure Cloud Shell

https://docs.microsoft.com/en-us/azure/cloud-shell/quickstart