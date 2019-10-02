# AWS::SageMaker::Workteam<a name="aws-resource-sagemaker-workteam"></a>

Creates a new work team for labeling your data\. A work team is defined by one or more Amazon Cognito user pools\. You must first create the user pools before you can create a work team\.

You cannot create more than 25 work teams in an account and region\.

## Syntax<a name="aws-resource-sagemaker-workteam-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-sagemaker-workteam-syntax.json"></a>

```
{
  "Type" : "AWS::SageMaker::Workteam",
  "Properties" : {
      "[Description](#cfn-sagemaker-workteam-description)" : String,
      "[MemberDefinitions](#cfn-sagemaker-workteam-memberdefinitions)" : [ [MemberDefinition](aws-properties-sagemaker-workteam-memberdefinition.md), ... ],
      "[NotificationConfiguration](#cfn-sagemaker-workteam-notificationconfiguration)" : [NotificationConfiguration](aws-properties-sagemaker-workteam-notificationconfiguration.md),
      "[Tags](#cfn-sagemaker-workteam-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[WorkteamName](#cfn-sagemaker-workteam-workteamname)" : String
    }
}
```

### YAML<a name="aws-resource-sagemaker-workteam-syntax.yaml"></a>

```
Type: AWS::SageMaker::Workteam
Properties: 
  [Description](#cfn-sagemaker-workteam-description): String
  [MemberDefinitions](#cfn-sagemaker-workteam-memberdefinitions): 
    - [MemberDefinition](aws-properties-sagemaker-workteam-memberdefinition.md)
  [NotificationConfiguration](#cfn-sagemaker-workteam-notificationconfiguration): 
    [NotificationConfiguration](aws-properties-sagemaker-workteam-notificationconfiguration.md)
  [Tags](#cfn-sagemaker-workteam-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [WorkteamName](#cfn-sagemaker-workteam-workteamname): String
```

## Properties<a name="aws-resource-sagemaker-workteam-properties"></a>

`Description`  <a name="cfn-sagemaker-workteam-description"></a>
A description of the work team\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `200`  
*Pattern*: `.+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MemberDefinitions`  <a name="cfn-sagemaker-workteam-memberdefinitions"></a>
The Amazon Cognito user groups that make up the work team\.  
*Required*: No  
*Type*: List of [MemberDefinition](aws-properties-sagemaker-workteam-memberdefinition.md)  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NotificationConfiguration`  <a name="cfn-sagemaker-workteam-notificationconfiguration"></a>
Configures SNS notifications of available or expiring work items for work teams\.  
*Required*: No  
*Type*: [NotificationConfiguration](aws-properties-sagemaker-workteam-notificationconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-sagemaker-workteam-tags"></a>
A list of key\-value pairs to apply to this resource\.  
For more information, see [Resource Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html) and [Using Cost Allocation Tags](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/cost-alloc-tags.html#allocation-what) in the * AWS Billing and Cost Management User Guide*\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WorkteamName`  <a name="cfn-sagemaker-workteam-workteamname"></a>
The name of the work team\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `63`  
*Pattern*: `^[a-zA-Z0-9](-*[a-zA-Z0-9])*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return Values<a name="aws-resource-sagemaker-workteam-return-values"></a>

### Ref<a name="aws-resource-sagemaker-workteam-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns details about a labeling work team\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-sagemaker-workteam-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

#### <a name="aws-resource-sagemaker-workteam-return-values-fn--getatt-fn--getatt"></a>

`WorkteamName`  <a name="WorkteamName-fn::getatt"></a>
The name of the work team\.

## Supported Regions

This ResourceType is supported by the following regions:

- `ap-northeast-1`
- `ap-southeast-2`
- `eu-west-1`
- `us-east-1`
- `us-east-2`
- `us-west-2`
