# AWS::ResilienceHub::App PhysicalResourceId<a name="aws-properties-resiliencehub-app-physicalresourceid"></a>

Defines a physical resource identifier\.

## Syntax<a name="aws-properties-resiliencehub-app-physicalresourceid-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-resiliencehub-app-physicalresourceid-syntax.json"></a>

```
{
  "[AwsAccountId](#cfn-resiliencehub-app-physicalresourceid-awsaccountid)" : String,
  "[AwsRegion](#cfn-resiliencehub-app-physicalresourceid-awsregion)" : String,
  "[Identifier](#cfn-resiliencehub-app-physicalresourceid-identifier)" : String,
  "[Type](#cfn-resiliencehub-app-physicalresourceid-type)" : String
}
```

### YAML<a name="aws-properties-resiliencehub-app-physicalresourceid-syntax.yaml"></a>

```
  [AwsAccountId](#cfn-resiliencehub-app-physicalresourceid-awsaccountid): String
  [AwsRegion](#cfn-resiliencehub-app-physicalresourceid-awsregion): String
  [Identifier](#cfn-resiliencehub-app-physicalresourceid-identifier): String
  [Type](#cfn-resiliencehub-app-physicalresourceid-type): String
```

## Properties<a name="aws-properties-resiliencehub-app-physicalresourceid-properties"></a>

`AwsAccountId`  <a name="cfn-resiliencehub-app-physicalresourceid-awsaccountid"></a>
The AWS account that owns the physical resource\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AwsRegion`  <a name="cfn-resiliencehub-app-physicalresourceid-awsregion"></a>
The AWS Region that the physical resource is located in\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Identifier`  <a name="cfn-resiliencehub-app-physicalresourceid-identifier"></a>
The identifier of the physical resource\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-resiliencehub-app-physicalresourceid-type"></a>
Specifies the type of physical resource identifier\.    
Arn  
The resource identifier is an Amazon Resource Name \(ARN\) \.  
Native  
The resource identifier is an AWS Resilience Hub\-native identifier\.
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)