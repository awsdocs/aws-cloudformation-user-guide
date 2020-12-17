# AWS::S3::Bucket RoutingRuleCondition<a name="aws-properties-s3-websiteconfiguration-routingrules-routingrulecondition"></a>

A container for describing a condition that must be met for the specified redirect to apply\. For example, 1\. If request is for pages in the `/docs` folder, redirect to the `/documents` folder\. 2\. If request results in HTTP error 4xx, redirect request to another host where you might process the error\.

## Syntax<a name="aws-properties-s3-websiteconfiguration-routingrules-routingrulecondition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-websiteconfiguration-routingrules-routingrulecondition-syntax.json"></a>

```
{
  "[HttpErrorCodeReturnedEquals](#cfn-s3-websiteconfiguration-routingrules-routingrulecondition-httperrorcodereturnedequals)" : String,
  "[KeyPrefixEquals](#cfn-s3-websiteconfiguration-routingrules-routingrulecondition-keyprefixequals)" : String
}
```

### YAML<a name="aws-properties-s3-websiteconfiguration-routingrules-routingrulecondition-syntax.yaml"></a>

```
  [HttpErrorCodeReturnedEquals](#cfn-s3-websiteconfiguration-routingrules-routingrulecondition-httperrorcodereturnedequals): String
  [KeyPrefixEquals](#cfn-s3-websiteconfiguration-routingrules-routingrulecondition-keyprefixequals): String
```

## Properties<a name="aws-properties-s3-websiteconfiguration-routingrules-routingrulecondition-properties"></a>

`HttpErrorCodeReturnedEquals`  <a name="cfn-s3-websiteconfiguration-routingrules-routingrulecondition-httperrorcodereturnedequals"></a>
The HTTP error code when the redirect is applied\. In the event of an error, if the error code equals this value, then the specified redirect is applied\.  
Required when parent element `Condition` is specified and sibling `KeyPrefixEquals` is not specified\. If both are specified, then both must be true for the redirect to be applied\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KeyPrefixEquals`  <a name="cfn-s3-websiteconfiguration-routingrules-routingrulecondition-keyprefixequals"></a>
The object key name prefix when the redirect is applied\. For example, to redirect requests for `ExamplePage.html`, the key prefix will be `ExamplePage.html`\. To redirect request for all pages with the prefix `docs/`, the key prefix will be `/docs`, which identifies all objects in the docs/ folder\.  
Required when the parent element `Condition` is specified and sibling `HttpErrorCodeReturnedEquals` is not specified\. If both conditions are specified, both must be true for the redirect to be applied\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-s3-websiteconfiguration-routingrules-routingrulecondition--seealso"></a>
+ AWS::S3::Bucket [Examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.html#aws-properties-s3-bucket--examples)

