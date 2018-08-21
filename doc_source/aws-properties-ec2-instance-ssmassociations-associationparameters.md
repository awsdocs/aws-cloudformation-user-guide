# Amazon EC2 Instance SsmAssociations AssociationParameters<a name="aws-properties-ec2-instance-ssmassociations-associationparameters"></a>

`AssociationParameters` is a property of the [Amazon EC2 Instance SsmAssociations](aws-properties-ec2-instance-ssmassociations.md) property that specifies input parameter values for an SSM document in AWS Systems Manager\.

## Syntax<a name="w3ab2c21c14d665b5"></a>

### JSON<a name="aws-properties-ec2-instance-ssmassociations-associationparameters-syntax.json"></a>

```
{
  "[Key](#cfn-ec2-instance-ssmassociations-associationparameters-key)" : String,
  "[Value](#cfn-ec2-instance-ssmassociations-associationparameters-value)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-ec2-instance-ssmassociations-associationparameters-syntax.yaml"></a>

```
[Key](#cfn-ec2-instance-ssmassociations-associationparameters-key): String
[Value](#cfn-ec2-instance-ssmassociations-associationparameters-value):
  - String
```

## Properties<a name="w3ab2c21c14d665b7"></a>

`Key`  <a name="cfn-ec2-instance-ssmassociations-associationparameters-key"></a>
The name of an input parameter that is in the associated SSM document\.  
*Required*: Yes  
*Type*: String

`Value`  <a name="cfn-ec2-instance-ssmassociations-associationparameters-value"></a>
The value of an input parameter\.  
*Required*: Yes  
*Type*: List of String values