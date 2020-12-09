# AWS::EC2::LaunchTemplate MetadataOptions<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-metadataoptions"></a>

Specifies the metadata options for the instance\.

`MetadataOptions` is a property of [AWS::EC2::LaunchTemplate LaunchTemplateData](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-launchtemplate-launchtemplatedata.html)\.

## Syntax<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-metadataoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-metadataoptions-syntax.json"></a>

```
{
  "[HttpEndpoint](#cfn-ec2-launchtemplate-launchtemplatedata-metadataoptions-httpendpoint)" : String,
  "[HttpPutResponseHopLimit](#cfn-ec2-launchtemplate-launchtemplatedata-metadataoptions-httpputresponsehoplimit)" : Integer,
  "[HttpTokens](#cfn-ec2-launchtemplate-launchtemplatedata-metadataoptions-httptokens)" : String
}
```

### YAML<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-metadataoptions-syntax.yaml"></a>

```
  [HttpEndpoint](#cfn-ec2-launchtemplate-launchtemplatedata-metadataoptions-httpendpoint): String
  [HttpPutResponseHopLimit](#cfn-ec2-launchtemplate-launchtemplatedata-metadataoptions-httpputresponsehoplimit): Integer
  [HttpTokens](#cfn-ec2-launchtemplate-launchtemplatedata-metadataoptions-httptokens): String
```

## Properties<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-metadataoptions-properties"></a>

`HttpEndpoint`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-metadataoptions-httpendpoint"></a>
This parameter enables or disables the HTTP metadata endpoint on your instances\. If the parameter is not specified, the default state is `enabled`\.  
If you specify a value of `disabled`, you will not be able to access your instance metadata\. 
*Required*: No  
*Type*: String  
*Allowed values*: `disabled | enabled`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HttpPutResponseHopLimit`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-metadataoptions-httpputresponsehoplimit"></a>
The desired HTTP PUT response hop limit for instance metadata requests\. The larger the number, the further instance metadata requests can travel\.  
Default: 1  
Possible values: Integers from 1 to 64  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HttpTokens`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-metadataoptions-httptokens"></a>
The state of token usage for your instance metadata requests\. If the parameter is not specified in the request, the default state is `optional`\.  
If the state is `optional`, you can choose to retrieve instance metadata with or without a signed token header on your request\. If you retrieve the IAM role credentials without a token, the version 1\.0 role credentials are returned\. If you retrieve the IAM role credentials using a valid signed token, the version 2\.0 role credentials are returned\.  
If the state is `required`, you must send a signed token header with any instance metadata retrieval requests\. In this state, retrieving the IAM role credentials always returns the version 2\.0 credentials; the version 1\.0 credentials are not available\.  
*Required*: No  
*Type*: String  
*Allowed values*: `optional | required`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)