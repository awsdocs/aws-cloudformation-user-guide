# Amazon Simple Email Service ConfigurationSetEventDestination DimensionConfiguration<a name="aws-properties-ses-configurationseteventdestination-dimensionconfiguration"></a>

<a name="aws-properties-ses-configurationseteventdestination-dimensionconfiguration-description"></a>The `DimensionConfiguration` property type specifies the dimension configuration to use when you publish email sending events to Amazon CloudWatch using Amazon SES\.

<a name="aws-properties-ses-configurationseteventdestination-dimensionconfiguration-inheritance"></a> `DimensionConfiguration` is a property of the [Amazon SES ConfigurationSetEventDestination CloudWatchDestination](aws-properties-ses-configurationseteventdestination-cloudwatchdestination.md) property type\.

## Syntax<a name="aws-properties-ses-configurationseteventdestination-dimensionconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ses-configurationseteventdestination-dimensionconfiguration-syntax.json"></a>

```
{
  "[DimensionValueSource](#cfn-ses-configurationseteventdestination-dimensionconfiguration-dimensionvaluesource)" : String,
  "[DefaultDimensionValue](#cfn-ses-configurationseteventdestination-dimensionconfiguration-defaultdimensionvalue)" : String,
  "[DimensionName](#cfn-ses-configurationseteventdestination-dimensionconfiguration-dimensionname)" : String
}
```

### YAML<a name="aws-properties-ses-configurationseteventdestination-dimensionconfiguration-syntax.yaml"></a>

```
[DimensionValueSource](#cfn-ses-configurationseteventdestination-dimensionconfiguration-dimensionvaluesource): String
[DefaultDimensionValue](#cfn-ses-configurationseteventdestination-dimensionconfiguration-defaultdimensionvalue): String
[DimensionName](#cfn-ses-configurationseteventdestination-dimensionconfiguration-dimensionname): String
```

## Properties<a name="aws-properties-ses-configurationseteventdestination-dimensionconfiguration-properties"></a>

`DefaultDimensionValue`  <a name="cfn-ses-configurationseteventdestination-dimensionconfiguration-defaultdimensionvalue"></a>
The default value of the dimension that is published to Amazon CloudWatch if you do not provide the value of the dimension when you send an email\. The default value can:  
+ Contain ASCII letters \(a\-z, A\-Z\), numbers \(0\-9\), underscores \(\_\), or dashes \(\-\)\.
+ Contain up to 256 characters\.
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`DimensionName`  <a name="cfn-ses-configurationseteventdestination-dimensionconfiguration-dimensionname"></a>
The name of an Amazon CloudWatch dimension associated with an email sending metric\. The name can:  
+ Contain ASCII letters \(a\-z, A\-Z\), numbers \(0\-9\), underscores \(\_\), or dashes \(\-\)\.
+ Contain up to 256 characters\.
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`DimensionValueSource`  <a name="cfn-ses-configurationseteventdestination-dimensionconfiguration-dimensionvaluesource"></a>
The place where Amazon SES finds the value of a dimension to publish to CloudWatch\. If you want Amazon SES to use the message tags that you specify using an `X-SES-MESSAGE-TAGS` header or a parameter to the `SendEmail/SendRawEmail`API, choose `messageTag`\. If you want Amazon SES to use your own email headers, choose `emailHeader`\.  
Valid values include: `emailHeader`, `linkTag`, and `messageTag`\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-ses-configurationseteventdestination-dimensionconfiguration-seealso"></a>
+ [Using Amazon SES Configuration Sets](url-ses-dev;using-configuration-sets.html) in the *Amazon Simple Email Service Developer Guide*
+ [CloudWatchDimensionConfiguration](http://docs.aws.amazon.com/ses/latest/APIReference/API_CloudWatchDimensionConfiguration.html) in the *Amazon Simple Email Service API Reference*