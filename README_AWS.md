Creating an EC2 Instance - `AWS`
-

- Log into AWS and make sure that proper region is selected `Ireland`.
- Find EC2.
- Select `Instances`.
- Click `Launch Instance`.
- Type `name` of your new Instance.
- Now you need to find OS `Ubuntu Server 20.04 LTS (HVM), SSD Volume Type`.
- In `Instance type` choose the size of an instance.
- Add `Key pair` for example `tech221`.
- In `Network settings` choose `Allow SSH traffic from` `My IP`
  and `Allow HTTP traffic from the internet`.
- Click `Edit` in `Network settings` to change a name of our
  `Security group name` and `Description`, also we need to make sure that `Auto-assign public IP` is `Enabled`.
- Select how many instances you want to choose.
- Click `Launch instance`.
- If everything works check your instance box and click `Connect` and head to SSH client.
- Open GitBash and head to the `.ssh` directory with command `cd .ssh`.
- Enter command `chmod 400 tech221.pem` which is visible on the top of your SSH client in new instance.
- Next copy the bottom command into the GitBash.
- For the first time we might need to type `yes` after pasting the command into GitBash.
