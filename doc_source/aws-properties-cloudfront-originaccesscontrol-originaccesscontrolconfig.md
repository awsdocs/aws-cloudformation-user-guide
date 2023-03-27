# AWS::CloudFront::OriginAccessControl OriginAccessControlConfig<a name="aws-properties-cloudfront-originaccesscontrol-originaccesscontrolconfig"></a>

Creates a new origin access control in CloudFront\. After you create an origin access control, you can add it to an origin in a CloudFront distribution so that CloudFront sends authenticated \(signed\) requests to the origin\.

This makes it possible to block public access to the origin, allowing viewers \(users\) to access the origin's content only through CloudFront\.

For more information about using a CloudFront origin access control, see [Restricting access to an AWS origin](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-restricting-access-to-origin.html) in the *Amazon CloudFront Developer Guide*\.

## Syntax<a name="aws-properties-cloudfront-originaccesscontrol-originaccesscontrolconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-originaccesscontrol-originaccesscontrolconfig-syntax.json"></a>

```
{
  "[Description](#cfn-cloudfront-originaccesscontrol-originaccesscontrolconfig-description)" : String,
  "[Name](#cfn-cloudfront-originaccesscontrol-originaccesscontrolconfig-name)" : String,
  "[OriginAccessControlOriginType](#cfn-cloudfront-originaccesscontrol-originaccesscontrolconfig-originaccesscontrolorigintype)" : String,
  "[SigningBehavior](#cfn-cloudfront-originaccesscontrol-originaccesscontrolconfig-signingbehavior)" : String,
  "[SigningProtocol](#cfn-cloudfront-originaccesscontrol-originaccesscontrolconfig-signingprotocol)" : String
}
```

### YAML<a name="aws-properties-cloudfront-originaccesscontrol-originaccesscontrolconfig-syntax.yaml"></a>

```
  [Description](#cfn-cloudfront-originaccesscontrol-originaccesscontrolconfig-description): String
  [Name](#cfn-cloudfront-originaccesscontrol-originaccesscontrolconfig-name): String
  [OriginAccessControlOriginType](#cfn-cloudfront-originaccesscontrol-originaccesscontrolconfig-originaccesscontrolorigintype): String
  [SigningBehavior](#cfn-cloudfront-originaccesscontrol-originaccesscontrolconfig-signingbehavior): String
  [SigningProtocol](#cfn-cloudfront-originaccesscontrol-originaccesscontrolconfig-signingprotocol): String
```

## Properties<a name="aws-properties-cloudfront-originaccesscontrol-originaccesscontrolconfig-properties"></a>

`Description`  <a name="cfn-cloudfront-originaccesscontrol-originaccesscontrolconfig-description"></a>
A description of the origin access control\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-cloudfront-originaccesscontrol-originaccesscontrolconfig-name"></a>
A name to identify the origin access control\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OriginAccessControlOriginType`  <a name="cfn-cloudfront-originaccesscontrol-originaccesscontrolconfig-originaccesscontrolorigintype"></a>
The type of origin that this origin access control is for\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `mediastore | s3`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SigningBehavior`  <a name="cfn-cloudfront-originaccesscontrol-originaccesscontrolconfig-signingbehavior"></a>
Specifies which requests CloudFront signs \(adds authentication information to\)\. Specify `always` for the most common use case\. For more information, see [origin access control advanced settings](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-restricting-access-to-s3.html#oac-advanced-settings) in the *Amazon CloudFront Developer Guide*\.  
This field can have one of the following values:  
+  `always` – CloudFront signs all origin requests, overwriting the `Authorization` header from the viewer request if one exists\.
+  `never` – CloudFront doesn't sign any origin requests\. This value turns off origin access control for all origins in all distributions that use this origin access control\.
+  `no-override` – If the viewer request doesn't contain the `Authorization` header, then CloudFront signs the origin request\. If the viewer request contains the `Authorization` header, then CloudFront doesn't sign the origin request and instead passes along the `Authorization` header from the viewer request\. **WARNING: To pass along the `Authorization` header from the viewer request, you *must* add the `Authorization` header to a [cache policy](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/controlling-the-cache-key.html) for all cache behaviors that use origins associated with this origin access control\.** 
*Required*: Yes  
*Type*: String  
*Allowed values*: `always | never | no-override`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SigningProtocol`  <a name="cfn-cloudfront-originaccesscontrol-originaccesscontrolconfig-signingprotocol"></a>
The signing protocol of the origin access control, which determines how CloudFront signs \(authenticates\) requests\. The only valid value is `sigv4`\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `sigv4`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)