---
title: Module 02: Setup
body-class: index-page
---

## Module 02 - Setup

The lab enviornment doesn't work properly when it installs the app. We'll build another EC2 instance to use instead.

## Create an EC2 Instance

* Name: CafeWebServer2
* AMI: Linux 2023
* t2.medium
* vockey
* Network settings -> edit
    * LabVPC
    * PublicSubnet    
    * Enable Auto-Assign IP
    * aws-cloud9-Cloud9-Lab-IDE security group

Open EC2 service, change Instance Metadata: Actions -> Instance Settings ->Modify Instance Metadata options

Change IDMSv2 Optional (originally Required), press Save

Actions->Security->Modify IAM Role
Add the LabInstanceProfile Role


Update aws-cloud9-Cloud9-Lab-IDE Security Group to allow port 22 from everywhere
Update aws-cloud9-Cloud9-Lab-IDE Security Group to allow port 80 from everywhere

!!! note "OPTIONAL"

    If you want to make things easier for yourselves, you may want to add an elastic IP to that instance as well. That way your cloud 9 connection will continue to work without needing to go in and change the IP address.

Connect to the EC2 instance

Run the following commands, one line at a time:

```
sudo dnf -y update
sudo systemctl enable amazon-ssm-agent
sudo systemctl start amazon-ssm-agent
sudo dnf install -y httpd wget php-fpm php-mysqli php-json php php-devel
sudo dnf install mariadb105-server
sudo dnf install nmap
sudo systemctl enable httpd
sudo systemctl start httpd
sudo systemctl enable mariadb
sudo systemctl start mariadb
sudo usermod -a -G apache ec2-user
exit
```

You just logged out, you'll need to reconnect to the EC2 instance and run these commands as well:

```
sudo touch /var/www/html/index.html
sudo chown -R ec2-user:apache /var/www
sudo echo '<html><h1>Web server is working. Access the <a href="cafe">cafe website</a>.</h1></html>' > /var/www/html/index.html
find /var/www -type d -exec chmod 2775 {} \;
chmod 2775 /var/www

wget https://byui-cse.github.io/itm310-course/module-02/setup.zip
unzip setup.zip
wget https://byui-cse.github.io/itm310-course/module-02/db.zip
unzip db.zip
wget https://byui-cse.github.io/itm310-course/module-02/cafe.zip
unzip cafe.zip -d /var/www/html/

cd ./db
sudo bash ./set-root-password.sh
sudo bash ./create-db.sh

mkdir /home/ec2-user/environment
mkdir /home/ec2-user/environment/samplelogs

wget -P /home/ec2-user/environment/samplelogs/ https://aws-tc-largeobjects.s3.us-west-2.amazonaws.com/CUR-TF-200-ACCAP4-1-79925/capstone-4-clickstream/s3/access_log.log

wget -P /home/ec2-user/environment/samplelogs/ https://aws-tc-largeobjects.s3.us-west-2.amazonaws.com/CUR-TF-200-ACCAP4-1-79925/capstone-4-clickstream/s3/access_log_geo.log

sudo yum install -y gcc nodejs
sudo yum -y groupinstall "Development Tools"
sudo yum -y install python-pip
sudo yum -y install collectd
ln -s /var/www/ /home/ec2-user/www
cd /home/ec2-user/environment
wget https://aws-tc-largeobjects.s3.us-west-2.amazonaws.com/CUR-TF-200-ACCAP4-1-79925/capstone-4-clickstream/s3/log-gen.py
chmod +x log-gen.py

wget https://aws-tc-largeobjects.s3.us-west-2.amazonaws.com/CUR-TF-200-ACCAP4-1-79925/capstone-4-clickstream/s3/log-gen_geo.py
chmod +x log-gen_geo.py

cd /home/ec2-user/environment/samplelogs

sed -i "s/2023-02-23/$(date '+%Y-%m-%d')/" access_log.log

sed -i "s/2023-02-23/$(date '+%Y-%m-%d')/" access_log_geo.log



sudo sed -i "2i date.timezone = \"America/New_York\" " /etc/php.ini
sudo service httpd restart
```


## Create a Cloud 9 Connection to the New EC2 Instance

Open a new tab on AWS and search for Cloud9 in services.
Click Create Environment in the Cloud9 service area.

* Name: NewCloud9
* Existing Compute
* Copy the key to clipboard
    * Open the tab that has your EC2 console

```
cd ~/.ssh/
sudo vim authorized_keys
```

* press a
* click end
* click enter
* right click paste the key at the end of the file
* press esc
* press :
* type wq
* press enter

Go back to the cloud 9 tab

* User: ec2-user
* Host: paste the public IP address of your EC2 Instance
* Click Create

Once this is completed. Click on "Open" next to NewCloud9

You can now continue with the AWS Lab instructions, starting at **Phase 2, Task 3**.

