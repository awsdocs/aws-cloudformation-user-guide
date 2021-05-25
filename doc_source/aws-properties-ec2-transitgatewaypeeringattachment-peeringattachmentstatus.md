# AWS::EC2::TransitGatewayPeeringAttachment PeeringAttachmentStatus<a name="aws-properties-ec2-transitgatewaypeeringattachment-peeringattachmentstatus"></a>

The status of the transit gateway peering attachment\.

## Syntax<a name="aws-properties-ec2-transitgatewaypeeringattachment-peeringattachmentstatus-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-transitgatewaypeeringattachment-peeringattachmentstatus-syntax.json"></a>

```
{
  "[Code](#cfn-ec2-transitgatewaypeeringattachment-peeringattachmentstatus-code)" : String,
  "[Message](#cfn-ec2-transitgatewaypeeringattachment-peeringattachmentstatus-message)" : String
}
```

### YAML<a name="aws-properties-ec2-transitgatewaypeeringattachment-peeringattachmentstatus-syntax.yaml"></a>

```
  [Code](#cfn-ec2-transitgatewaypeeringattachment-peeringattachmentstatus-code): String
  [Message](#cfn-ec2-transitgatewaypeeringattachment-peeringattachmentstatus-message): String
```

## Properties<a name="aws-properties-ec2-transitgatewaypeeringattachment-peeringattachmentstatus-properties"></a>

`Code`  <a name="cfn-ec2-transitgatewaypeeringattachment-peeringattachmentstatus-code"></a>
The status code\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Message`  <a name="cfn-ec2-transitgatewaypeeringattachment-peeringattachmentstatus-message"></a>
The status message, if applicable\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)