# AWS::IoTFleetWise::SignalCatalog Branch<a name="aws-properties-iotfleetwise-signalcatalog-branch"></a>

A group of signals that are defined in a hierarchical structure\.

## Syntax<a name="aws-properties-iotfleetwise-signalcatalog-branch-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotfleetwise-signalcatalog-branch-syntax.json"></a>

```
{
  "[Description](#cfn-iotfleetwise-signalcatalog-branch-description)" : String,
  "[FullyQualifiedName](#cfn-iotfleetwise-signalcatalog-branch-fullyqualifiedname)" : String
}
```

### YAML<a name="aws-properties-iotfleetwise-signalcatalog-branch-syntax.yaml"></a>

```
  [Description](#cfn-iotfleetwise-signalcatalog-branch-description): String
  [FullyQualifiedName](#cfn-iotfleetwise-signalcatalog-branch-fullyqualifiedname): String
```

## Properties<a name="aws-properties-iotfleetwise-signalcatalog-branch-properties"></a>

`Description`  <a name="cfn-iotfleetwise-signalcatalog-branch-description"></a>
A brief description of the branch\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `[^\u0000-\u001F\u007F]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FullyQualifiedName`  <a name="cfn-iotfleetwise-signalcatalog-branch-fullyqualifiedname"></a>
The fully qualified name of the branch\. For example, the fully qualified name of a branch might be `Vehicle.Body.Engine`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)