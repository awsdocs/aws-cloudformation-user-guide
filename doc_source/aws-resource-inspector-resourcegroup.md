# AWS::Inspector::ResourceGroup<a name="aws-resource-inspector-resourcegroup"></a>

The `AWS::Inspector::ResourceGroup` resource is used to create Amazon Inspector resource groups\. A resource group defines a set of tags that, when queried, identify the AWS resources that make up the assessment target\.

**Topics**
+ [Syntax](#aws-resource-inspector-resourcegroup-syntax)
+ [Properties](#aws-resource-inspector-resourcegroup-properties)
+ [Return Values](#aws-resource-inspector-resourcegroup-returnvalues)
+ [Examples](#aws-resource-inspector-resourcegroup-examples)

## Syntax<a name="aws-resource-inspector-resourcegroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-inspector-resourcegroup-syntax.json"></a>

```
{
  "Type" : "AWS::Inspector::ResourceGroup",
  "Properties" : {
    "[ResourceGroupTags](#cfn-inspector-resourcegroup-resourcegrouptags)" : [ Resource Tag, ... ]
  }
}
```

### YAML<a name="aws-resource-inspector-resourcegroup-syntax.yaml"></a>

```
Type: "AWS::Inspector::ResourceGroup"
Properties:
  [ResourceGroupTags](#cfn-inspector-resourcegroup-resourcegrouptags): 
    - Resource Tag
```

## Properties<a name="aws-resource-inspector-resourcegroup-properties"></a>

`ResourceGroupTags`  <a name="cfn-inspector-resourcegroup-resourcegrouptags"></a>
The tags \(key and value pairs\) of the resource group\.  
 *Required*: Yes  
 *Type*: List of [AWS CloudFormation Resource Tags](aws-properties-resource-tags.md)  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## Return Values<a name="aws-resource-inspector-resourcegroup-returnvalues"></a>

### Fn::GetAtt<a name="aws-resource-inspector-resourcegroup-getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

`Arn`  
The Amazon Resource Name \(ARN\) that specifies the resource group that is created\. 

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\. 

## Examples<a name="aws-resource-inspector-resourcegroup-examples"></a>

### Declaring an Amazon Inspector Assessment Resource Group Resource<a name="aws-resource-inspector-resourcegroup-example1"></a>

The following example shows how to declare an AWS::Inspector::ResourceGroup resource to create an Amazon Inspector resource group\.

#### JSON<a name="aws-resource-inspector-resourcegroup-example1.json"></a>

```
"myresourcegroup": {
    "Type": "AWS: : Inspector: : ResourceGroup",
        "Properties": {
            "ResourceGroupTags": [
                {
                    "Key": "Name",
                    "Value": "example"
                }
            ]
        }
}
```

#### YAML<a name="aws-resource-inspector-resourcegroup-example1.yaml"></a>

```
myresourcegroup: 
  Type: "AWS::Inspector::ResourceGroup"
  Properties: 
    ResourceGroupTags : 
	  -
        Key: "Name"
        Value": "example"
```