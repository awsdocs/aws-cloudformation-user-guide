# AWS::S3::Bucket WebsiteConfiguration<a name="aws-properties-s3-websiteconfiguration"></a>

Specifies website configuration parameters for an Amazon S3 bucket\.

## Syntax<a name="aws-properties-s3-websiteconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-websiteconfiguration-syntax.json"></a>

```
{
  "[ErrorDocument](#cfn-s3-websiteconfiguration-errordocument)" : String,
  "[IndexDocument](#cfn-s3-websiteconfiguration-indexdocument)" : String,
  "[RedirectAllRequestsTo](#cfn-s3-websiteconfiguration-redirectallrequeststo)" : RedirectAllRequestsTo,
  "[RoutingRules](#cfn-s3-websiteconfiguration-routingrules)" : [ RoutingRule, ... ]
}
```

### YAML<a name="aws-properties-s3-websiteconfiguration-syntax.yaml"></a>

```
  [ErrorDocument](#cfn-s3-websiteconfiguration-errordocument): String
  [IndexDocument](#cfn-s3-websiteconfiguration-indexdocument): String
  [RedirectAllRequestsTo](#cfn-s3-websiteconfiguration-redirectallrequeststo): 
    RedirectAllRequestsTo
  [RoutingRules](#cfn-s3-websiteconfiguration-routingrules): 
    - RoutingRule
```

## Properties<a name="aws-properties-s3-websiteconfiguration-properties"></a>

`ErrorDocument`  <a name="cfn-s3-websiteconfiguration-errordocument"></a>
The name of the error document for the website\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IndexDocument`  <a name="cfn-s3-websiteconfiguration-indexdocument"></a>
The name of the index document for the website\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RedirectAllRequestsTo`  <a name="cfn-s3-websiteconfiguration-redirectallrequeststo"></a>
The redirect behavior for every request to this bucket's website endpoint\.  
If you specify this property, you can't specify any other property\.
*Required*: No  
*Type*: [RedirectAllRequestsTo](aws-properties-s3-websiteconfiguration-redirectallrequeststo.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoutingRules`  <a name="cfn-s3-websiteconfiguration-routingrules"></a>
Rules that define when a redirect is applied and the redirect behavior\.  
*Required*: No  
*Type*: List of [RoutingRule](aws-properties-s3-websiteconfiguration-routingrules.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-s3-websiteconfiguration--seealso"></a>
+ AWS::S3::Bucket [Examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.html#aws-properties-s3-bucket--examples)

