# AWS::Inspector::ResourceGroup<a name="aws-resource-inspector-resourcegroup"></a>

The `AWS::Inspector::ResourceGroup` resource is used to create Amazon Inspector resource groups\. A resource group defines a set of tags that, when queried, identify the AWS resources that make up the assessment target\.

## Syntax<a name="aws-resource-inspector-resourcegroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-inspector-resourcegroup-syntax.json"></a>

```
{
  "Type" : "AWS::Inspector::ResourceGroup",
  "Properties" : {
      "[ResourceGroupTags](#cfn-inspector-resourcegroup-resourcegrouptags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-inspector-resourcegroup-syntax.yaml"></a>

```
Type: AWS::Inspector::ResourceGroup
Properties: 
  [ResourceGroupTags](#cfn-inspector-resourcegroup-resourcegrouptags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-inspector-resourcegroup-properties"></a>

`ResourceGroupTags`  <a name="cfn-inspector-resourcegroup-resourcegrouptags"></a>
The tags \(key and value pairs\) that will be associated with the resource group\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: Yes  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `10`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-inspector-resourcegroup-return-values"></a>

### Ref<a name="aws-resource-inspector-resourcegroup-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ARN of the new resource group\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-inspector-resourcegroup-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-inspector-resourcegroup-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) that specifies the resource group that is created\.

## Examples<a name="aws-resource-inspector-resourcegroup--examples"></a>



### Declaring an Amazon Inspector Resource Group Resource<a name="aws-resource-inspector-resourcegroup--examples--Declaring_an_Amazon_Inspector_Resource_Group_Resource"></a>

The following example shows how to declare an `AWS::Inspector::ResourceGroup` resource to create an Amazon Inspector resource group\.

#### JSON<a name="aws-resource-inspector-resourcegroup--examples--Declaring_an_Amazon_Inspector_Resource_Group_Resource--json"></a>

```
"myresourcegroup": {
  "Type": "AWS::Inspector::ResourceGroup",
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

#### YAML<a name="aws-resource-inspector-resourcegroup--examples--Declaring_an_Amazon_Inspector_Resource_Group_Resource--yaml"></a>

```
myresourcegroup: 
  Type: "AWS::Inspector::ResourceGroup"
  Properties: 
    ResourceGroupTags: 
      - Key: "Name"
      Value: "example"
```