echo "# demodq2" >> README.md
git init
git add README.md
git add *
git commit -m "commit demo dq v1.0"
git remote add origin https://github.com/olivierlemaire/demodq2.git
git push -u origin master

git commit -m "commit demo dq v2.0"
git add
git push -u origin master


ssh -i $HOME/.ssh/isg-key1.pem ec2-user@ec2-34-249-34-82.eu-west-1.compute.amazonaws.com

#install codedeploy agent
#sudo yum update
sudo yum install ruby
sudo yum install wget
cd /home/ec2-user
wget https://aws-codedeploy-eu-west-1.s3.amazonaws.com/latest/install
chmod +x ./install
sudo ./install auto

sudo yum install httpd
sudo service httpd start
sudo service httpd status


#service role
arn:aws:iam::049414109541:role/olmCodeDeployServiceRole



