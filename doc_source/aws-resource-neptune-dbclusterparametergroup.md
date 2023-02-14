# AWS::Neptune::DBClusterParameterGroup<a name="aws-resource-neptune-dbclusterparametergroup"></a>

The `AWS::Neptune::DBClusterParameterGroup` resource creates a new Amazon Neptune DB cluster parameter group\.

**Note**  
Applying a parameter group to a DB cluster might require instances to reboot, resulting in a database outage while the instances reboot\.

## Syntax<a name="aws-resource-neptune-dbclusterparametergroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-neptune-dbclusterparametergroup-syntax.json"></a>

```
{
  "Type" : "AWS::Neptune::DBClusterParameterGroup",
  "Properties" : {
      "[Description](#cfn-neptune-dbclusterparametergroup-description)" : String,
      "[Family](#cfn-neptune-dbclusterparametergroup-family)" : String,
      "[Name](#cfn-neptune-dbclusterparametergroup-name)" : String,
      "[Parameters](#cfn-neptune-dbclusterparametergroup-parameters)" : Json,
      "[Tags](#cfn-neptune-dbclusterparametergroup-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-neptune-dbclusterparametergroup-syntax.yaml"></a>

```
Type: AWS::Neptune::DBClusterParameterGroup
Properties: 
  [Description](#cfn-neptune-dbclusterparametergroup-description): String
  [Family](#cfn-neptune-dbclusterparametergroup-family): String
  [Name](#cfn-neptune-dbclusterparametergroup-name): String
  [Parameters](#cfn-neptune-dbclusterparametergroup-parameters): Json
  [Tags](#cfn-neptune-dbclusterparametergroup-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-neptune-dbclusterparametergroup-properties"></a>

`Description`  <a name="cfn-neptune-dbclusterparametergroup-description"></a>
Provides the customer\-specified description for this DB cluster parameter group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Family`  <a name="cfn-neptune-dbclusterparametergroup-family"></a>
Must be `neptune1`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-neptune-dbclusterparametergroup-name"></a>
Provides the name of the DB cluster parameter group\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Parameters`  <a name="cfn-neptune-dbclusterparametergroup-parameters"></a>
The parameters to set for this DB cluster parameter group\.  
The parameters are expressed as a JSON object consisting of key\-value pairs\.  
If you update the parameters, some interruption may occur depending on which parameters you update\.  
*Required*: Yes  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-neptune-dbclusterparametergroup-tags"></a>
The tags that you want to attach to this parameter group\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-neptune-dbclusterparametergroup-return-values"></a>

### Ref<a name="aws-resource-neptune-dbclusterparametergroup-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.