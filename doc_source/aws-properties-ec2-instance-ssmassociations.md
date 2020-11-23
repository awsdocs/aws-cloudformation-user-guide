# AWS::EC2::Instance SsmAssociation<a name="aws-properties-ec2-instance-ssmassociations"></a>

Specifies the SSM document and parameter values in AWS Systems Manager to associate with an instance\.

 `SsmAssociations` is a property of the [AWS::EC2::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html) resource\. 

## Syntax<a name="aws-properties-ec2-instance-ssmassociations-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-instance-ssmassociations-syntax.json"></a>

```
{
  "[AssociationParameters](#cfn-ec2-instance-ssmassociations-associationparameters)" : [ AssociationParameter, ... ],
  "[DocumentName](#cfn-ec2-instance-ssmassociations-documentname)" : String
}
```

### YAML<a name="aws-properties-ec2-instance-ssmassociations-syntax.yaml"></a>

```
  [AssociationParameters](#cfn-ec2-instance-ssmassociations-associationparameters): 
    - AssociationParameter
  [DocumentName](#cfn-ec2-instance-ssmassociations-documentname): String
```

## Properties<a name="aws-properties-ec2-instance-ssmassociations-properties"></a>

`AssociationParameters`  <a name="cfn-ec2-instance-ssmassociations-associationparameters"></a>
The input parameter values to use with the associated SSM document\.  
*Required*: No  
*Type*: List of [AssociationParameter](aws-properties-ec2-instance-ssmassociations-associationparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DocumentName`  <a name="cfn-ec2-instance-ssmassociations-documentname"></a>
The name of an SSM document to associate with the instance\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)