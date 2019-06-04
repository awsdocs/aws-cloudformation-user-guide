# AWS::AppMesh::Route TagRef<a name="aws-properties-appmesh-route-tagref"></a>

Optional metadata that you apply to a resource to assist with categorization and organization\. Each tag consists of a key and an optional value, both of which you define\. Tag keys can have a maximum character length of 128 characters, and tag values can have a maximum length of 256 characters\.

## Syntax<a name="aws-properties-appmesh-route-tagref-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-route-tagref-syntax.json"></a>

```
{
  "[Key](#cfn-appmesh-route-tagref-key)" : String,
  "[Value](#cfn-appmesh-route-tagref-value)" : String
}
```

### YAML<a name="aws-properties-appmesh-route-tagref-syntax.yaml"></a>

```
  [Key](#cfn-appmesh-route-tagref-key): String
  [Value](#cfn-appmesh-route-tagref-value): String
```

## Properties<a name="aws-properties-appmesh-route-tagref-properties"></a>

`Key`  <a name="cfn-appmesh-route-tagref-key"></a>
One part of a key\-value pair that make up a tag\. A `key` is a general label that acts like a category for more specific tag values\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-appmesh-route-tagref-value"></a>
The optional part of a key\-value pair that make up a tag\. A `value` acts as a descriptor within a tag category \(key\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)