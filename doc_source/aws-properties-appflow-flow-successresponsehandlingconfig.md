# AWS::AppFlow::Flow SuccessResponseHandlingConfig<a name="aws-properties-appflow-flow-successresponsehandlingconfig"></a>

Determines how Amazon AppFlow handles the success response that it gets from the connector after placing data\.

For example, this setting would determine where to write the response from the destination connector upon a successful insert operation\.

## Syntax<a name="aws-properties-appflow-flow-successresponsehandlingconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-flow-successresponsehandlingconfig-syntax.json"></a>

```
{
  "[BucketName](#cfn-appflow-flow-successresponsehandlingconfig-bucketname)" : String,
  "[BucketPrefix](#cfn-appflow-flow-successresponsehandlingconfig-bucketprefix)" : String
}
```

### YAML<a name="aws-properties-appflow-flow-successresponsehandlingconfig-syntax.yaml"></a>

```
  [BucketName](#cfn-appflow-flow-successresponsehandlingconfig-bucketname): String
  [BucketPrefix](#cfn-appflow-flow-successresponsehandlingconfig-bucketprefix): String
```

## Properties<a name="aws-properties-appflow-flow-successresponsehandlingconfig-properties"></a>

`BucketName`  <a name="cfn-appflow-flow-successresponsehandlingconfig-bucketname"></a>
The name of the Amazon S3 bucket\.  
*Required*: No  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `63`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BucketPrefix`  <a name="cfn-appflow-flow-successresponsehandlingconfig-bucketprefix"></a>
The Amazon S3 bucket prefix\.  
*Required*: No  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)