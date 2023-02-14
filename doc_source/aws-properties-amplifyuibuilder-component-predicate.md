# AWS::AmplifyUIBuilder::Component Predicate<a name="aws-properties-amplifyuibuilder-component-predicate"></a>

The `Predicate` property specifies information for generating Amplify DataStore queries\. Use `Predicate` to retrieve a subset of the data in a collection\.

## Syntax<a name="aws-properties-amplifyuibuilder-component-predicate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-amplifyuibuilder-component-predicate-syntax.json"></a>

```
{
  "[And](#cfn-amplifyuibuilder-component-predicate-and)" : [ Predicate, ... ],
  "[Field](#cfn-amplifyuibuilder-component-predicate-field)" : String,
  "[Operand](#cfn-amplifyuibuilder-component-predicate-operand)" : String,
  "[Operator](#cfn-amplifyuibuilder-component-predicate-operator)" : String,
  "[Or](#cfn-amplifyuibuilder-component-predicate-or)" : [ Predicate, ... ]
}
```

### YAML<a name="aws-properties-amplifyuibuilder-component-predicate-syntax.yaml"></a>

```
  [And](#cfn-amplifyuibuilder-component-predicate-and): 
    - Predicate
  [Field](#cfn-amplifyuibuilder-component-predicate-field): String
  [Operand](#cfn-amplifyuibuilder-component-predicate-operand): String
  [Operator](#cfn-amplifyuibuilder-component-predicate-operator): String
  [Or](#cfn-amplifyuibuilder-component-predicate-or): 
    - Predicate
```

## Properties<a name="aws-properties-amplifyuibuilder-component-predicate-properties"></a>

`And`  <a name="cfn-amplifyuibuilder-component-predicate-and"></a>
A list of predicates to combine logically\.  
*Required*: No  
*Type*: List of [Predicate](#aws-properties-amplifyuibuilder-component-predicate)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Field`  <a name="cfn-amplifyuibuilder-component-predicate-field"></a>
The field to query\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Operand`  <a name="cfn-amplifyuibuilder-component-predicate-operand"></a>
The value to use when performing the evaluation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Operator`  <a name="cfn-amplifyuibuilder-component-predicate-operator"></a>
The operator to use to perform the evaluation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Or`  <a name="cfn-amplifyuibuilder-component-predicate-or"></a>
A list of predicates to combine logically\.  
*Required*: No  
*Type*: List of [Predicate](#aws-properties-amplifyuibuilder-component-predicate)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)