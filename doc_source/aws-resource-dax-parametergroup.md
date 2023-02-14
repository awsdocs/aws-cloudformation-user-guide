# AWS::DAX::ParameterGroup<a name="aws-resource-dax-parametergroup"></a>

A named set of parameters that are applied to all of the nodes in a DAX cluster\.

## Syntax<a name="aws-resource-dax-parametergroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-dax-parametergroup-syntax.json"></a>

```
{
  "Type" : "AWS::DAX::ParameterGroup",
  "Properties" : {
      "[Description](#cfn-dax-parametergroup-description)" : String,
      "[ParameterGroupName](#cfn-dax-parametergroup-parametergroupname)" : String,
      "[ParameterNameValues](#cfn-dax-parametergroup-parameternamevalues)" : Json
    }
}
```

### YAML<a name="aws-resource-dax-parametergroup-syntax.yaml"></a>

```
Type: AWS::DAX::ParameterGroup
Properties: 
  [Description](#cfn-dax-parametergroup-description): String
  [ParameterGroupName](#cfn-dax-parametergroup-parametergroupname): String
  [ParameterNameValues](#cfn-dax-parametergroup-parameternamevalues): Json
```

## Properties<a name="aws-resource-dax-parametergroup-properties"></a>

`Description`  <a name="cfn-dax-parametergroup-description"></a>
A description of the parameter group\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ParameterGroupName`  <a name="cfn-dax-parametergroup-parametergroupname"></a>
The name of the parameter group\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ParameterNameValues`  <a name="cfn-dax-parametergroup-parameternamevalues"></a>
An array of name\-value pairs for the parameters in the group\. Each element in the array represents a single parameter\.  
 `record-ttl-millis` and `query-ttl-millis` are the only supported parameter names\. For more details, see [Configuring TTL Settings](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/DAX.cluster-management.html#DAX.cluster-management.custom-settings.ttl)\.
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-dax-parametergroup-return-values"></a>

### Ref<a name="aws-resource-dax-parametergroup-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the created parameter group\. For example: 

```
{ "Ref": "MyDAXParameterGroup" }
```

Returns a value similar to the following:

```
my-dax-parameter-group
```

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-dax-parametergroup--examples"></a>

### Create Parameter Group<a name="aws-resource-dax-parametergroup--examples--Create__Parameter_Group"></a>

The following example creates a DAX parameter group\.

#### JSON<a name="aws-resource-dax-parametergroup--examples--Create__Parameter_Group--json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Description": "DAX parameter group",
  "Resources": {
    "daxParamGroup": {
      "Type": "AWS::DAX::ParameterGroup",
      "Properties": {
        "ParameterGroupName": "MyDAXParameterGroup",
        "Description": "Description for my DAX parameter group",
        "ParameterNameValues": {
          "query-ttl-millis": "75000",
          "record-ttl-millis": "88000"
        }
      }
    }
  },
  "Outputs": {
    "ParameterGroup": {
      "Value": {
        "Ref": "daxParamGroup"
      }
    }
  }
}
```

#### YAML<a name="aws-resource-dax-parametergroup--examples--Create__Parameter_Group--yaml"></a>

```
AWSTemplateFormatVersion: "2010-09-09"
Description: "DAX parameter group"
Resources:
  daxParamGroup:
    Type: AWS::DAX::ParameterGroup
    Properties:
      ParameterGroupName: "MyDAXParameterGroup" 
      Description: "Description for my DAX parameter group" 
      ParameterNameValues:
         "query-ttl-millis" : "75000"
         "record-ttl-millis" : "88000"
Outputs:
  ParameterGroup:
    Value: !Ref daxParamGroup
```