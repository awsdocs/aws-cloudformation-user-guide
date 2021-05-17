# AWS::AppFlow::Flow SnowflakeDestinationProperties<a name="aws-properties-appflow-flow-snowflakedestinationproperties"></a>

 The properties that are applied when Snowflake is being used as a destination\. 

## Syntax<a name="aws-properties-appflow-flow-snowflakedestinationproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-flow-snowflakedestinationproperties-syntax.json"></a>

```
{
  "[BucketPrefix](#cfn-appflow-flow-snowflakedestinationproperties-bucketprefix)" : String,
  "[ErrorHandlingConfig](#cfn-appflow-flow-snowflakedestinationproperties-errorhandlingconfig)" : ErrorHandlingConfig,
  "[IntermediateBucketName](#cfn-appflow-flow-snowflakedestinationproperties-intermediatebucketname)" : String,
  "[Object](#cfn-appflow-flow-snowflakedestinationproperties-object)" : String
}
```

### YAML<a name="aws-properties-appflow-flow-snowflakedestinationproperties-syntax.yaml"></a>

```
  [BucketPrefix](#cfn-appflow-flow-snowflakedestinationproperties-bucketprefix): String
  [ErrorHandlingConfig](#cfn-appflow-flow-snowflakedestinationproperties-errorhandlingconfig): 
    ErrorHandlingConfig
  [IntermediateBucketName](#cfn-appflow-flow-snowflakedestinationproperties-intermediatebucketname): String
  [Object](#cfn-appflow-flow-snowflakedestinationproperties-object): String
```

## Properties<a name="aws-properties-appflow-flow-snowflakedestinationproperties-properties"></a>

`BucketPrefix`  <a name="cfn-appflow-flow-snowflakedestinationproperties-bucketprefix"></a>
 The object key for the destination bucket in which Amazon AppFlow places the files\.   
*Required*: No  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ErrorHandlingConfig`  <a name="cfn-appflow-flow-snowflakedestinationproperties-errorhandlingconfig"></a>
 The settings that determine how Amazon AppFlow handles an error when placing data in the Snowflake destination\. For example, this setting would determine if the flow should fail after one insertion error, or continue and attempt to insert every record regardless of the initial failure\. `ErrorHandlingConfig` is a part of the destination connector details\.   
*Required*: No  
*Type*: [ErrorHandlingConfig](aws-properties-appflow-flow-errorhandlingconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IntermediateBucketName`  <a name="cfn-appflow-flow-snowflakedestinationproperties-intermediatebucketname"></a>
 The intermediate bucket that Amazon AppFlow uses when moving data into Snowflake\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `63`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Object`  <a name="cfn-appflow-flow-snowflakedestinationproperties-object"></a>
 The object specified in the Snowflake flow destination\.   
*Required*: Yes  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-appflow-flow-snowflakedestinationproperties--seealso"></a>
+ [SnowflakeDestinationProperties](https://docs.aws.amazon.com/appflow/1.0/APIReference/API_SnowflakeDestinationProperties.html) in the *Amazon AppFlow API Reference*\.

