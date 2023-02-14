# AWS::EC2::LaunchTemplate MetadataOptions<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-metadataoptions"></a>

The metadata options for the instance\. For more information, see [Instance metadata and user data](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-instance-metadata.html) in the *Amazon EC2 User Guide*\.

`MetadataOptions` is a property of [AWS::EC2::LaunchTemplate LaunchTemplateData](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-launchtemplate-launchtemplatedata.html)\.

## Syntax<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-metadataoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-metadataoptions-syntax.json"></a>

```
{
  "[HttpEndpoint](#cfn-ec2-launchtemplate-launchtemplatedata-metadataoptions-httpendpoint)" : String,
  "[HttpProtocolIpv6](#cfn-ec2-launchtemplate-launchtemplatedata-metadataoptions-httpprotocolipv6)" : String,
  "[HttpPutResponseHopLimit](#cfn-ec2-launchtemplate-launchtemplatedata-metadataoptions-httpputresponsehoplimit)" : Integer,
  "[HttpTokens](#cfn-ec2-launchtemplate-launchtemplatedata-metadataoptions-httptokens)" : String,
  "[InstanceMetadataTags](#cfn-ec2-launchtemplate-launchtemplatedata-metadataoptions-instancemetadatatags)" : String
}
```

### YAML<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-metadataoptions-syntax.yaml"></a>

```
  [HttpEndpoint](#cfn-ec2-launchtemplate-launchtemplatedata-metadataoptions-httpendpoint): String
  [HttpProtocolIpv6](#cfn-ec2-launchtemplate-launchtemplatedata-metadataoptions-httpprotocolipv6): String
  [HttpPutResponseHopLimit](#cfn-ec2-launchtemplate-launchtemplatedata-metadataoptions-httpputresponsehoplimit): Integer
  [HttpTokens](#cfn-ec2-launchtemplate-launchtemplatedata-metadataoptions-httptokens): String
  [InstanceMetadataTags](#cfn-ec2-launchtemplate-launchtemplatedata-metadataoptions-instancemetadatatags): String
```

## Properties<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-metadataoptions-properties"></a>

`HttpEndpoint`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-metadataoptions-httpendpoint"></a>
Enables or disables the HTTP metadata endpoint on your instances\. If the parameter is not specified, the default state is `enabled`\.  
If you specify a value of `disabled`, you will not be able to access your instance metadata\. 
*Required*: No  
*Type*: String  
*Allowed values*: `disabled | enabled`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HttpProtocolIpv6`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-metadataoptions-httpprotocolipv6"></a>
Enables or disables the IPv6 endpoint for the instance metadata service\.  
Default: `disabled`   
*Required*: No  
*Type*: String  
*Allowed values*: `disabled | enabled`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HttpPutResponseHopLimit`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-metadataoptions-httpputresponsehoplimit"></a>
The desired HTTP PUT response hop limit for instance metadata requests\. The larger the number, the further instance metadata requests can travel\.  
Default: `1`   
Possible values: Integers from 1 to 64  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HttpTokens`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-metadataoptions-httptokens"></a>
IMDSv2 uses token\-backed sessions\. Set the use of HTTP tokens to `optional` \(in other words, set the use of IMDSv2 to `optional`\) or `required` \(in other words, set the use of IMDSv2 to `required`\)\.  
+  `optional` \- When IMDSv2 is optional, you can choose to retrieve instance metadata with or without a session token in your request\. If you retrieve the IAM role credentials without a token, the IMDSv1 role credentials are returned\. If you retrieve the IAM role credentials using a valid session token, the IMDSv2 role credentials are returned\.
+  `required` \- When IMDSv2 is required, you must send a session token with any instance metadata retrieval requests\. In this state, retrieving the IAM role credentials always returns IMDSv2 credentials; IMDSv1 credentials are not available\.
Default: `optional`   
*Required*: No  
*Type*: String  
*Allowed values*: `optional | required`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceMetadataTags`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-metadataoptions-instancemetadatatags"></a>
Set to `enabled` to allow access to instance tags from the instance metadata\. Set to `disabled` to turn off access to instance tags from the instance metadata\. For more information, see [Work with instance tags using the instance metadata](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/Using_Tags.html#work-with-tags-in-IMDS)\.  
Default: `disabled`   
*Required*: No  
*Type*: String  
*Allowed values*: `disabled | enabled`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)