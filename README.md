Azure VM Provisioning using Ansible 🚀
This repository contains an Ansible Playbook for provisioning Azure Virtual Machines along with necessary network components like resource groups, virtual networks, and security groups.

📂 Repository Structure

Azure_vm_provisioning/
│── roles/
│   ├── create_public_ip/
│   ├── create_resource_group/
│   ├── create_security_group/
│   ├── create_subnet/
│   ├── create_virtual_machine/
│   ├── create_virtual_network/
│── main.yml
│── README.md

✨ Features
✅ Automates the provisioning of Azure Virtual Machines
✅ Uses Ansible roles for modularity
✅ Creates all required network components (VNet, Subnet, Public IP, Security Group)
✅ Easy deployment using a single playbook

⚙️ Prerequisites
Before running the playbook, ensure you have:

An Azure Subscription
Installed Ansible and the required Azure collections:

bash
pip install ansible-core
ansible-galaxy collection install azure.azcollection
Configured Azure CLI authentication:

bash
az login

🚀 How to Use
1️⃣ Clone the Repository
bash
git clone https://github.com/KumariPriyaa25/Azure_vm_provisioning.git
cd Azure_vm_provisioning

2️⃣ Update Ansible Variables (if needed)
Modify vars files inside roles if you need to customize configurations.

3️⃣ Run the Playbook
bash
ansible-playbook vm_provisioning.yml

4️⃣ Verify the Deployment
After execution, you can check the deployed resources in the Azure portal or via CLI:

bash
az vm list -o table

🛠 Roles Explanation
Role Name	Description
create_resource_group ->	Creates an Azure resource group
create_virtual_network ->	Sets up a Virtual Network (VNet)
create_subnet -> 	Configures a subnet inside the VNet
create_security_group ->	Defines security rules for VM traffic
create_public_ip ->	Allocates a public IP for the VM
create_virtual_machine ->	Provisions the virtual machine with given specs

📝 Customization
To customize VM properties, update the vars section in the respective roles, such as:

yaml
vm_size: Standard_DS1_v2
admin_username: testvm
image: "UbuntuServer:Canonical:18.04-LTS:latest"

📄 License
This project is licensed under the MIT License.
