# AWS::EC2::Instance AssociationParameter<a name="aws-properties-ec2-instance-ssmassociations-associationparameters"></a>

Specifies input parameter values for an SSM document in AWS Systems Manager\.

 `AssociationParameter` is a property of the [ Amazon EC2 Instance SsmAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance-ssmassociations.html) property\.

## Syntax<a name="aws-properties-ec2-instance-ssmassociations-associationparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

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

## Properties<a name="aws-properties-ec2-instance-ssmassociations-associationparameters-properties"></a>

`Key`  <a name="cfn-ec2-instance-ssmassociations-associationparameters-key"></a>
The name of an input parameter that is in the associated SSM document\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-ec2-instance-ssmassociations-associationparameters-value"></a>
The value of an input parameter\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)