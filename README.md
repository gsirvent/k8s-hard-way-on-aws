# k8s-hard-way-on-aws


## AWS deploy CF template for controllers and workers

```
aws cloudformation create-stack \
  --stack-name $NAME \
  --template-body file://k8s_hard_way.yaml \
  --parameters \
    ParameterKey=SubnetAZ1,ParameterValue=$AZ1 \
    ParameterKey=SubnetAZ2,ParameterValue=$AZ2 \
    ParameterKey=SubnetAZ3,ParameterValue=$AZ3 \
    ParameterKey=KeyName,ParameterValue=$KN \
  --profile $PRFL
```
