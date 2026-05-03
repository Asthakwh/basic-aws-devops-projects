# EC2-ALB-vs-S3-Static-Website-Hosting
# Compute-based hosting (EC2 + ALB) 

create security group for access ssh and http
create 2 ec2 instance
attach sg to it and launch it

sudo apt update && sudo apt install -y nginx
echo "<h1>Hello from this server</h1>" | sudo tee /var/www/html/index.html
sudo systemctl enable nginx
sudo systemctl start nginx
http://<IP> # check on browser

create Target group -> attach both instance to it and create
load balancer-> create add target group -> VPC -> SG -> and 2 zones -> and create

now copy the DNS name from load balancer
and paste on browser 'http://<id> ###it will show that page running on nginx html code you entered.

Finally we hosted on ec2


# Storage-based hosting (S3 static website)


create s3 -> upload object -> turn off block public access(means allow access) -> enable static hosting paste script given below( change arn with your bucket arn)

apply 

paste bucket website endpoint in browser with http://<url>
and access you html page
