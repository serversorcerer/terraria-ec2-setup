# Terraria Server on AWS EC2 Guide

This repository provides a comprehensive guide for setting up a Terraria game server on an Amazon Web Services (AWS) EC2 instance, optimized for cost efficiency with the use of Spot Instances.

## 📋 Prerequisites

- An active AWS account.
- Familiarity with AWS services, particularly EC2.
- Basic knowledge of Windows server administration.
- An RDP client for connecting to the Windows instance.

## 🚀 Quick Start

1. **Provision EC2 Spot Instance**: Choose a suitable Windows AMI, configure your instance specifications, and define your spot price.
2. **Configure Security Groups**: Enable traffic on TCP ports 7777 (Terraria) and 3389 (RDP).
3. **Establish RDP Connection**: Use your instance's public IP and the retrieved admin password from the EC2 console.
4. **Deploy Terraria Server**: Utilize SteamCMD for the game server installation.
5. **Server Configuration**: Execute `TerrariaServer.exe` to customize your server setup.
6. **Ongoing Maintenance**: Implement regular backups of your game world and monitor server performance.

## 📘 Detailed Guide

### Setting Up the Instance

- **Spot Instance Request**: Request a Spot Instance from the EC2 dashboard, select a Windows Server AMI, and configure the instance details and storage options.
- **Security Group Setup**: Modify the security group to allow Terraria's required TCP port 7777 and RDP port 3389.

### Instance Connection

- **Remote Desktop**: Connect to your instance via RDP using the public IP address provided.
- **Password Retrieval**: Decrypt the admin password using your key pair in the EC2 console.

### Server Installation

- **SteamCMD Setup**: Download and execute SteamCMD. Install Terraria server files.
- **Terraria Configuration**: Launch `TerrariaServer.exe` in the command line interface and follow the prompts to set up your world and port.

### Monitoring and Expenses

- **EC2 Dashboard**: Keep track of server health and metrics through the EC2 dashboard.
- **Expense Tracking**: Manage your costs effectively with the help of AWS Cost Explorer and Budgets.

### Regular Maintenance

- **Data Backups**: Securely back up your Terraria world to Amazon S3 or another reliable service.
- **Updates**: Regularly update your server using SteamCMD and Windows Update.

## 🛠 Troubleshooting

Encountered a hiccup? Here’s what to check:

- **Review Security Group Settings**: Verify if the security group rules are correctly applied.
- **Check Windows Firewall**: Make sure the Windows Firewall settings are not blocking necessary ports.
- **Examine Server Logs**: Inspect the Terraria server logs for specific error details.

## 🤝 Contributing

Your contributions are what make the community great. Feel free to fork this repository, submit pull requests, or open issues to suggest improvements or changes.

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

