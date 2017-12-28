# Amazon EC2 Instance SsmAssociations AssociationParameters<a name="aws-properties-ec2-instance-ssmassociations-associationparameters"></a>

`AssociationParameters` is a property of the [Amazon EC2 Instance SsmAssociations](aws-properties-ec2-instance-ssmassociations.md) property that specifies input parameter values for an Amazon EC2 Systems Manager \(SSM\) document\.

## Syntax<a name="w3ab2c21c14d567b5"></a>

### JSON<a name="aws-properties-ec2-instance-ssmassociations-associationparameters-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-instance-ssmassociations-associationparameters-key)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-instance-ssmassociations-associationparameters-value)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-ec2-instance-ssmassociations-associationparameters-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-instance-ssmassociations-associationparameters-key): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-instance-ssmassociations-associationparameters-value):
  - String
```

## Properties<a name="w3ab2c21c14d567b7"></a>

`Key`  
The name of an input parameter that is in the associated SSM document\.  
*Required: *Yes  
*Type*: String

`Value`  
The value of an input parameter\.  
*Required: *Yes  
*Type*: List of String values