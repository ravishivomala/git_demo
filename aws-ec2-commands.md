1. Open WSL
       ↓
2. aws login --remote
       ↓
3. aws sts get-caller-identity
       ↓
4. Check EC2
   aws ec2 describe-instances ...
       ↓
5. Get Public IP
       ↓
6. SSH
   ssh -i ~/ken0705.pem ec2-user@<PUBLIC-IP>
       ↓
7. Work inside EC2
       ↓
8. exit



# AWS EC2 Commands

## AWS Login

```bash
aws login --remote
```

## Check AWS Identity

```bash
aws sts get-caller-identity
```

## List EC2 Instances

```bash
aws ec2 describe-instances
```

## Show Instance ID, State and Public IP

```bash
aws ec2 describe-instances \
--query "Reservations[*].Instances[*].[InstanceId,State.Name,PublicIpAddress]" \
--output table
```

## SSH into EC2

```bash
ssh -i ~/KEY_FILE.pem ec2-user@YOUR_PUBLIC_IP
```

## Check Current User

```bash
whoami
```

## Check Current Directory

```bash
pwd
```

## Check Hostname

```bash
hostname
```

## List Files

```bash
ls -l
```

## Go to DevOps Directory

```bash
cd ~/devops
```

## Display File Content

```bash
cat text.txt
```

## Exit EC2

```bash
exit

