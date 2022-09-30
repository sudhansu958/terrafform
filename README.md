# terraform_instance_ec2

#creating a file name p2
mkdir p2
#creating creds.tf
vi creds.tf
#aws credentials
provider "aws"{
 access_key="ASIATSVOPX3DF3Q6IOTI"
 secret_key="QX+DbgNO5zHo+18P0VXQ6NkwEDfkHs3s4evi/DBC"
 token="FwoGZXIvYXdzELv//////////wEaDAlWUx2VKqLGrmuKWiKyAbzidIH6V5wKDf1Ml52a1wSvaohwdL9zRpulde8tJC97JbsLRBA38d52IPsfJocSxj3LQzZcYcA6VtV5XaJ3vy5lNze/FCet4ot7dVBD+s2tNrcnd9hWV94ewsRI3/Iy/og2loIn3XYt0q4IJ5YcuSV4Avo6KGZQjbe9LWRAQQZCpptnTSK+o29xMibRQfXpFXXln0FJiZnJ5PpSCZwOXa2qqp5hL1A6rZUlSDfzegrX2dQopNncmQYyLZGgoURRGGZSn83N1eJcT8YS/6gd9OwkE/YkxapUt3bYc3TFjEIcn7IyfgeqDg=="
 region="us-east-1"
}
#creating main.tf for resource details of ec2 ubuntu instance
vi main.tf
#aws resource file
resource "aws_instance" "example" {
  


  ami           = "ami-08c40ec9ead489471"#ubuntu ami no



  instance_type = "t2.micro"#instance type

 key_name="hipan"#key pair name hipan.pem

}
#then we must use terraform init
terraform init
#then terraform apply to create aws ec2 instance
terraform apply

#it is time to go to aws console
#doing ssh into ubuntu instance
command chmod 400 hipan.pem
#doing ssh to ubuntu
ssh -i "hipan.pem" ubuntu@54.175.186.167

#now we are in the ubuntu instance
lets install java 

#command to instal java
sudo apt install openjdk-11-jre-headless 
#to check java --version
java --version
#to install python
sudo apt-get install python3
#to check python version
python3 --version
#to download jenkins on ubuntu
 wget -q -O - https://pkg.jenkins.io/debian-stable/jenkins.io.key |sudo gpg --dearmor -o /usr/share/keyrings/jenkins.gpg
 sudo sh -c 'echo deb [signed-by=/usr/share/keyrings/jenkins.gpg] http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'
#update the dependencies
 sudo apt update
#jenkins download command
 sudo apt install jenkins
#to check jenkins --version
 jenkins --version
  java --version
  python3 --version
  jenkins --version
  clear
  history
  exit

#after this is i uploaded alll the files to my repository link:https://github.com/sudhansu958/terrafform.git

git hub link:https://github.com/sudhansu958/terrafform.git

# terraform
# terraform
