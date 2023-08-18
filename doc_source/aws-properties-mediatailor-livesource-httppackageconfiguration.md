# AWS::MediaTailor::LiveSource HttpPackageConfiguration<a name="aws-properties-mediatailor-livesource-httppackageconfiguration"></a>

The HTTP package configuration properties for the requested VOD source\.

## Syntax<a name="aws-properties-mediatailor-livesource-httppackageconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediatailor-livesource-httppackageconfiguration-syntax.json"></a>

```
{
  "[Path](#cfn-mediatailor-livesource-httppackageconfiguration-path)" : String,
  "[SourceGroup](#cfn-mediatailor-livesource-httppackageconfiguration-sourcegroup)" : String,
  "[Type](#cfn-mediatailor-livesource-httppackageconfiguration-type)" : String
}
```

### YAML<a name="aws-properties-mediatailor-livesource-httppackageconfiguration-syntax.yaml"></a>

```
  [Path](#cfn-mediatailor-livesource-httppackageconfiguration-path): String
  [SourceGroup](#cfn-mediatailor-livesource-httppackageconfiguration-sourcegroup): String
  [Type](#cfn-mediatailor-livesource-httppackageconfiguration-type): String
```

## Properties<a name="aws-properties-mediatailor-livesource-httppackageconfiguration-properties"></a>

`Path`  <a name="cfn-mediatailor-livesource-httppackageconfiguration-path"></a>
The relative path to the URL for this VOD source\. This is combined with `SourceLocation::HttpConfiguration::BaseUrl` to form a valid URL\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceGroup`  <a name="cfn-mediatailor-livesource-httppackageconfiguration-sourcegroup"></a>
The name of the source group\. This has to match one of the `Channel::Outputs::SourceGroup`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-mediatailor-livesource-httppackageconfiguration-type"></a>
The streaming protocol for this package configuration\. Supported values are `HLS` and `DASH`\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `DASH | HLS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)