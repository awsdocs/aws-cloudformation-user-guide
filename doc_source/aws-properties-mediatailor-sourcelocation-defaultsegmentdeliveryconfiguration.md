# AWS::MediaTailor::SourceLocation DefaultSegmentDeliveryConfiguration<a name="aws-properties-mediatailor-sourcelocation-defaultsegmentdeliveryconfiguration"></a>

The optional configuration for a server that serves segments\. Use this if you want the segment delivery server to be different from the source location server\. For example, you can configure your source location server to be an origination server, such as MediaPackage, and the segment delivery server to be a content delivery network \(CDN\), such as CloudFront\. If you don't specify a segment delivery server, then the source location server is used\.

## Syntax<a name="aws-properties-mediatailor-sourcelocation-defaultsegmentdeliveryconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediatailor-sourcelocation-defaultsegmentdeliveryconfiguration-syntax.json"></a>

```
{
  "[BaseUrl](#cfn-mediatailor-sourcelocation-defaultsegmentdeliveryconfiguration-baseurl)" : String
}
```

### YAML<a name="aws-properties-mediatailor-sourcelocation-defaultsegmentdeliveryconfiguration-syntax.yaml"></a>

```
  [BaseUrl](#cfn-mediatailor-sourcelocation-defaultsegmentdeliveryconfiguration-baseurl): String
```

## Properties<a name="aws-properties-mediatailor-sourcelocation-defaultsegmentdeliveryconfiguration-properties"></a>

`BaseUrl`  <a name="cfn-mediatailor-sourcelocation-defaultsegmentdeliveryconfiguration-baseurl"></a>
The hostname of the server that will be used to serve segments\. This string must include the protocol, such as **https://**\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)