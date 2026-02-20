# 1. AWS EC2

- Create instance, using 'launch instance'
- put details
- select 'key' (create new or use old, its like a password to your instance).


## Commands for deploying static site
```code

sudo apt update
sudo apt install nginx
nginx -v
git clone http://github.com/your_profile/repo_name.git

sudo cp -r ./repo_name/* /var/www/html
history

```

 ~now this site is deployed;

## Security Inbounds
  set http and https in inbound setting
  go to wizard for it.

# 2. Creating Image (AMI)
  We create images, when there is more load. So we can divert the traffic. (although for static sites, AWS Auto Scaling is used. For automatic creations, and also Kubernetes EKS)

  - right click on deployed instance
  - create new image.
  - launch new instance
  - edit the config for all access directly there
  - use the previous key, else create new
  - done


# 3. Creating Volume and attaching it

if more volume is needed, We use Elastic Block Storage (EBS).

- go to EBS, create volume
- select the configuration as per need;
- In Tags sections ~ Provide **key** as *'Name'* and then **Value** as *"Volume_name"*;
- create volume
- select the volume and then **Attach** it to needed instance;

After the use user can *detach* the volume.

# 4. AWS Auto Scaling and Load Balancer

 




# FAQ

## Ques 1:
  Can we connect "volume" and "Instance" of different availability zone?
## Ans 1:
  No, we can't. The Availability zone must be same.
  Think of it like pendrive and laptop, if both of them are present in different places then its impossible to connect them.

## Ques 2:
  Can we connect multiple Volume to one instance?
## Ans 2:
  Yes, we can connect multiple to one instance.

## Ques 3:
  
