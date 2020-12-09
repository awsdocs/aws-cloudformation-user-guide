# AWS::EC2::VPCEndpointConnectionNotification<a name="aws-resource-ec2-vpcendpointconnectionnotification"></a>

Specifies a connection notification for a VPC endpoint or VPC endpoint service\. A connection notification notifies you of specific endpoint events\. You must create an SNS topic to receive notifications\. For more information, see [Create a Topic](https://docs.aws.amazon.com/sns/latest/dg/CreateTopic.html) in the *Amazon Simple Notification Service Developer Guide*\.

You can create a connection notification for interface endpoints only\.

## Syntax<a name="aws-resource-ec2-vpcendpointconnectionnotification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-vpcendpointconnectionnotification-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::VPCEndpointConnectionNotification",
  "Properties" : {
      "[ConnectionEvents](#cfn-ec2-vpcendpointconnectionnotification-connectionevents)" : [ String, ... ],
      "[ConnectionNotificationArn](#cfn-ec2-vpcendpointconnectionnotification-connectionnotificationarn)" : String,
      "[ServiceId](#cfn-ec2-vpcendpointconnectionnotification-serviceid)" : String,
      "[VPCEndpointId](#cfn-ec2-vpcendpointconnectionnotification-vpcendpointid)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-vpcendpointconnectionnotification-syntax.yaml"></a>

```
Type: AWS::EC2::VPCEndpointConnectionNotification
Properties: 
  [ConnectionEvents](#cfn-ec2-vpcendpointconnectionnotification-connectionevents): 
    - String
  [ConnectionNotificationArn](#cfn-ec2-vpcendpointconnectionnotification-connectionnotificationarn): String
  [ServiceId](#cfn-ec2-vpcendpointconnectionnotification-serviceid): String
  [VPCEndpointId](#cfn-ec2-vpcendpointconnectionnotification-vpcendpointid): String
```

## Properties<a name="aws-resource-ec2-vpcendpointconnectionnotification-properties"></a>

`ConnectionEvents`  <a name="cfn-ec2-vpcendpointconnectionnotification-connectionevents"></a>
One or more endpoint events for which to receive notifications\. Valid values are `Accept`, `Connect`, `Delete`, and `Reject`\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConnectionNotificationArn`  <a name="cfn-ec2-vpcendpointconnectionnotification-connectionnotificationarn"></a>
The ARN of the SNS topic for the notifications\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceId`  <a name="cfn-ec2-vpcendpointconnectionnotification-serviceid"></a>
The ID of the endpoint service\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VPCEndpointId`  <a name="cfn-ec2-vpcendpointconnectionnotification-vpcendpointid"></a>
The ID of the endpoint\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ec2-vpcendpointconnectionnotification-return-values"></a>

### Ref<a name="aws-resource-ec2-vpcendpointconnectionnotification-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the VPC endpoint connection\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.