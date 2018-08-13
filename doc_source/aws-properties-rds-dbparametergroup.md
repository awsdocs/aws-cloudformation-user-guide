# AWS::RDS::DBParameterGroup<a name="aws-properties-rds-dbparametergroup"></a>

Creates a custom parameter group for an RDS database family\. For more information about RDS parameter groups, see [Working with DB Parameter Groups](http://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_WorkingWithParamGroups.html) in the *Amazon Relational Database Service User Guide*\.

This type can be declared in a template and referenced in the `DBParameterGroupName` parameter of [AWS::RDS::DBInstance](aws-properties-rds-database-instance.md)\.

**Note**  
Applying a ParameterGroup to a DBInstance may require the instance to reboot, resulting in a database outage for the duration of the reboot\.

**Topics**
+ [Syntax](#aws-resource-rds-dbparametergroup-syntax)
+ [Properties](#w3ab2c21c10d962c13)
+ [Return Values](#w3ab2c21c10d962c15)
+ [Example](#w3ab2c21c10d962c17)

## Syntax<a name="aws-resource-rds-dbparametergroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-rds-dbparametergroup-syntax.json"></a>

```
{
   "Type" : "AWS::RDS::DBParameterGroup",
   "Properties" : {
      "[Description](#cfn-rds-dbparametergroup-description)" : String,
      "[Family](#cfn-rds-dbparametergroup-family)" : String,
      "[Parameters](#cfn-rds-dbparametergroup-parameters)" : DBParameters,
      "[Tags](#cfn-rds-dbparametergroup-tags)" : [ Resource Tag, ... ]
   }
}
```

### YAML<a name="aws-resource-rds-dbparametergroup-syntax.yaml"></a>

```
Type: "AWS::RDS::DBParameterGroup"
Properties: 
  [Description](#cfn-rds-dbparametergroup-description): String
  [Family](#cfn-rds-dbparametergroup-family): String
  [Parameters](#cfn-rds-dbparametergroup-parameters):
    DBParameters
  [Tags](#cfn-rds-dbparametergroup-tags):
    - Resource Tag
```

## Properties<a name="w3ab2c21c10d962c13"></a>

`Description`  <a name="cfn-rds-dbparametergroup-description"></a>
A friendly description of the RDS parameter group\. For example, `"My Parameter Group"`\.  
*Required*: Yes  
*Type:* String  
*Update requires*: Updates are not supported\.

`Family`  <a name="cfn-rds-dbparametergroup-family"></a>
The database family of this RDS parameter group\. For example, `"MySQL5.1"`\.  
*Required*: Yes  
*Type:* String  
*Update requires*: Updates are not supported\.

`Parameters`  <a name="cfn-rds-dbparametergroup-parameters"></a>
The parameters to set for this RDS parameter group\.  
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

`Tags`  <a name="cfn-rds-dbparametergroup-tags"></a>
The tags that you want to attach to the RDS parameter group\.  
*Required*: No  
*Type*: A list of [resource tags](aws-properties-resource-tags.md)\.  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Values<a name="w3ab2c21c10d962c15"></a>

### Ref<a name="w3ab2c21c10d962c15b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\. For example:

```
{ "Ref": "MyDBParameterGroup" }
```

For the RDS::DBParameterGroup with the logical ID "MyDBParameterGroup", `Ref` will return the resource name\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="w3ab2c21c10d962c17"></a>

The following snippet creates a parameter group for an Aurora DB cluster that applies the `IGNORE_SPACE` SQL mode\.

### JSON<a name="aws-resource-rds-dbparametergroup-example.json"></a>

```
"RDSDBParameterGroup": {
  "Type": "AWS::RDS::DBParameterGroup",
  "Properties" : {
    "Description" : "CloudFormation Sample Parameter Group",
    "Family" : "aurora5.6",
    "Parameters" : {
      "sql_mode": "IGNORE_SPACE"
    }
  }
}
```

### YAML<a name="aws-resource-rds-dbparametergroup-example.yaml"></a>

```
RDSDBParameterGroup:
  Type: AWS::RDS::DBParameterGroup
  Properties:
    Description: CloudFormation Sample Parameter Group
    Family: aurora5.6
    Parameters:
      sql_mode: IGNORE_SPACE
```