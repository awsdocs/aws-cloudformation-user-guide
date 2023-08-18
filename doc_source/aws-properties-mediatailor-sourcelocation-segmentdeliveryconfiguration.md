# AWS::MediaTailor::SourceLocation SegmentDeliveryConfiguration<a name="aws-properties-mediatailor-sourcelocation-segmentdeliveryconfiguration"></a>

The segment delivery configuration settings\.

## Syntax<a name="aws-properties-mediatailor-sourcelocation-segmentdeliveryconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediatailor-sourcelocation-segmentdeliveryconfiguration-syntax.json"></a>

```
{
  "[BaseUrl](#cfn-mediatailor-sourcelocation-segmentdeliveryconfiguration-baseurl)" : String,
  "[Name](#cfn-mediatailor-sourcelocation-segmentdeliveryconfiguration-name)" : String
}
```

### YAML<a name="aws-properties-mediatailor-sourcelocation-segmentdeliveryconfiguration-syntax.yaml"></a>

```
  [BaseUrl](#cfn-mediatailor-sourcelocation-segmentdeliveryconfiguration-baseurl): String
  [Name](#cfn-mediatailor-sourcelocation-segmentdeliveryconfiguration-name): String
```

## Properties<a name="aws-properties-mediatailor-sourcelocation-segmentdeliveryconfiguration-properties"></a>

`BaseUrl`  <a name="cfn-mediatailor-sourcelocation-segmentdeliveryconfiguration-baseurl"></a>
The base URL of the host or path of the segment delivery server that you're using to serve segments\. This is typically a content delivery network \(CDN\)\. The URL can be absolute or relative\. To use an absolute URL include the protocol, such as `https://example.com/some/path`\. To use a relative URL specify the relative path, such as `/some/path*`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-mediatailor-sourcelocation-segmentdeliveryconfiguration-name"></a>
A unique identifier used to distinguish between multiple segment delivery configurations in a source location\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)