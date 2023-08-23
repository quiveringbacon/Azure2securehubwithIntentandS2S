# Azure 2 securehubs with Routing Intent and S2S

This creates a vwan with 2 secure hubs and a couple of spoke vnets with VM's connected to vhub1 and 2 and onprem vnets with a S2S tunnel to each hub. Routing intent is setup to secure all private and internet traffic in each hub. You'll be prompted for the resource group name, your public ip and username and password to use for the VM's. NSG's are placed on the default subnets of each vnet allowing RDP access from your public ip. This also creates a logic app that will delete the resource group in 24hrs.
The topology will look like this:

![image](https://github.com/quiveringbacon/Azure2securehubwithIntentandS2S/assets/128983862/d2044a78-766f-4d0c-a261-1574c4ee8fb7)

You can run Terraform right from the Azure cloud shell by cloning this git repository with "git clone https://github.com/quiveringbacon/Azure2securehubwithIntentandS2S.git ./terraform".

Then, "cd terraform" then, "terraform init" and finally "terraform apply -auto-approve" to deploy.
