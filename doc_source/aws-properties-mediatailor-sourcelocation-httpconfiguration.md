# AWS::MediaTailor::SourceLocation HttpConfiguration<a name="aws-properties-mediatailor-sourcelocation-httpconfiguration"></a>

The HTTP configuration for the source location\.

## Syntax<a name="aws-properties-mediatailor-sourcelocation-httpconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediatailor-sourcelocation-httpconfiguration-syntax.json"></a>

```
{
  "[BaseUrl](#cfn-mediatailor-sourcelocation-httpconfiguration-baseurl)" : String
}
```

### YAML<a name="aws-properties-mediatailor-sourcelocation-httpconfiguration-syntax.yaml"></a>

```
  [BaseUrl](#cfn-mediatailor-sourcelocation-httpconfiguration-baseurl): String
```

## Properties<a name="aws-properties-mediatailor-sourcelocation-httpconfiguration-properties"></a>

`BaseUrl`  <a name="cfn-mediatailor-sourcelocation-httpconfiguration-baseurl"></a>
The base URL for the source location host server\. This string must include the protocol, such as **https://**\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)