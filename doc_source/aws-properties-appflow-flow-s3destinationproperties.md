# AWS::AppFlow::Flow S3DestinationProperties<a name="aws-properties-appflow-flow-s3destinationproperties"></a>

 The properties that are applied when Amazon S3 is used as a destination\. 

## Syntax<a name="aws-properties-appflow-flow-s3destinationproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-flow-s3destinationproperties-syntax.json"></a>

```
{
  "[BucketName](#cfn-appflow-flow-s3destinationproperties-bucketname)" : String,
  "[BucketPrefix](#cfn-appflow-flow-s3destinationproperties-bucketprefix)" : String,
  "[S3OutputFormatConfig](#cfn-appflow-flow-s3destinationproperties-s3outputformatconfig)" : S3OutputFormatConfig
}
```

### YAML<a name="aws-properties-appflow-flow-s3destinationproperties-syntax.yaml"></a>

```
  [BucketName](#cfn-appflow-flow-s3destinationproperties-bucketname): String
  [BucketPrefix](#cfn-appflow-flow-s3destinationproperties-bucketprefix): String
  [S3OutputFormatConfig](#cfn-appflow-flow-s3destinationproperties-s3outputformatconfig): 
    S3OutputFormatConfig
```

## Properties<a name="aws-properties-appflow-flow-s3destinationproperties-properties"></a>

`BucketName`  <a name="cfn-appflow-flow-s3destinationproperties-bucketname"></a>
 The Amazon S3 bucket name in which Amazon AppFlow places the transferred data\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `63`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BucketPrefix`  <a name="cfn-appflow-flow-s3destinationproperties-bucketprefix"></a>
 The object key for the destination bucket in which Amazon AppFlow places the files\.   
*Required*: No  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3OutputFormatConfig`  <a name="cfn-appflow-flow-s3destinationproperties-s3outputformatconfig"></a>
 The configuration that determines how Amazon AppFlow should format the flow output data when Amazon S3 is used as the destination\.   
*Required*: No  
*Type*: [S3OutputFormatConfig](aws-properties-appflow-flow-s3outputformatconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-appflow-flow-s3destinationproperties--seealso"></a>
+ [S3DestinationProperties](https://docs.aws.amazon.com/appflow/1.0/APIReference/API_S3DestinationProperties.html) in the *Amazon AppFlow API Reference*\.

