# AWS::MemoryDB::ParameterGroup<a name="aws-resource-memorydb-parametergroup"></a>

Specifies a new MemoryDB parameter group\. A parameter group is a collection of parameters and their values that are applied to all of the nodes in any cluster\. For more information, see [Configuring engine parameters using parameter groups](https://docs.aws.amazon.com/memorydb/latest/devguide/parametergroups.html)\. 

## Syntax<a name="aws-resource-memorydb-parametergroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-memorydb-parametergroup-syntax.json"></a>

```
{
  "Type" : "AWS::MemoryDB::ParameterGroup",
  "Properties" : {
      "[Description](#cfn-memorydb-parametergroup-description)" : String,
      "[Family](#cfn-memorydb-parametergroup-family)" : String,
      "[ParameterGroupName](#cfn-memorydb-parametergroup-parametergroupname)" : String,
      "[Parameters](#cfn-memorydb-parametergroup-parameters)" : Json,
      "[Tags](#cfn-memorydb-parametergroup-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-memorydb-parametergroup-syntax.yaml"></a>

```
Type: AWS::MemoryDB::ParameterGroup
Properties: 
  [Description](#cfn-memorydb-parametergroup-description): String
  [Family](#cfn-memorydb-parametergroup-family): String
  [ParameterGroupName](#cfn-memorydb-parametergroup-parametergroupname): String
  [Parameters](#cfn-memorydb-parametergroup-parameters): Json
  [Tags](#cfn-memorydb-parametergroup-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-memorydb-parametergroup-properties"></a>

`Description`  <a name="cfn-memorydb-parametergroup-description"></a>
A description of the parameter group\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Family`  <a name="cfn-memorydb-parametergroup-family"></a>
The name of the parameter group family that this parameter group is compatible with\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ParameterGroupName`  <a name="cfn-memorydb-parametergroup-parametergroupname"></a>
The name of the parameter group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Parameters`  <a name="cfn-memorydb-parametergroup-parameters"></a>
Returns the detailed parameter list for the parameter group\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-memorydb-parametergroup-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-memorydb-parametergroup-return-values"></a>

### Fn::GetAtt<a name="aws-resource-memorydb-parametergroup-return-values-fn--getatt"></a>

#### <a name="aws-resource-memorydb-parametergroup-return-values-fn--getatt-fn--getatt"></a>

`ARN`  <a name="ARN-fn::getatt"></a>
When you pass the logical ID of this resource to the intrinsic `Ref` function, Ref returns the ARN of the parameter group, such as `arn:aws:memorydb:us-east-1:123456789012:parametergroup/my-parameter-group`