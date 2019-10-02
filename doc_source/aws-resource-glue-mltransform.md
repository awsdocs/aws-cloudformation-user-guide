# AWS::Glue::MLTransform<a name="aws-resource-glue-mltransform"></a>

The AWS::Glue::MLTransform is an AWS Glue resource type that manages machine learning transforms\.

## Syntax<a name="aws-resource-glue-mltransform-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-glue-mltransform-syntax.json"></a>

```
{
  "Type" : "AWS::Glue::MLTransform",
  "Properties" : {
      "[Description](#cfn-glue-mltransform-description)" : String,
      "[InputRecordTables](#cfn-glue-mltransform-inputrecordtables)" : [InputRecordTables](aws-properties-glue-mltransform-inputrecordtables.md),
      "[MaxCapacity](#cfn-glue-mltransform-maxcapacity)" : Double,
      "[MaxRetries](#cfn-glue-mltransform-maxretries)" : Integer,
      "[Name](#cfn-glue-mltransform-name)" : String,
      "[NumberOfWorkers](#cfn-glue-mltransform-numberofworkers)" : Integer,
      "[Role](#cfn-glue-mltransform-role)" : String,
      "[Timeout](#cfn-glue-mltransform-timeout)" : Integer,
      "[TransformParameters](#cfn-glue-mltransform-transformparameters)" : [TransformParameters](aws-properties-glue-mltransform-transformparameters.md),
      "[WorkerType](#cfn-glue-mltransform-workertype)" : String
    }
}
```

### YAML<a name="aws-resource-glue-mltransform-syntax.yaml"></a>

```
Type: AWS::Glue::MLTransform
Properties: 
  [Description](#cfn-glue-mltransform-description): String
  [InputRecordTables](#cfn-glue-mltransform-inputrecordtables): 
    [InputRecordTables](aws-properties-glue-mltransform-inputrecordtables.md)
  [MaxCapacity](#cfn-glue-mltransform-maxcapacity): Double
  [MaxRetries](#cfn-glue-mltransform-maxretries): Integer
  [Name](#cfn-glue-mltransform-name): String
  [NumberOfWorkers](#cfn-glue-mltransform-numberofworkers): Integer
  [Role](#cfn-glue-mltransform-role): String
  [Timeout](#cfn-glue-mltransform-timeout): Integer
  [TransformParameters](#cfn-glue-mltransform-transformparameters): 
    [TransformParameters](aws-properties-glue-mltransform-transformparameters.md)
  [WorkerType](#cfn-glue-mltransform-workertype): String
```

## Properties<a name="aws-resource-glue-mltransform-properties"></a>

`Description`  <a name="cfn-glue-mltransform-description"></a>
A user\-defined, long\-form description text for the machine learning transform\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InputRecordTables`  <a name="cfn-glue-mltransform-inputrecordtables"></a>
A list of AWS Glue table definitions used by the transform\.  
*Required*: Yes  
*Type*: [InputRecordTables](aws-properties-glue-mltransform-inputrecordtables.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MaxCapacity`  <a name="cfn-glue-mltransform-maxcapacity"></a>
The number of AWS Glue data processing units \(DPUs\) that are allocated to task runs for this transform\. You can allocate from 2 to 100 DPUs; the default is 10\. A DPU is a relative measure of processing power that consists of 4 vCPUs of compute capacity and 16 GB of memory\. For more information, see the [AWS Glue pricing page](http://aws.amazon.com/glue/pricing/)\.   
`MaxCapacity` is a mutually exclusive option with `NumberOfWorkers` and `WorkerType`\.  
+ If either `NumberOfWorkers` or `WorkerType` is set, then `MaxCapacity` cannot be set\.
+ If `MaxCapacity` is set then neither `NumberOfWorkers` or `WorkerType` can be set\.
+ If `WorkerType` is set, then `NumberOfWorkers` is required \(and vice versa\)\.
+ `MaxCapacity` and `NumberOfWorkers` must both be at least 1\.
When the `WorkerType` field is set to a value other than `Standard`, the `MaxCapacity` field is set automatically and becomes read\-only\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxRetries`  <a name="cfn-glue-mltransform-maxretries"></a>
The maximum number of times to retry after an `MLTaskRun` of the machine learning transform fails\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-glue-mltransform-name"></a>
A user\-defined name for the machine learning transform\. Names are required to be unique\. `Name` is optional\. If you supply `Name`, the stack cannot be repeatedly created\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NumberOfWorkers`  <a name="cfn-glue-mltransform-numberofworkers"></a>
The number of workers of a defined `workerType` that are allocated when a task of the transform runs\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Role`  <a name="cfn-glue-mltransform-role"></a>
The name or Amazon Resource Name \(ARN\) of the IAM role with the required permissions\. This role needs permission to your Amazon Simple Storage Service \(Amazon S3\) sources, targets, temporary directory, scripts, and any libraries used by the task run for this transform\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Timeout`  <a name="cfn-glue-mltransform-timeout"></a>
The timeout in minutes of the machine learning transform\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TransformParameters`  <a name="cfn-glue-mltransform-transformparameters"></a>
The algorithm\-specific parameters that are associated with the machine learning transform\.  
*Required*: Yes  
*Type*: [TransformParameters](aws-properties-glue-mltransform-transformparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WorkerType`  <a name="cfn-glue-mltransform-workertype"></a>
The type of predefined worker that is allocated when a task of this transform runs\. Accepts a value of Standard, G\.1X, or G\.2X\.  
+ For the `Standard` worker type, each worker provides 4 vCPU, 16 GB of memory and a 50GB disk, and 2 executors per worker\.
+ For the `G.1X` worker type, each worker provides 4 vCPU, 16 GB of memory and a 64GB disk, and 1 executor per worker\.
+ For the `G.2X` worker type, each worker provides 8 vCPU, 32 GB of memory and a 128GB disk, and 1 executor per worker\.
`MaxCapacity` is a mutually exclusive option with `NumberOfWorkers` and `WorkerType`\.  
+ If either `NumberOfWorkers` or `WorkerType` is set, then `MaxCapacity` cannot be set\.
+ If `MaxCapacity` is set then neither `NumberOfWorkers` or `WorkerType` can be set\.
+ If `WorkerType` is set, then `NumberOfWorkers` is required \(and vice versa\)\.
+ `MaxCapacity` and `NumberOfWorkers` must both be at least 1\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-glue-mltransform-return-values"></a>

### Ref<a name="aws-resource-glue-mltransform-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the transform name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Supported Regions

This ResourceType is supported by the following regions:

- `ap-northeast-1`
- `eu-west-1`
- `us-east-1`
- `us-east-2`
- `us-west-2`
