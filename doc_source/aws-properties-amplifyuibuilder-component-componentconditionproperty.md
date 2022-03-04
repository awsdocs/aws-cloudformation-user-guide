# AWS::AmplifyUIBuilder::Component ComponentConditionProperty<a name="aws-properties-amplifyuibuilder-component-componentconditionproperty"></a>

The `ComponentConditionProperty` property specifies a conditional expression for setting a component property\. Use `ComponentConditionProperty` to set a property to different values conditionally, based on the value of another property\.

## Syntax<a name="aws-properties-amplifyuibuilder-component-componentconditionproperty-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-amplifyuibuilder-component-componentconditionproperty-syntax.json"></a>

```
{
  "[Else](#cfn-amplifyuibuilder-component-componentconditionproperty-else)" : ComponentProperty,
  "[Field](#cfn-amplifyuibuilder-component-componentconditionproperty-field)" : String,
  "[Operand](#cfn-amplifyuibuilder-component-componentconditionproperty-operand)" : String,
  "[OperandType](#cfn-amplifyuibuilder-component-componentconditionproperty-operandtype)" : String,
  "[Operator](#cfn-amplifyuibuilder-component-componentconditionproperty-operator)" : String,
  "[Property](#cfn-amplifyuibuilder-component-componentconditionproperty-property)" : String,
  "[Then](#cfn-amplifyuibuilder-component-componentconditionproperty-then)" : ComponentProperty
}
```

### YAML<a name="aws-properties-amplifyuibuilder-component-componentconditionproperty-syntax.yaml"></a>

```
  [Else](#cfn-amplifyuibuilder-component-componentconditionproperty-else): 
    ComponentProperty
  [Field](#cfn-amplifyuibuilder-component-componentconditionproperty-field): String
  [Operand](#cfn-amplifyuibuilder-component-componentconditionproperty-operand): String
  [OperandType](#cfn-amplifyuibuilder-component-componentconditionproperty-operandtype): String
  [Operator](#cfn-amplifyuibuilder-component-componentconditionproperty-operator): String
  [Property](#cfn-amplifyuibuilder-component-componentconditionproperty-property): String
  [Then](#cfn-amplifyuibuilder-component-componentconditionproperty-then): 
    ComponentProperty
```

## Properties<a name="aws-properties-amplifyuibuilder-component-componentconditionproperty-properties"></a>

`Else`  <a name="cfn-amplifyuibuilder-component-componentconditionproperty-else"></a>
The value to assign to the property if the condition is not met\.  
*Required*: No  
*Type*: [ComponentProperty](aws-properties-amplifyuibuilder-component-componentproperty.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Field`  <a name="cfn-amplifyuibuilder-component-componentconditionproperty-field"></a>
The name of a field\. Specify this when the property is a data model\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Operand`  <a name="cfn-amplifyuibuilder-component-componentconditionproperty-operand"></a>
The value of the property to evaluate\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OperandType`  <a name="cfn-amplifyuibuilder-component-componentconditionproperty-operandtype"></a>
The type of the property to evaluate\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Operator`  <a name="cfn-amplifyuibuilder-component-componentconditionproperty-operator"></a>
The operator to use to perform the evaluation, such as `eq` to represent equals\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Property`  <a name="cfn-amplifyuibuilder-component-componentconditionproperty-property"></a>
The name of the conditional property\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Then`  <a name="cfn-amplifyuibuilder-component-componentconditionproperty-then"></a>
The value to assign to the property if the condition is met\.  
*Required*: No  
*Type*: [ComponentProperty](aws-properties-amplifyuibuilder-component-componentproperty.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)