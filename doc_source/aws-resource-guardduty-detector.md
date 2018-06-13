# AWS::GuardDuty::Detector<a name="aws-resource-guardduty-detector"></a>

The `AWS::GuardDuty::Detector` resource creates a single Amazon GuardDuty detector\. A detector is an object that represents the GuardDuty service\. You must create a detector for GuardDuty to become operational\. 

**Topics**
+ [Syntax](#aws-resource-guardduty-detector-syntax)
+ [Properties](#aws-resource-guardduty-detector-properties)
+ [Return Values](#aws-resource-guardduty-detector-returnvalues)
+ [Examples](#aws-resource-guardduty-detector-examples)

## Syntax<a name="aws-resource-guardduty-detector-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-guardduty-detector-syntax.json"></a>

```
{
  "Type" : "AWS::GuardDuty::Detector",
  "Properties" : {
    "[Enable](#cfn-guardduty-detector-enable)" : Boolean
  }
}
```

### YAML<a name="aws-resource-guardduty-detector-syntax.yaml"></a>

```
Type: "AWS::GuardDuty::Detector"
Properties:
  [Enable](#cfn-guardduty-detector-enable): Boolean
```

## Properties<a name="aws-resource-guardduty-detector-properties"></a>

`Enable`  <a name="cfn-guardduty-detector-enable"></a>
A Boolean value that specifies whether the detector is to be enabled\.  
 *Required*: Yes  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-guardduty-detector-returnvalues"></a>

### Ref<a name="aws-resource-guardduty-detector-ref"></a>

When you pass the logical ID of an `AWS::GuardDuty::Detector` resource to the intrinsic `Ref` function, the function returns the unique ID of the created detector\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

## Examples<a name="aws-resource-guardduty-detector-examples"></a>

### Declaring a GuardDuty Detector Resource<a name="aws-resource-guardduty-detector-example1"></a>

The following example shows how to declare an `AWS::GuardDuty::Detector` resource to create a GuardDuty detector\.

#### JSON<a name="aws-resource-guardduty-detector-example1.json"></a>

```
"mydetector": {
  "Type": "AWS::GuardDuty::Detector",
  "Properties": {
    "Enable": true
  }
}
```

#### YAML<a name="aws-resource-guardduty-detector-example1.yaml"></a>

```
mydetector:
  Type: "AWS::GuardDuty::Detector"
  Properties:
    Enable: true
```