# AWS::EC2::VPCEndpointConnectionNotification<a name="aws-resource-ec2-vpcendpointconnectionnotification"></a>

Creates a connection notification for the specified VPC endpoint or VPC endpoint service\. A connection notification notifies you of specific endpoint events\. You must create an SNS topic to receive notifications\. For more information, see [CreateVpcEndpointConnectionNotification](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateVpcEndpointConnectionNotification.html)\.

**Topics**
+ [Syntax](#aws-resource-ec2-vpcendpointconnectionnotification-syntax)
+ [Properties](#aws-resource-ec2-vpcendpointconnectionnotification-properties)
+ [Return Values](#aws-resource-ec2-vpcendpointconnectionnotification-returnvalues)

## Syntax<a name="aws-resource-ec2-vpcendpointconnectionnotification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-vpcendpointconnectionnotification-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::VPCEndpointConnectionNotification",
  "Properties" : {
    "[ConnectionEvents](#cfn-ec2-vpcendpointconnectionnotification-connectionevents)" : [ String, ... ],
    "[VPCEndpointId](#cfn-ec2-vpcendpointconnectionnotification-vpcendpointid)" : String,
    "[ServiceId](#cfn-ec2-vpcendpointconnectionnotification-serviceid)" : String,
    "[ConnectionNotificationArn](#cfn-ec2-vpcendpointconnectionnotification-connectionnotificationarn)" : String
  }
}
```

### YAML<a name="aws-resource-ec2-vpcendpointconnectionnotification-syntax.yaml"></a>

```
Type: "AWS::EC2::VPCEndpointConnectionNotification"
Properties:
  [ConnectionEvents](#cfn-ec2-vpcendpointconnectionnotification-connectionevents): 
    - String
  [VPCEndpointId](#cfn-ec2-vpcendpointconnectionnotification-vpcendpointid): String
  [ServiceId](#cfn-ec2-vpcendpointconnectionnotification-serviceid): String
  [ConnectionNotificationArn](#cfn-ec2-vpcendpointconnectionnotification-connectionnotificationarn): String
```

## Properties<a name="aws-resource-ec2-vpcendpointconnectionnotification-properties"></a>

`ConnectionEvents`  <a name="cfn-ec2-vpcendpointconnectionnotification-connectionevents"></a>
One or more endpoint events for which to receive notifications\. Valid values are `Accept`, `Connect`, `Delete`, and `Reject`\.  
 *Required*: Yes  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ConnectionNotificationArn`  <a name="cfn-ec2-vpcendpointconnectionnotification-connectionnotificationarn"></a>
The ARN of the SNS topic for the notifications\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ServiceId`  <a name="cfn-ec2-vpcendpointconnectionnotification-serviceid"></a>
The ID of the endpoint service\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`VPCEndpointId`  <a name="cfn-ec2-vpcendpointconnectionnotification-vpcendpointid"></a>
The ID of the endpoint\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-ec2-vpcendpointconnectionnotification-returnvalues"></a>

### Ref<a name="aws-resource-ec2-vpcendpointconnectionnotification-ref"></a>

When you pass the logical ID of an `AWS::EC2::VPCEndpointConnectionNotification` resource to the intrinsic `Ref` function, the function returns the ID of the connection notification\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 