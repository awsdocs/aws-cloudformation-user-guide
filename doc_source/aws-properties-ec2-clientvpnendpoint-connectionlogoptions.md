# AWS::EC2::ClientVpnEndpoint ConnectionLogOptions<a name="aws-properties-ec2-clientvpnendpoint-connectionlogoptions"></a>

Describes the client connection logging options for the Client VPN endpoint\.

## Syntax<a name="aws-properties-ec2-clientvpnendpoint-connectionlogoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-clientvpnendpoint-connectionlogoptions-syntax.json"></a>

```
{
  "[CloudwatchLogGroup](#cfn-ec2-clientvpnendpoint-connectionlogoptions-cloudwatchloggroup)" : String,
  "[CloudwatchLogStream](#cfn-ec2-clientvpnendpoint-connectionlogoptions-cloudwatchlogstream)" : String,
  "[Enabled](#cfn-ec2-clientvpnendpoint-connectionlogoptions-enabled)" : Boolean
}
```

### YAML<a name="aws-properties-ec2-clientvpnendpoint-connectionlogoptions-syntax.yaml"></a>

```
  [CloudwatchLogGroup](#cfn-ec2-clientvpnendpoint-connectionlogoptions-cloudwatchloggroup): String
  [CloudwatchLogStream](#cfn-ec2-clientvpnendpoint-connectionlogoptions-cloudwatchlogstream): String
  [Enabled](#cfn-ec2-clientvpnendpoint-connectionlogoptions-enabled): Boolean
```

## Properties<a name="aws-properties-ec2-clientvpnendpoint-connectionlogoptions-properties"></a>

`CloudwatchLogGroup`  <a name="cfn-ec2-clientvpnendpoint-connectionlogoptions-cloudwatchloggroup"></a>
The name of the CloudWatch Logs log group\. Required if connection logging is enabled\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CloudwatchLogStream`  <a name="cfn-ec2-clientvpnendpoint-connectionlogoptions-cloudwatchlogstream"></a>
The name of the CloudWatch Logs log stream to which the connection data is published\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enabled`  <a name="cfn-ec2-clientvpnendpoint-connectionlogoptions-enabled"></a>
Indicates whether connection logging is enabled\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)