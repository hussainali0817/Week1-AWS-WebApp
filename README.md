# Week 1: AWS Static Website
## Progress
- Starting my Cloud Support journey!
- Created a new professional email (HussainA.Cloud@gmail.com) for roadmap accounts.
- Set up AWS Free Tier account to begin cloud projects.
- Configured LinkedIn profile with Co-Founder experience at HHCommerce LLC (2017–2023), focusing on e-commerce and wholesale retail.
- Uploaded resume to LinkedIn, highlighting technical support and automation skills.
- Joined r/aws community on Reddit using existing account for networking.
- Tested draw.io by creating an EC2-S3 diagram, preparing for the Week 1 architecture diagram.
- Finished AWS Cloud Practitioner Essentials Module 1 and aced the quiz (3/3 correct).
- Set $5/month budget alert in AWS to manage costs, with thresholds at 80% ($4) and 100% ($5).
- Completed AWS Cloud Practitioner Essentials Module 2 (compute services: EKS, ECS, SNS, SQS) and took the quiz.
- Explored AWS Console (EC2, S3, VPC)
- Read AWS EC2 Lab intro to prepare for instance setup.
- Launched an EC2 instance (Amazon Linux 2, t2.micro, Instance ID: [i-0bf4f1fd1fa058314], Public DNS: ec2-3-133-89-50.us-east-2.compute.amazonaws.com), saved .pem key securely, and connected via SSH on Windows.
- Created S3 test bucket (week1-test-bucket-hussain) and uploaded test.txt for Week 1 project.
## Friday, May 30, 2025: EC2 Static Website Setup
- Installed Apache on EC2 instance (Amazon Linux 2, t2.micro, Public DNS: ec2-3-133-89-50.us-east-2.compute.amazonaws.com) using `sudo yum install httpd -y`, started and enabled with `systemctl`, verified with `curl localhost`.
- Deployed website files: Downloaded test.txt from S3, uploaded to /var/www/html/, created index.html ("Hello World" page with link to test.txt), set permissions, tested with `curl localhost`.
- Configured EC2 security group: Added HTTP rule (port 80, source: Anywhere), tested website in browser (`http://ec2-3-133-89-50.us-east-2.compute.amazonaws.com`), confirmed test.txt link worked.
- Stopped EC2 instance to pause Free Tier usage.
## Monday, June 2, 2025: Home Lab Network Setup
- Configured home lab network: Enabled DHCP on AT&T router (IP: 192.168.1.254, range: 192.168.1.64–192.168.1.253), assigned static IPs (desktop: 192.168.1.10 via Ethernet settings, Ubuntu VM: 192.168.1.11 via /etc/netplan/01-network-manager-all.yaml in VirtualBox, Bridged Adapter, interface: enp0s3). Tested connectivity with ping (desktop to VM: 192.168.1.11, VM to desktop: 192.168.1.10), 0% packet loss after troubleshooting (enabled ICMP via Windows Defender Firewall).
- Simulated IP conflict: Changed VM IP to 192.168.1.10 (same as desktop), ping failed (Request timed out). Troubleshooted: Checked IPs with `ip addr` (VM) and `ipconfig` (desktop), identified conflict, reverted VM to 192.168.1.11, retested connectivity—successful (ping replies: 0% packet loss).
## Tuesday, June 3, 2025: NextWork VPC Projects – Parts 0, 1, & 2
- Completed NextWork "AWS Networks Intro" project: Quick read-through, learned key concepts (e.g., VPC: virtual network in AWS, Subnet: smaller network within a VPC).
- Completed NextWork "Build a Virtual Private Cloud (VPC)" project: Created a VPC (name: NextWork VPC, CIDR: 10.0.0.0/16, VPC ID: [vpc-id]), created a public subnet (name: Public 1, CIDR: 10.0.0.0/24, Subnet ID: [subnet-id], Availability Zone: [e.g., us-east-1a], enabled auto-assign public IPv4 address), created and attached an internet gateway (name: NextWork IG, ID: [igw-id]).
- Completed NextWork "VPC Traffic Flow and Security" project: Created a route table (name: NextWork route table, ID: [rtb-id], added route to NextWork IG), created a security group (name: NextWork Security Group, ID: [sg-id], allowed HTTP port 80 from Anywhere-IPv4), created a network ACL (name: NextWork Network ACL, ID: [acl-id], allowed all traffic inbound/outbound, associated with Public 1).
