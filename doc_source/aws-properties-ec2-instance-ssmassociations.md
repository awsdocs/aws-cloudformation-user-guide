# Amazon EC2 Instance SsmAssociations<a name="aws-properties-ec2-instance-ssmassociations"></a>

`SsmAssociations` is a property of the [AWS::EC2::Instance](aws-properties-ec2-instance.md) resource that specifies the SSM document and parameter values in AWS Systems Manager to associate with an instance\.

## Syntax<a name="w3ab2c21c14d670b5"></a>

### JSON<a name="aws-properties-ec2-instance-ssmassociations-syntax.json"></a>

```
{
  "[AssociationParameters](#cfn-ec2-instance-ssmassociations-associationparameters)" : [ Parameters, ... ],
  "[DocumentName](#cfn-ec2-instance-ssmassociations-documentname)" : String
}
```

### YAML<a name="aws-properties-ec2-instance-ssmassociations-syntax.yaml"></a>

```
[AssociationParameters](#cfn-ec2-instance-ssmassociations-associationparameters):
  - Parameters
[DocumentName](#cfn-ec2-instance-ssmassociations-documentname): String
```

## Properties<a name="w3ab2c21c14d670b7"></a>

`AssociationParameters`  <a name="cfn-ec2-instance-ssmassociations-associationparameters"></a>
The input parameter values to use with the associated SSM document\.  
*Required*: No  
*Type*: List of [Amazon EC2 Instance SsmAssociations AssociationParameters](aws-properties-ec2-instance-ssmassociations-associationparameters.md)

`DocumentName`  <a name="cfn-ec2-instance-ssmassociations-documentname"></a>
The name of an SSM document to associate with the instance\.  
*Required*: Yes  
*Type*: String