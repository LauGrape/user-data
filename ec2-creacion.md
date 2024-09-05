aws --region us-east-1 \
  ec2 run-instances \
  --image-id ami-222222222222 \
  --count 1 \
  --instance-type t3a.small \
  --key-name prueba \
  --security-group-ids sg-22222222222222222 \
  --subnet-id subnet-2222222 \2
  --user-data file://user-data2.txt \
  --tag-specifications 'ResourceType=instance,Tags=[{Key=Name,Value=ec2}]'