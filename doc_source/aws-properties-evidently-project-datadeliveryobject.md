# AWS::Evidently::Project DataDeliveryObject<a name="aws-properties-evidently-project-datadeliveryobject"></a>

A structure that contains information about where Evidently is to store evaluation events for longer term storage\.

## Syntax<a name="aws-properties-evidently-project-datadeliveryobject-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-evidently-project-datadeliveryobject-syntax.json"></a>

```
{
  "[LogGroup](#cfn-evidently-project-datadeliveryobject-loggroup)" : String,
  "[S3](#cfn-evidently-project-datadeliveryobject-s3)" : S3Destination
}
```

### YAML<a name="aws-properties-evidently-project-datadeliveryobject-syntax.yaml"></a>

```
  [LogGroup](#cfn-evidently-project-datadeliveryobject-loggroup): String
  [S3](#cfn-evidently-project-datadeliveryobject-s3): 
    S3Destination
```

## Properties<a name="aws-properties-evidently-project-datadeliveryobject-properties"></a>

`LogGroup`  <a name="cfn-evidently-project-datadeliveryobject-loggroup"></a>
If the project stores evaluation events in CloudWatch Logs, this structure stores the log group name\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3`  <a name="cfn-evidently-project-datadeliveryobject-s3"></a>
If the project stores evaluation events in an Amazon S3 bucket, this structure stores the bucket name and bucket prefix\.  
*Required*: No  
*Type*: [S3Destination](aws-properties-evidently-project-s3destination.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)