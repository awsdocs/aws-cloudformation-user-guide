# AWS::DAX::ParameterGroup<a name="aws-resource-dax-parametergroup"></a>

Use the AWS CloudFormation `AWS::DAX::ParameterGroup` resource to create a parameter group for use with Amazon DynamoDB\.

For more information, see [https://docs.aws.amazon.com/amazondynamodb/latest/APIReference/API_dax_ParameterGroup.html](https://docs.aws.amazon.com/amazondynamodb/latest/APIReference/API_dax_ParameterGroup.html) in the *Amazon DynamoDB Developer Guide*\.

## Syntax<a name="aws-resource-dax-parametergroup-syntax"></a>

### JSON<a name="aws-resource-dax-parametergroup-syntax.json"></a>

```
{
   "Type": "AWS::DAX::ParameterGroup",
   "Properties": {
      "[ParameterGroupName](#cfn-dax-parametergroup-name)": String,
      "[Description](#cfn-dax-parametergroup-description)": String,
      "[ParameterNameValues](#cfn-dax-parametergroup-name-values)": { String:String, ... }
    }
}
```

### YAML<a name="aws-resource-dax-parametergroup-syntax.yaml"></a>

```
Type: AWS::DAX::ParameterGroup
Properties:
      [ParameterGroupName](#cfn-dax-parametergroup-name): String
      [Description](#cfn-dax-parametergroup-description): String
      [ParameterNameValues](#cfn-dax-parametergroup-name-values): { String:String, ... }
```

## Properties<a name="aws-resource-dax-parametergroup-properties"></a>

`ParameterGroupName`  <a name="cfn-dax-parametergroup-name"></a>
The name of the parameter group\.  
*Required*: No  
*Type*: String  
*Update requires*: Updates are not supported\.

`Description`  <a name="cfn-dax-parametergroup-description"></a>
A description of the parameter group\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt);

`ParameterNameValues`  <a name="cfn-dax-parametergroup-name-values"></a>
A map of DAX parameter names and values\.  
*Required*: No  
*Type*: String to String map  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Values<a name="aws-resource-dax-parametergroup-returnvalues"></a>

### Ref<a name="w13ab1c21c10c93c19c11b2"></a>

When you provide the logical ID of this resource to the `Ref` intrinsic function, `Ref` returns the ARN of the created parameter group\. For example:

```
{ "Ref": "MyDAXParameterGroup" }
```

Returns a value similar to the following:

```
my-dax-parameter-group
```

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="aws-resource-dax-parametergroup-examples"></a>

The following example creates a DAX parameter group\.

### JSON<a name="aws-resource-dax-parametergroup-example.json"></a>

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

### YAML<a name="aws-resource-dax-cluster-parametergroup.yaml"></a>

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