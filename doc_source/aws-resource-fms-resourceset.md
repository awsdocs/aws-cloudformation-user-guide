# AWS::FMS::ResourceSet<a name="aws-resource-fms-resourceset"></a>

A set of resources to include in a policy\.

## Syntax<a name="aws-resource-fms-resourceset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-fms-resourceset-syntax.json"></a>

```
{
  "Type" : "AWS::FMS::ResourceSet",
  "Properties" : {
      "[Description](#cfn-fms-resourceset-description)" : String,
      "[Name](#cfn-fms-resourceset-name)" : String,
      "[Resources](#cfn-fms-resourceset-resources)" : [ String, ... ],
      "[ResourceTypeList](#cfn-fms-resourceset-resourcetypelist)" : [ String, ... ],
      "[Tags](#cfn-fms-resourceset-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-fms-resourceset-syntax.yaml"></a>

```
Type: AWS::FMS::ResourceSet
Properties: 
  [Description](#cfn-fms-resourceset-description): String
  [Name](#cfn-fms-resourceset-name): String
  [Resources](#cfn-fms-resourceset-resources): 
    - String
  [ResourceTypeList](#cfn-fms-resourceset-resourcetypelist): 
    - String
  [Tags](#cfn-fms-resourceset-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-fms-resourceset-properties"></a>

`Description`  <a name="cfn-fms-resourceset-description"></a>
A description of the resource set\.  
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `^([\p{L}\p{Z}\p{N}_.:/=+\-@]*)$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-fms-resourceset-name"></a>
The descriptive name of the resource set\. You can't change the name of a resource set after you create it\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `^([\p{L}\p{Z}\p{N}_.:/=+\-@]*)$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Resources`  <a name="cfn-fms-resourceset-resources"></a>
The resources included in the resource set\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceTypeList`  <a name="cfn-fms-resourceset-resourcetypelist"></a>
Determines the resources that can be associated to the resource set\. Depending on your setting for max results and the number of resource sets, a single call might not return the full list\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-fms-resourceset-tags"></a>
A collection of key:value pairs associated with a resource set\. The key:value pair can be anything you define\. Typically, the tag key represents a category \(such as "environment"\) and the tag value represents a specific value within that category \(such as "test," "development," or "production"\)\. You can add up to 50 tags to each AWS resource\.   
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-fms-resourceset-return-values"></a>

### Ref<a name="aws-resource-fms-resourceset-return-values-ref"></a>

The `Ref` for this resource returns the `ResourceSet.Id`\. 

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource physical ID, such as 1234a1a\-a1b1\-12a1\-abcd\-a123b123456\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-fms-resourceset-return-values-fn--getatt"></a>

#### <a name="aws-resource-fms-resourceset-return-values-fn--getatt-fn--getatt"></a>

`Id`  <a name="Id-fn::getatt"></a>
The ID of the resource set\.