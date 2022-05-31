# AWS::Timestream::ScheduledQuery ErrorReportConfiguration<a name="aws-properties-timestream-scheduledquery-errorreportconfiguration"></a>

Configuration required for error reporting\.

## Syntax<a name="aws-properties-timestream-scheduledquery-errorreportconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-timestream-scheduledquery-errorreportconfiguration-syntax.json"></a>

```
{
  "[S3Configuration](#cfn-timestream-scheduledquery-errorreportconfiguration-s3configuration)" : S3Configuration
}
```

### YAML<a name="aws-properties-timestream-scheduledquery-errorreportconfiguration-syntax.yaml"></a>

```
  [S3Configuration](#cfn-timestream-scheduledquery-errorreportconfiguration-s3configuration): 
    S3Configuration
```

## Properties<a name="aws-properties-timestream-scheduledquery-errorreportconfiguration-properties"></a>

`S3Configuration`  <a name="cfn-timestream-scheduledquery-errorreportconfiguration-s3configuration"></a>
The S3 configuration for the error reports\.  
*Required*: Yes  
*Type*: [S3Configuration](aws-properties-timestream-scheduledquery-s3configuration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)