# AWS::EC2::ClientVpnEndpoint ClientConnectOptions<a name="aws-properties-ec2-clientvpnendpoint-clientconnectoptions"></a>

Indicates whether client connect options are enabled\. The default is `false` \(not enabled\)\.

## Syntax<a name="aws-properties-ec2-clientvpnendpoint-clientconnectoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-clientvpnendpoint-clientconnectoptions-syntax.json"></a>

```
{
  "[Enabled](#cfn-ec2-clientvpnendpoint-clientconnectoptions-enabled)" : Boolean,
  "[LambdaFunctionArn](#cfn-ec2-clientvpnendpoint-clientconnectoptions-lambdafunctionarn)" : String
}
```

### YAML<a name="aws-properties-ec2-clientvpnendpoint-clientconnectoptions-syntax.yaml"></a>

```
  [Enabled](#cfn-ec2-clientvpnendpoint-clientconnectoptions-enabled): Boolean
  [LambdaFunctionArn](#cfn-ec2-clientvpnendpoint-clientconnectoptions-lambdafunctionarn): String
```

## Properties<a name="aws-properties-ec2-clientvpnendpoint-clientconnectoptions-properties"></a>

`Enabled`  <a name="cfn-ec2-clientvpnendpoint-clientconnectoptions-enabled"></a>
Indicates whether client connect options are enabled\. The default is `false` \(not enabled\)\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LambdaFunctionArn`  <a name="cfn-ec2-clientvpnendpoint-clientconnectoptions-lambdafunctionarn"></a>
The Amazon Resource Name \(ARN\) of the AWS Lambda function used for connection authorization\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)