# AWS::ResourceExplorer2::Index<a name="aws-resource-resourceexplorer2-index"></a>

Turns on Resource Explorer in the AWS Region in which you called this operation by creating an index\. Resource Explorer begins discovering the resources in this Region and stores the details about the resources in the index so that they can be queried by using the [Search](https://docs.aws.amazon.com/resource-explorer/latest/APIReference/API_Search.html) operation\.

You can create either a local index that returns search results from only the AWS Region in which the index exists, or you can create an aggregator index that returns search results from all AWS Regions in the AWS account\.

For more details about what happens when you turn on Resource Explorer in an AWS Region, see [Turning on Resource Explorer to index your resources in an AWS Region](https://docs.aws.amazon.com/resource-explorer/latest/userguide/manage-service-activate.html) in the *AWS Resource Explorer User Guide\.*

If this is the first AWS Region in which you've created an index for Resource Explorer, this operation also creates a service\-linked role in your AWS account that allows Resource Explorer to search for your resources and populate the index\.

## Syntax<a name="aws-resource-resourceexplorer2-index-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-resourceexplorer2-index-syntax.json"></a>

```
{
  "Type" : "AWS::ResourceExplorer2::Index",
  "Properties" : {
      "[Tags](#cfn-resourceexplorer2-index-tags)" : {Key : Value, ...},
      "[Type](#cfn-resourceexplorer2-index-type)" : String
    }
}
```

### YAML<a name="aws-resource-resourceexplorer2-index-syntax.yaml"></a>

```
Type: AWS::ResourceExplorer2::Index
Properties: 
  [Tags](#cfn-resourceexplorer2-index-tags): 
    Key : Value
  [Type](#cfn-resourceexplorer2-index-type): String
```

## Properties<a name="aws-resource-resourceexplorer2-index-properties"></a>

`Tags`  <a name="cfn-resourceexplorer2-index-tags"></a>
The specified tags are attached to only the index created in this AWS Region\. The tags don't attach to any of the resources listed in the index\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-resourceexplorer2-index-type"></a>
Specifies the type of the index in this Region\. For information about the aggregator index and how it differs from a local index, see [Turning on cross\-Region search by creating an aggregator index](https://docs.aws.amazon.com/resource-explorer/latest/userguide/manage-aggregator-region.html) in the *AWS Resource Explorer User Guide\.*\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `AGGREGATOR | LOCAL`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-resourceexplorer2-index-return-values"></a>

### Ref<a name="aws-resource-resourceexplorer2-index-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ARN of the new index\. For example:

`arn:aws:resource-explorer-2:us-east-1:123456789012:index/EXAMPLE8-90ab-cdef-fedc-EXAMPLE22222`

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-resourceexplorer2-index-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-resourceexplorer2-index-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the new index for the AWS Region\. For example:  
`arn:aws:resource-explorer-2:us-east-1:123456789012:index/EXAMPLE8-90ab-cdef-fedc-EXAMPLE22222`

`IndexState`  <a name="IndexState-fn::getatt"></a>
Indicates the current state of the index\. For example:  
`CREATING`

## Examples<a name="aws-resource-resourceexplorer2-index--examples"></a>

### Turning on Resource Explorer in a Region by creating an index<a name="aws-resource-resourceexplorer2-index--examples--Turning_on_Resource_Explorer_in_a_Region_by_creating_an_index"></a>

#### JSON<a name="aws-resource-resourceexplorer2-index--examples--Turning_on_Resource_Explorer_in_a_Region_by_creating_an_index--json"></a>

```
{
    "Description": "Sample stack template that creates a Resource Explorer aggregator index",
    "Resources": {
        "SampleIndex": {
            "Type": "AWS::ResourceExplorer2::Index",
            "Properties": {
                "Type": "AGGREGATOR",
                "Tags": {
                    "Purpose": "ResourceExplorer Sample Stack"
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-resourceexplorer2-index--examples--Turning_on_Resource_Explorer_in_a_Region_by_creating_an_index--yaml"></a>

```
AWSTemplateFormatVersion: "2010-09-09"
Description: A sample template that creates a Resource Explorer aggregator index
Resources:
  SampleIndex:
    Type: 'AWS::ResourceExplorer2::Index'
    Properties:
      Type: AGGREGATOR
      Tags:
        Purpose: ResourceExplorer Sample Stack
```