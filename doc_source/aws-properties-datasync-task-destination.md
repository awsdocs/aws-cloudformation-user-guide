# AWS::DataSync::Task Destination<a name="aws-properties-datasync-task-destination"></a>

Specifies where DataSync uploads your [task report](https://docs.aws.amazon.com/datasync/latest/userguide/creating-task-reports.html)\.

## Syntax<a name="aws-properties-datasync-task-destination-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-datasync-task-destination-syntax.json"></a>

```
{
  "[S3](#cfn-datasync-task-destination-s3)" : S3
}
```

### YAML<a name="aws-properties-datasync-task-destination-syntax.yaml"></a>

```
  [S3](#cfn-datasync-task-destination-s3): 
    S3
```

## Properties<a name="aws-properties-datasync-task-destination-properties"></a>

`S3`  <a name="cfn-datasync-task-destination-s3"></a>
Specifies the Amazon S3 bucket where DataSync uploads your task report\.  
*Required*: No  
*Type*: [S3](aws-properties-datasync-task-s3.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)