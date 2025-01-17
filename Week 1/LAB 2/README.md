# Lab 2: Manage Linux VMs with the Azure CLI

Task: 

1. Create resource group
created resource group with the command 
 az group create --name myResourceGroupVM --location eastus 
2. Create virtual machine
i created virtual machine with  the command 
az vm create \
    --resource-group myResourceGroupVM \
    --name myVM \
    --image UbuntuLTS \
    --admin-username azureuser \
    --generate-ssh-keys
3. Connect to VM
i connected to vm succesfully      with command 
ssh azureuser@52.168.142.199
4. Understand VM images
i understood vm images withthe following command
az vm image list --output table
az vm image list --output table
5. Understand VM sizes
i understand with the following command
az vm list-sizes --location eastus --output table
6. VM power states
i did with the following command
az vm get-instance-view \
    --name myVM \
    --resource-group myResourceGroupVM \
    --query instanceView.statuses[1] --output table
7. Management tasks
i did  with following command
az vm list-ip-addresses --resource-group myResourceGroupVM --name myVM --output table

Notes:
Quickstart: Create a Linux VM

https://docs.microsoft.com/en-us/azure/virtual-machines/linux/tutorial-manage-vm
Quickstart for Bash in Azure Cloud Shell

https://docs.microsoft.com/en-us/azure/cloud-shell/quickstart