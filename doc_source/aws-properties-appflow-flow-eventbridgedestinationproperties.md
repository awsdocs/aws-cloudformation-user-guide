# AWS::AppFlow::Flow EventBridgeDestinationProperties<a name="aws-properties-appflow-flow-eventbridgedestinationproperties"></a>

 The properties that are applied when Amazon EventBridge is being used as a destination\. 

## Syntax<a name="aws-properties-appflow-flow-eventbridgedestinationproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-flow-eventbridgedestinationproperties-syntax.json"></a>

```
{
  "[ErrorHandlingConfig](#cfn-appflow-flow-eventbridgedestinationproperties-errorhandlingconfig)" : ErrorHandlingConfig,
  "[Object](#cfn-appflow-flow-eventbridgedestinationproperties-object)" : String
}
```

### YAML<a name="aws-properties-appflow-flow-eventbridgedestinationproperties-syntax.yaml"></a>

```
  [ErrorHandlingConfig](#cfn-appflow-flow-eventbridgedestinationproperties-errorhandlingconfig): 
    ErrorHandlingConfig
  [Object](#cfn-appflow-flow-eventbridgedestinationproperties-object): String
```

## Properties<a name="aws-properties-appflow-flow-eventbridgedestinationproperties-properties"></a>

`ErrorHandlingConfig`  <a name="cfn-appflow-flow-eventbridgedestinationproperties-errorhandlingconfig"></a>
 The object specified in the Amplitude flow source\.   
*Required*: No  
*Type*: [ErrorHandlingConfig](aws-properties-appflow-flow-errorhandlingconfig.md)  
*Maximum*: `512`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Object`  <a name="cfn-appflow-flow-eventbridgedestinationproperties-object"></a>
 The object specified in the Amazon EventBridge flow destination\.   
*Required*: Yes  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-appflow-flow-eventbridgedestinationproperties--seealso"></a>
+ [EventBridgeDestinationProperties](https://docs.aws.amazon.com/appflow/1.0/APIReference/API_EventBridgeDestinationProperties.html) in the *Amazon AppFlow API Reference*\.

