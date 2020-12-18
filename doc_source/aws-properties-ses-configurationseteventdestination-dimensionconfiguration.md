# AWS::SES::ConfigurationSetEventDestination DimensionConfiguration<a name="aws-properties-ses-configurationseteventdestination-dimensionconfiguration"></a>

Contains the dimension configuration to use when you publish email sending events to Amazon CloudWatch\.

For information about publishing email sending events to Amazon CloudWatch, see the [Amazon SES Developer Guide](https://docs.aws.amazon.com/ses/latest/DeveloperGuide/event-publishing-add-event-destination-cloudwatch.html)\.

## Syntax<a name="aws-properties-ses-configurationseteventdestination-dimensionconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ses-configurationseteventdestination-dimensionconfiguration-syntax.json"></a>

```
{
  "[DefaultDimensionValue](#cfn-ses-configurationseteventdestination-dimensionconfiguration-defaultdimensionvalue)" : String,
  "[DimensionName](#cfn-ses-configurationseteventdestination-dimensionconfiguration-dimensionname)" : String,
  "[DimensionValueSource](#cfn-ses-configurationseteventdestination-dimensionconfiguration-dimensionvaluesource)" : String
}
```

### YAML<a name="aws-properties-ses-configurationseteventdestination-dimensionconfiguration-syntax.yaml"></a>

```
  [DefaultDimensionValue](#cfn-ses-configurationseteventdestination-dimensionconfiguration-defaultdimensionvalue): String
  [DimensionName](#cfn-ses-configurationseteventdestination-dimensionconfiguration-dimensionname): String
  [DimensionValueSource](#cfn-ses-configurationseteventdestination-dimensionconfiguration-dimensionvaluesource): String
```

## Properties<a name="aws-properties-ses-configurationseteventdestination-dimensionconfiguration-properties"></a>

`DefaultDimensionValue`  <a name="cfn-ses-configurationseteventdestination-dimensionconfiguration-defaultdimensionvalue"></a>
The default value of the dimension that is published to Amazon CloudWatch if you do not provide the value of the dimension when you send an email\. The default value must:  
+ Only contain ASCII letters \(a–z, A–Z\), numbers \(0–9\), underscores \(\_\), or dashes \(\-\)\.
+ Contain 256 or fewer characters\.
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DimensionName`  <a name="cfn-ses-configurationseteventdestination-dimensionconfiguration-dimensionname"></a>
The name of an Amazon CloudWatch dimension associated with an email sending metric\. The name must:   
+ Only contain ASCII letters \(a–z, A–Z\), numbers \(0–9\), underscores \(\_\), or dashes \(\-\)\.
+ Contain 256 or fewer characters\.
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DimensionValueSource`  <a name="cfn-ses-configurationseteventdestination-dimensionconfiguration-dimensionvaluesource"></a>
The place where Amazon SES finds the value of a dimension to publish to Amazon CloudWatch\. If you want Amazon SES to use the message tags that you specify using an `X-SES-MESSAGE-TAGS` header or a parameter to the `SendEmail` or `SendRawEmail` API, choose `messageTag`\. If you want Amazon SES to use your own email headers, choose `emailHeader`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)