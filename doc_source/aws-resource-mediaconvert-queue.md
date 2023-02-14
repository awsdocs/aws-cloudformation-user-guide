# AWS::MediaConvert::Queue<a name="aws-resource-mediaconvert-queue"></a>

The AWS::MediaConvert::Queue resource is an AWS Elemental MediaConvert resource type that you can use to manage the resources that are available to your account for parallel processing of jobs\. For more information about queues, see [Working with AWS Elemental MediaConvert Queues](https://docs.aws.amazon.com/mediaconvert/latest/ug/working-with-queues.html) in the *AWS Elemental MediaConvert User Guide*\.

## Syntax<a name="aws-resource-mediaconvert-queue-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-mediaconvert-queue-syntax.json"></a>

```
{
  "Type" : "AWS::MediaConvert::Queue",
  "Properties" : {
      "[Description](#cfn-mediaconvert-queue-description)" : String,
      "[Name](#cfn-mediaconvert-queue-name)" : String,
      "[PricingPlan](#cfn-mediaconvert-queue-pricingplan)" : String,
      "[Status](#cfn-mediaconvert-queue-status)" : String,
      "[Tags](#cfn-mediaconvert-queue-tags)" : Json
    }
}
```

### YAML<a name="aws-resource-mediaconvert-queue-syntax.yaml"></a>

```
Type: AWS::MediaConvert::Queue
Properties: 
  [Description](#cfn-mediaconvert-queue-description): String
  [Name](#cfn-mediaconvert-queue-name): String
  [PricingPlan](#cfn-mediaconvert-queue-pricingplan): String
  [Status](#cfn-mediaconvert-queue-status): String
  [Tags](#cfn-mediaconvert-queue-tags): Json
```

## Properties<a name="aws-resource-mediaconvert-queue-properties"></a>

`Description`  <a name="cfn-mediaconvert-queue-description"></a>
Optional\. A description of the queue that you are creating\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-mediaconvert-queue-name"></a>
The name of the queue that you are creating\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PricingPlan`  <a name="cfn-mediaconvert-queue-pricingplan"></a>
When you use AWS CloudFormation, you can create only on\-demand queues\. Therefore, always set `PricingPlan` to the value "ON\_DEMAND" when declaring an AWS::MediaConvert::Queue in your AWS CloudFormation template\.  
To create a reserved queue, use the AWS Elemental MediaConvert console at https://console\.aws\.amazon\.com/mediaconvert to set up a contract\. For more information, see [Working with AWS Elemental MediaConvert Queues](https://docs.aws.amazon.com/mediaconvert/latest/ug/working-with-queues.html) in the *AWS Elemental MediaConvert User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Status`  <a name="cfn-mediaconvert-queue-status"></a>
Initial state of the queue\. Queues can be either ACTIVE or PAUSED\. If you create a paused queue, then jobs that you send to that queue won't begin\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-mediaconvert-queue-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-mediaconvert-queue-return-values"></a>

### Ref<a name="aws-resource-mediaconvert-queue-return-values-ref"></a>

When you pass the logical ID of an `AWS::MediaConvert::Queue` resource to the intrinsic `Ref` function, the function returns the name of the queue, such as `Queue 2`\. 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-mediaconvert-queue-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-mediaconvert-queue-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the queue, such as `arn:aws:mediaconvert:us-west-2:123456789012`\.

`Name`  <a name="Name-fn::getatt"></a>
The name of the queue, such as `Queue 2`\.