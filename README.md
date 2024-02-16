# ansible
ansible all -i inventory -m ping
ansible-playbook -i inventory playbook.yml
sudo systemctl status nginx
# swap file
sudo fallocate -l 1G 1G.swap
stat 1G.swap
sudo chmod 600 1G.swap
sudo mkswap 1G.swap
sudo swapon 1G.swap
# copying to the fstab because we want the file for our next reboot
echo '/home/ec2-user/1G.swap swap swap defaults 0 0' | sudo tee -a /etc/fstab 
