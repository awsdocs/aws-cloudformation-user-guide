# AWS::Neptune::DBClusterParameterGroup<a name="aws-resource-neptune-dbclusterparametergroup"></a>

The `AWS::Neptune::DBClusterParameterGroup` resource creates a new Amazon Neptune DB cluster parameter group\.

**Note**  
Applying a parameter group to a DB cluster might require instances to reboot, resulting in a database outage while the instances reboot\.

**Topics**
+ [Syntax](#aws-resource-neptune-dbclusterparametergroup-syntax)
+ [Properties](#w3ab2c21c10d892c11)
+ [Return Values](#w3ab2c21c10d892c13)

## Syntax<a name="aws-resource-neptune-dbclusterparametergroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-neptune-dbclusterparametergroup-syntax.json"></a>

```
{
  "Type" : "AWS::Neptune::DBClusterParameterGroup",
  "Properties" : {
    "[Description](#cfn-neptune-dbclusterparametergroup-description)" : String,
    "[Parameters](#cfn-neptune-dbclusterparametergroup-parameters)" : DBParameters,
    "[Family](#cfn-neptune-dbclusterparametergroup-family)" : String,
    "[Tags](#cfn-neptune-dbclusterparametergroup-tags)" : [ Resource Tag, ... ],
    "[Name](#cfn-neptune-dbclusterparametergroup-name)" : String
  }
}
```

### YAML<a name="aws-resource-neptune-dbclusterparametergroup-syntax.yaml"></a>

```
Type: "AWS::Neptune::DBClusterParameterGroup"
Properties: 
  [Description](#cfn-neptune-dbclusterparametergroup-description): String
  [Parameters](#cfn-neptune-dbclusterparametergroup-parameters): DBParameters
  [Family](#cfn-neptune-dbclusterparametergroup-family) : String
  [Tags](#cfn-neptune-dbclusterparametergroup-tags):
    Resource Tag 
  [Name](#cfn-neptune-dbclusterparametergroup-name) : String
```

## Properties<a name="w3ab2c21c10d892c11"></a>

`Description`  <a name="cfn-neptune-dbclusterparametergroup-description"></a>
A friendly description for this DB cluster parameter group\.  
*Required*: Yes  
*Type:* String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Parameters`  <a name="cfn-neptune-dbclusterparametergroup-parameters"></a>
The parameters to set for this DB cluster parameter group\.   
Changes to dynamic parameters are applied immediately\. Changes to static parameters require a reboot without failover to the DB instance that is associated with the parameter group before the change can take effect\.  
*Required*: Yes  
*Type:* A JSON object consisting of string key\-value pairs, as shown in the following example:  

```
"Parameters" : {
   "Key1" : "Value1",
   "Key2" : "Value2",
   "Key3" : "Value3"
}
```
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) or [some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt), depending on the parameters that you update\.

`Family`  <a name="cfn-neptune-dbclusterparametergroup-family"></a>
Must be `neptune1`\.  
*Required*: Yes  
*Type:* String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Tags`  <a name="cfn-neptune-dbclusterparametergroup-tags"></a>
The tags that you want to attach to this parameter group\.  
*Required*: No  
*Type*: A list of [resource tags](aws-properties-resource-tags.md)  
*Update requires*: Updates are not supported\.

`Name`  <a name="cfn-neptune-dbclusterparametergroup-name"></a>
A friendly name for the cluster\.  
*Required*: No  
*Type:* String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Values<a name="w3ab2c21c10d892c13"></a>

### Ref<a name="w3ab2c21c10d892c13b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.