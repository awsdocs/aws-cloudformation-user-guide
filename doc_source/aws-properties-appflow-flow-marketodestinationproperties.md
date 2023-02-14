# AWS::AppFlow::Flow MarketoDestinationProperties<a name="aws-properties-appflow-flow-marketodestinationproperties"></a>

The properties that Amazon AppFlow applies when you use Marketo as a flow destination\.

## Syntax<a name="aws-properties-appflow-flow-marketodestinationproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-flow-marketodestinationproperties-syntax.json"></a>

```
{
  "[ErrorHandlingConfig](#cfn-appflow-flow-marketodestinationproperties-errorhandlingconfig)" : ErrorHandlingConfig,
  "[Object](#cfn-appflow-flow-marketodestinationproperties-object)" : String
}
```

### YAML<a name="aws-properties-appflow-flow-marketodestinationproperties-syntax.yaml"></a>

```
  [ErrorHandlingConfig](#cfn-appflow-flow-marketodestinationproperties-errorhandlingconfig): 
    ErrorHandlingConfig
  [Object](#cfn-appflow-flow-marketodestinationproperties-object): String
```

## Properties<a name="aws-properties-appflow-flow-marketodestinationproperties-properties"></a>

`ErrorHandlingConfig`  <a name="cfn-appflow-flow-marketodestinationproperties-errorhandlingconfig"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: [ErrorHandlingConfig](aws-properties-appflow-flow-errorhandlingconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Object`  <a name="cfn-appflow-flow-marketodestinationproperties-object"></a>
The object specified in the Marketo flow destination\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)