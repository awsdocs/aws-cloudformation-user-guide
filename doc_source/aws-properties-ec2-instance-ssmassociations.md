# Amazon EC2 Instance SsmAssociations<a name="aws-properties-ec2-instance-ssmassociations"></a>

`SsmAssociations` is a property of the [AWS::EC2::Instance](aws-properties-ec2-instance.md) resource that specifies the Amazon EC2 Systems Manager \(SSM\) document and parameter values to associate with an instance\.

## Syntax<a name="w3ab2c21c14d563b5"></a>

### JSON<a name="aws-properties-ec2-instance-ssmassociations-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-instance-ssmassociations-associationparameters)" : [ Parameters, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-instance-ssmassociations-documentname)" : String
}
```

### YAML<a name="aws-properties-ec2-instance-ssmassociations-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-instance-ssmassociations-associationparameters):
  - Parameters
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-instance-ssmassociations-documentname): String
```

## Properties<a name="w3ab2c21c14d563b7"></a>

`AssociationParameters`  
The input parameter values to use with the associated SSM document\.  
*Required: *No  
*Type*: List of [Amazon EC2 Instance SsmAssociations AssociationParameters](aws-properties-ec2-instance-ssmassociations-associationparameters.md)

`DocumentName`  
The name of an SSM document to associate with the instance\.  
*Required: *Yes  
*Type*: String