# Terraria Server on AWS EC2 Guide with Network Load Balancer

This repository provides a comprehensive guide for setting up a Terraria game server on an Amazon Web Services (AWS) EC2 instance. This setup is optimized for performance and security with the use of Network Load Balancer (NLB) and Spot Instances.

## 📋 Prerequisites

- An active AWS account.
- Familiarity with AWS services, especially EC2 and NLB.
- Basic knowledge of Windows server administration.
- An RDP client for connecting to the Windows instance.

## 🚀 Quick Start

1. **Provision EC2 Spot Instance**: Choose a suitable Windows AMI, configure your instance specifications, and set your spot price.
2. **Configure Security Groups**: Restrict traffic on TCP ports 7777 (Terraria) and 3389 (RDP) to only known IPs for enhanced security.
3. **Establish RDP Connection**: Use your instance's public IP and the retrieved admin password from the EC2 console.
4. **Deploy Terraria Server**: Utilize SteamCMD for the game server installation.
5. **Server Configuration**: Execute `TerrariaServer.exe` to customize your server setup.
6. **Setup Network Load Balancer**: Configure NLB to manage incoming traffic on port 7777.
7. **Ongoing Maintenance**: Implement regular backups of your game world and monitor server performance through the EC2 dashboard.

## 📘 Detailed Guide

### Setting Up the Instance

- **Spot Instance Request**: Launch a Spot Instance from the EC2 dashboard, choosing a Windows Server AMI and configuring instance details.
- **Security Group Setup**: Modify the security group to allow Terraria's required TCP port 7777 and RDP port 3389 from specific IP addresses only.

### Network Load Balancer Configuration

- **Create NLB**: Set up a Network Load Balancer in your VPC that listens on TCP port 7777.
- **Target Group Configuration**: Associate your EC2 instance with a target group under the NLB to handle traffic routing.

### Instance Connection and Server Deployment

- **Remote Desktop**: Connect to your instance via RDP using the provided public IP address.
- **Password Retrieval**: Decrypt the admin password using your key pair in the EC2 console.
- **SteamCMD Setup**: Download and execute SteamCMD, then install Terraria server files.
- **Terraria Server Launch**: Use `TerrariaServer.exe` to configure your server.

### Monitoring and Security

- **NLB Monitoring**: Monitor load balancer performance and health checks to ensure traffic is correctly routed.
- **Security Enhancements**: Regularly update the security group settings to maintain tight security as IP addresses change.

### Regular Maintenance

- **Data Backups**: Back up your Terraria world to Amazon S3 or similar services.
- **Server Updates**: Keep the server up to date using SteamCMD and regular Windows updates.

## 🛠 Troubleshooting

Encountered issues? Check the following:

- **Security Group Settings**: Ensure the security group rules allow traffic only from designated IPs.
- **NLB Health Checks**: Confirm that the NLB health checks pass and that the EC2 instance is marked as healthy.
- **Server Logs**: Review the Terraria server logs for error messages or connectivity issues.

## 🤝 Contributing

Contributions are welcome! Fork this repository, propose changes through pull requests, or submit issues to discuss enhancements and fixes.

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
