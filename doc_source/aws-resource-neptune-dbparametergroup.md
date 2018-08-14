# AWS::Neptune::DBParameterGroup<a name="aws-resource-neptune-dbparametergroup"></a>

Creates a custom parameter group for DB instances\. 

This type can be declared in a template and referenced in the `DBParameterGroupName` parameter of [AWS::Neptune::DBInstance](aws-resource-neptune-dbinstance.md)\.

**Note**  
Applying a ParameterGroup to a DBInstance may require the instance to reboot, resulting in a database outage for the duration of the reboot\.

**Topics**
+ [Syntax](#aws-resource-neptune-dbparametergroup-syntax)
+ [Properties](#w3ab2c21c10d902c13)
+ [Return Values](#w3ab2c21c10d902c15)

## Syntax<a name="aws-resource-neptune-dbparametergroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-neptune-dbparametergroup-syntax.json"></a>

```
{
   "Type" : "AWS::Neptune::DBParameterGroup",
   "Properties" : {
      "[Description](#cfn-neptune-dbparametergroup-description)" : String,
      "[Parameters](#cfn-neptune-dbparametergroup-parameters)" : DBParameters,
      "[Family](#cfn-neptune-dbparametergroup-family)" : String,
      "[Tags](#cfn-neptune-dbparametergroup-tags)" : [ Resource Tag, ... ],
      "[Name](#cfn-neptune-dbparametergroup-name)" : String
   }
}
```

### YAML<a name="aws-resource-neptune-dbparametergroup-syntax.yaml"></a>

```
Type: "AWS::Neptune::DBParameterGroup"
Properties: 
  [Description](#cfn-neptune-dbparametergroup-description): String
  [Parameters](#cfn-neptune-dbparametergroup-parameters):
    DBParameters
  [Family](#cfn-neptune-dbparametergroup-family) : String
  [Tags](#cfn-neptune-dbparametergroup-tags):
    - Resource Tag 
  [Name](#cfn-neptune-dbparametergroup-name) : String
```

## Properties<a name="w3ab2c21c10d902c13"></a>

`Description`  <a name="cfn-neptune-dbparametergroup-description"></a>
A friendly description of the DB parameter group\. For example, `"My Parameter Group"`\.  
*Required*: Yes  
*Type:* String  
*Update requires*: Updates are not supported\.

`Parameters`  <a name="cfn-neptune-dbparametergroup-parameters"></a>
The parameters to set for this DB parameter group\.  
*Required*: No  
*Type:* A JSON object consisting of string key\-value pairs, as shown in the following example:  

```
"Parameters" : {
   "Key1" : "Value1",
   "Key2" : "Value2",
   "Key3" : "Value3"
}
```
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) or [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)\. Changes to dynamic parameters are applied immediately\. During an update, if you have static parameters \(whether they were changed or not\), triggers AWS CloudFormation to reboot the associated DB instance without failover\.

`Family`  <a name="cfn-neptune-dbparametergroup-family"></a>
Must be `neptune1`\.  
*Required*: Yes  
*Type:* String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Tags`  <a name="cfn-neptune-dbparametergroup-tags"></a>
The tags that you want to attach to the DB parameter group\.  
*Required*: No  
*Type*: A list of [resource tags](aws-properties-resource-tags.md)\.  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Name`  <a name="cfn-neptune-dbparametergroup-name"></a>
A friendly name for the cluster\.  
*Required*: No  
*Type:* String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Values<a name="w3ab2c21c10d902c15"></a>

### Ref<a name="w3ab2c21c10d902c15b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\. For example:

```
{ "Ref": "MyDBParameterGroup" }
```

For the RDS::DBParameterGroup with the logical ID "MyDBParameterGroup", `Ref` will return the resource name\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.