# AWS::DAX::ParameterGroup<a name="aws-resource-dax-parametergroup"></a>

Use the AWS CloudFormation `AWS::DAX::ParameterGroup` resource to create a parameter group for use with Amazon DynamoDB\.

For more information, see [http://docs.aws.amazon.com/amazondynamodb/latest/APIReference/API_dax_ParameterGroup.html](http://docs.aws.amazon.com/amazondynamodb/latest/APIReference/API_dax_ParameterGroup.html) in the *Amazon DynamoDB Developer Guide*\.

## Syntax<a name="aws-resource-dax-parametergroup-syntax"></a>

### JSON<a name="aws-resource-dax-parametergroup-syntax.json"></a>

```
{
   "Type": "AWS::DAX::ParameterGroup",
   "Properties": {
      "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dax-parametergroup-name)": String,
      "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dax-parametergroup-description)": String,
      "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dax-parametergroup-name-values)": { String:String, ... }
    }
}
```

### YAML<a name="aws-resource-dax-parametergroup-syntax.yaml"></a>

```
Type: "AWS::DAX::ParameterGroup"
Properties:
      [[ERROR] BAD/MISSING LINK TEXT](#cfn-dax-parametergroup-name): String
      [[ERROR] BAD/MISSING LINK TEXT](#cfn-dax-parametergroup-description): String
      [[ERROR] BAD/MISSING LINK TEXT](#cfn-dax-parametergroup-name-values): { String:String, ... }
```

## Properties<a name="aws-resource-dax-parametergroup-properties"></a>

`ParameterGroupName`  
The name of the parameter group\.  
*Required: *No  
*Type*: String  
*Update requires*: Updates are not supported\.

`Description`  
A description of the parameter group\.   
*Required: *No  
*Type*: String  
*Update requires*: No interruption;

`ParameterNameValues`  
A map of DAX parameter names and values\.  
*Required: *No  
*Type*: String to String map  
*Update requires*: No interruption

## Return Values<a name="aws-resource-dax-parametergroup-returnvalues"></a>

### Ref<a name="w3ab2c21c10d294c11b2"></a>

When you provide the logical ID of this resource to the `Ref` intrinsic function, `Ref` returns the ARN of the created parameter group\. For example:

```
{ "Ref": "MyDAXParameterGroup" }
```

Returns a value similar to the following:

```
my-dax-parameter-group
```

For more information about using the `Ref` function, see Ref\.

### Fn::GetAtt<a name="w3ab2c21c10d294c11b4"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`ParameterGroupName`  
Returns the name of the parameter group\. For example:  

```
{ "Fn::GetAtt": ["MyDAXParameterGroup", "ParameterGroupName"] }
```
Returns a value similar to the following:  

```
mydaxparametergroup
```

For more information about using `Fn::GetAtt`, see Fn::GetAtt\.

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
        "ParameterGroupDescription": "Description for my DAX parameter group",
        "ParameterNameValues": {
          "query-ttl-millis": "75000",
          "record-ttl-millis": "88000"
        }
      }
    }
  },
  "Outputs": {
    "ParameterGroup": {
      "Value": "daxParamGroup"
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
      ParameterGroupDescription: "Description for my DAX parameter group" 
      ParameterNameValues:
         "query-ttl-millis" : "75000"
         "record-ttl-millis" : "88000"
Outputs:
  ParameterGroup:
    Value: !Ref daxParamGroup
```