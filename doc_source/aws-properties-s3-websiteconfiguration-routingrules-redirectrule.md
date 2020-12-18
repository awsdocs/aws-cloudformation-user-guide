# AWS::S3::Bucket RedirectRule<a name="aws-properties-s3-websiteconfiguration-routingrules-redirectrule"></a>

Specifies how requests are redirected\. In the event of an error, you can specify a different error code to return\.

## Syntax<a name="aws-properties-s3-websiteconfiguration-routingrules-redirectrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-websiteconfiguration-routingrules-redirectrule-syntax.json"></a>

```
{
  "[HostName](#cfn-s3-websiteconfiguration-redirectrule-hostname)" : String,
  "[HttpRedirectCode](#cfn-s3-websiteconfiguration-redirectrule-httpredirectcode)" : String,
  "[Protocol](#cfn-s3-websiteconfiguration-redirectrule-protocol)" : String,
  "[ReplaceKeyPrefixWith](#cfn-s3-websiteconfiguration-redirectrule-replacekeyprefixwith)" : String,
  "[ReplaceKeyWith](#cfn-s3-websiteconfiguration-redirectrule-replacekeywith)" : String
}
```

### YAML<a name="aws-properties-s3-websiteconfiguration-routingrules-redirectrule-syntax.yaml"></a>

```
  [HostName](#cfn-s3-websiteconfiguration-redirectrule-hostname): String
  [HttpRedirectCode](#cfn-s3-websiteconfiguration-redirectrule-httpredirectcode): String
  [Protocol](#cfn-s3-websiteconfiguration-redirectrule-protocol): String
  [ReplaceKeyPrefixWith](#cfn-s3-websiteconfiguration-redirectrule-replacekeyprefixwith): String
  [ReplaceKeyWith](#cfn-s3-websiteconfiguration-redirectrule-replacekeywith): String
```

## Properties<a name="aws-properties-s3-websiteconfiguration-routingrules-redirectrule-properties"></a>

`HostName`  <a name="cfn-s3-websiteconfiguration-redirectrule-hostname"></a>
The host name to use in the redirect request\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HttpRedirectCode`  <a name="cfn-s3-websiteconfiguration-redirectrule-httpredirectcode"></a>
The HTTP redirect code to use on the response\. Not required if one of the siblings is present\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Protocol`  <a name="cfn-s3-websiteconfiguration-redirectrule-protocol"></a>
Protocol to use when redirecting requests\. The default is the protocol that is used in the original request\.  
*Required*: No  
*Type*: String  
*Allowed values*: `http | https`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReplaceKeyPrefixWith`  <a name="cfn-s3-websiteconfiguration-redirectrule-replacekeyprefixwith"></a>
The object key prefix to use in the redirect request\. For example, to redirect requests for all pages with prefix `docs/` \(objects in the `docs/` folder\) to `documents/`, you can set a condition block with `KeyPrefixEquals` set to `docs/` and in the Redirect set `ReplaceKeyPrefixWith` to `/documents`\. Not required if one of the siblings is present\. Can be present only if `ReplaceKeyWith` is not provided\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReplaceKeyWith`  <a name="cfn-s3-websiteconfiguration-redirectrule-replacekeywith"></a>
The specific object key to use in the redirect request\. For example, redirect request to `error.html`\. Not required if one of the siblings is present\. Can be present only if `ReplaceKeyPrefixWith` is not provided\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-s3-websiteconfiguration-routingrules-redirectrule--seealso"></a>
+ AWS::S3::Bucket [Examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.html#aws-properties-s3-bucket--examples)

