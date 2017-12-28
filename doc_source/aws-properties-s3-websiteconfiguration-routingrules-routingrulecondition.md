# Amazon S3 Website Configuration Routing Rules Routing Rule Condition Property<a name="aws-properties-s3-websiteconfiguration-routingrules-routingrulecondition"></a>

The `RoutingRuleCondition` property is an embedded property of the [Amazon S3 Website Configuration Routing Rules Property](aws-properties-s3-websiteconfiguration-routingrules.md) that describes a condition that must be met for a redirect to apply\.

## Syntax<a name="w3ab2c21c14e1566b5"></a>

### JSON<a name="aws-properties-s3-websiteconfiguration-routingrules-routingrulecondition-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-websiteconfiguration-routingrules-routingrulecondition-httperrorcodereturnedequals)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-websiteconfiguration-routingrules-routingrulecondition-keyprefixequals)" : String
}
```

### YAML<a name="aws-properties-s3-websiteconfiguration-routingrules-routingrulecondition-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-websiteconfiguration-routingrules-routingrulecondition-httperrorcodereturnedequals): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-websiteconfiguration-routingrules-routingrulecondition-keyprefixequals): String
```

## Properties<a name="w3ab2c21c14e1566b7"></a>

`HttpErrorCodeReturnedEquals`  
Applies this redirect if the error code equals this value in the event of an error\.  
*Required: *Conditional\. You must specify at least one condition property\.  
*Type*: String

`KeyPrefixEquals`  
The object key name prefix when the redirect is applied\. For example, to redirect requests for `ExamplePage.html`, set the key prefix to `ExamplePage.html`\. To redirect request for all pages with the prefix `docs/`, set the key prefix to `docs/`, which identifies all objects in the `docs/` folder\.  
*Required: *Conditional\. You must at least one condition property\.  
*Type*: String