#step by step process for the completion of this project

#step 1
-  created a MarketPeak_Ecommerce directory using git bash
  { [ **mkdir MarketPeak_Ecommerce
    cd MarketPeak_Ecommerce
    git init**]}

-  created an Html file by downloading an E-commerce web template
-  successfully added and commited the changes on the main branch
   ** { [  git add .
       git config --global user.name "YourUsername"
       git config --global user.email "youremail@example.com"
       git commit -m "Initial commit with basic e-commerce site structure"]**

**[git remote add origin https://github.com/your-git-username/MarketPeak_Ecommerce.git]}

[git push -u origin master]**

#step 2
-  successfuly logged into the AWS console 
-  launched and EC2 instance

 [ **cat /home/ubuntu/.ssh/id_rsa.pub**
**git clone https://github.com/devops-tobi/MarketPeak_Ecommerce.git**]

-  installed a web server (Apache) on the EC2 instance
**  [sudo yum update -y
sudo yum install httpd -y
sudo systemctl start httpd
sudo systemctl enable httpd]**

-  configured the server to be able to deploy from a web server using the public IP on the EC2 instance
** [ sudo rm -rf /var/www/html/*
sudo cp -r ~/MarketPeak_Ecommerce/* /var/www/html/**
**sudo systemctl reload httpd]**


#step 3
-  created another development branch using git bash
  **[git branch development
git checkout development]**

-  made sum changes and used a PR and push command to push it to the main branch
**[git add .
git commit -m "Add new features or fix bugs"
git push origin development
git checkout master
git merge development
git push origin master
git pull origin main
sudo systemctl reload httpd]**

#challenges:
**[connecting the server with the EC2 instance, the server was unable to start until i used the "sudo systemctl start apache2" command.]**

