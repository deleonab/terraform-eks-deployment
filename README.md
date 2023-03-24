### create keypair through AWS CLI and chmod 400
```
NAME=eks-terraform-key
aws ec2 create-key-pair \
  --key-name ${NAME} \
  --output text --query 'KeyMaterial' \
  > private-key/${NAME}.id_rsa
chmod 400 private-key/${NAME}.id_rsa
```