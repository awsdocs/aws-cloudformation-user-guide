# AWS::RDS::DBParameterGroup<a name="aws-properties-rds-dbparametergroup"></a>

Creates a custom parameter group for an RDS database family\. For more information about RDS parameter groups, see [Working with DB Parameter Groups](http://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_WorkingWithParamGroups.html) in the *Amazon Relational Database Service User Guide*\.

This type can be declared in a template and referenced in the `DBParameterGroupName` parameter of AWS::RDS::DBInstance\.

**Note**  
Applying a ParameterGroup to a DBInstance may require the instance to reboot, resulting in a database outage for the duration of the reboot\.


+ [Syntax](#aws-resource-rds-dbparametergroup-syntax)
+ [Properties](#w3ab2c21c10d890c13)
+ [Return Values](#w3ab2c21c10d890c15)
+ [Example](#w3ab2c21c10d890c17)

## Syntax<a name="aws-resource-rds-dbparametergroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-rds-dbparametergroup-syntax.json"></a>

```
{
   "Type" : "AWS::RDS::DBParameterGroup",
   "Properties" : {
      "Description" : String,
      "Family" : String,
      "Parameters" : DBParameters,
      "[[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbparametergroup-tags)" : [ Resource Tag, ... ]
   }
}
```

### YAML<a name="aws-resource-rds-dbparametergroup-syntax.yaml"></a>

```
Type: "AWS::RDS::DBParameterGroup"
Properties: 
  Description: String
  Family: String
  Parameters:
    DBParameters
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbparametergroup-tags):
    - Resource Tag
```

## Properties<a name="w3ab2c21c10d890c13"></a>

`Description`  
A friendly description of the RDS parameter group\. For example, `"My Parameter Group"`\.  
*Required: *Yes  
*Type:* String  
*Update requires*: Updates are not supported\.

`Family`  
The database family of this RDS parameter group\. For example, `"MySQL5.1"`\.  
*Required: *Yes  
*Type:* String  
*Update requires*: Updates are not supported\.

`Parameters`  
The parameters to set for this RDS parameter group\.  
*Required: *No  
*Type:* A JSON object consisting of string key\-value pairs, as shown in the following example:  

```
"Parameters" : {
   "Key1" : "Value1",
   "Key2" : "Value2",
   "Key3" : "Value3"
}
```
*Update requires*: No interruption or Some interruptions\. Changes to dynamic parameters are applied immediately\. During an update, if you have static parameters \(whether they were changed or not\), triggers AWS CloudFormation to reboot the associated DB instance without failover\.

`Tags`  
The tags that you want to attach to the RDS parameter group\.  
*Required: *No  
*Type*: A list of resource tags\.  
*Update requires*: No interruption

## Return Values<a name="w3ab2c21c10d890c15"></a>

### Ref<a name="w3ab2c21c10d890c15b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\. For example:

```
{ "Ref": "MyDBParameterGroup" }
```

For the RDS::DBParameterGroup with the logical ID "MyDBParameterGroup", `Ref` will return the resource name\.

For more information about using the `Ref` function, see Ref\.

## Example<a name="w3ab2c21c10d890c17"></a>

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