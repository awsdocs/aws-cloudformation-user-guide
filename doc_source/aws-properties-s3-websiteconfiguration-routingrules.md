# AWS::S3::Bucket RoutingRule<a name="aws-properties-s3-websiteconfiguration-routingrules"></a>

Specifies the redirect behavior and when a redirect is applied\. For more information about routing rules, see [Configuring advanced conditional redirects](https://docs.aws.amazon.com/AmazonS3/latest/dev/how-to-page-redirect.html#advanced-conditional-redirects) in the *Amazon Simple Storage Service Developer Guide*\.

## Syntax<a name="aws-properties-s3-websiteconfiguration-routingrules-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-websiteconfiguration-routingrules-syntax.json"></a>

```
{
  "[RedirectRule](#cfn-s3-websiteconfiguration-routingrules-redirectrule)" : RedirectRule,
  "[RoutingRuleCondition](#cfn-s3-websiteconfiguration-routingrules-routingrulecondition)" : RoutingRuleCondition
}
```

### YAML<a name="aws-properties-s3-websiteconfiguration-routingrules-syntax.yaml"></a>

```
  [RedirectRule](#cfn-s3-websiteconfiguration-routingrules-redirectrule): 
    RedirectRule
  [RoutingRuleCondition](#cfn-s3-websiteconfiguration-routingrules-routingrulecondition): 
    RoutingRuleCondition
```

## Properties<a name="aws-properties-s3-websiteconfiguration-routingrules-properties"></a>

`RedirectRule`  <a name="cfn-s3-websiteconfiguration-routingrules-redirectrule"></a>
Container for redirect information\. You can redirect requests to another host, to another page, or with another protocol\. In the event of an error, you can specify a different error code to return\.  
*Required*: Yes  
*Type*: [RedirectRule](aws-properties-s3-websiteconfiguration-routingrules-redirectrule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoutingRuleCondition`  <a name="cfn-s3-websiteconfiguration-routingrules-routingrulecondition"></a>
A container for describing a condition that must be met for the specified redirect to apply\. For example, 1\. If request is for pages in the `/docs` folder, redirect to the `/documents` folder\. 2\. If request results in HTTP error 4xx, redirect request to another host where you might process the error\.  
*Required*: No  
*Type*: [RoutingRuleCondition](aws-properties-s3-websiteconfiguration-routingrules-routingrulecondition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-s3-websiteconfiguration-routingrules--seealso"></a>
+ AWS::S3::Bucket [Examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.html#aws-properties-s3-bucket--examples)

