# AWS::AutoScaling::LaunchConfiguration MetadataOptions<a name="aws-properties-autoscaling-launchconfiguration-metadataoptions"></a>

 `MetadataOptions` is a property of [AWS::AutoScaling::LaunchConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-launchconfig.html) that describes metadata options for the instances\.

For more information, see [Configure the instance metadata options](https://docs.aws.amazon.com/autoscaling/ec2/userguide/create-launch-config.html#launch-configurations-imds) in the *Amazon EC2 Auto Scaling User Guide*\.

## Syntax<a name="aws-properties-autoscaling-launchconfiguration-metadataoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscaling-launchconfiguration-metadataoptions-syntax.json"></a>

```
{
  "[HttpEndpoint](#cfn-autoscaling-launchconfiguration-metadataoptions-httpendpoint)" : String,
  "[HttpPutResponseHopLimit](#cfn-autoscaling-launchconfiguration-metadataoptions-httpputresponsehoplimit)" : Integer,
  "[HttpTokens](#cfn-autoscaling-launchconfiguration-metadataoptions-httptokens)" : String
}
```

### YAML<a name="aws-properties-autoscaling-launchconfiguration-metadataoptions-syntax.yaml"></a>

```
  [HttpEndpoint](#cfn-autoscaling-launchconfiguration-metadataoptions-httpendpoint): String
  [HttpPutResponseHopLimit](#cfn-autoscaling-launchconfiguration-metadataoptions-httpputresponsehoplimit): Integer
  [HttpTokens](#cfn-autoscaling-launchconfiguration-metadataoptions-httptokens): String
```

## Properties<a name="aws-properties-autoscaling-launchconfiguration-metadataoptions-properties"></a>

`HttpEndpoint`  <a name="cfn-autoscaling-launchconfiguration-metadataoptions-httpendpoint"></a>
This parameter enables or disables the HTTP metadata endpoint on your instances\. If the parameter is not specified, the default state is `enabled`\.  
If you specify a value of `disabled`, you will not be able to access your instance metadata\. 
*Required*: No  
*Type*: String  
*Allowed values*: `disabled | enabled`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`HttpPutResponseHopLimit`  <a name="cfn-autoscaling-launchconfiguration-metadataoptions-httpputresponsehoplimit"></a>
The desired HTTP PUT response hop limit for instance metadata requests\. The larger the number, the further instance metadata requests can travel\.  
Default: 1  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `64`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`HttpTokens`  <a name="cfn-autoscaling-launchconfiguration-metadataoptions-httptokens"></a>
The state of token usage for your instance metadata requests\. If the parameter is not specified in the request, the default state is `optional`\.  
If the state is `optional`, you can choose to retrieve instance metadata with or without a signed token header on your request\. If you retrieve the IAM role credentials without a token, the version 1\.0 role credentials are returned\. If you retrieve the IAM role credentials using a valid signed token, the version 2\.0 role credentials are returned\.  
If the state is `required`, you must send a signed token header with any instance metadata retrieval requests\. In this state, retrieving the IAM role credentials always returns the version 2\.0 credentials; the version 1\.0 credentials are not available\.  
*Required*: No  
*Type*: String  
*Allowed values*: `optional | required`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)