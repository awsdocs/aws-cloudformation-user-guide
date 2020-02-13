# AWS::Transfer::User HomeDirectoryMapEntry<a name="aws-properties-transfer-user-homedirectorymapentry"></a>

Represents an object that contains entries and a targets for `HomeDirectoryMappings`\.

## Syntax<a name="aws-properties-transfer-user-homedirectorymapentry-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-transfer-user-homedirectorymapentry-syntax.json"></a>

```
{
  "[Entry](#cfn-transfer-user-homedirectorymapentry-entry)" : String,
  "[Target](#cfn-transfer-user-homedirectorymapentry-target)" : String
}
```

### YAML<a name="aws-properties-transfer-user-homedirectorymapentry-syntax.yaml"></a>

```
  [Entry](#cfn-transfer-user-homedirectorymapentry-entry): String
  [Target](#cfn-transfer-user-homedirectorymapentry-target): String
```

## Properties<a name="aws-properties-transfer-user-homedirectorymapentry-properties"></a>

`Entry`  <a name="cfn-transfer-user-homedirectorymapentry-entry"></a>
Represents an entry and a target for `HomeDirectoryMappings`\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `1024`  
*Pattern*: `^/.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Target`  <a name="cfn-transfer-user-homedirectorymapentry-target"></a>
Represents the map target that is used in a `HomeDirectorymapEntry`\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `1024`  
*Pattern*: `^/.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)