# Resource Tag<a name="aws-properties-resource-tags"></a>

You can use the Resource Tags property to apply tags to resources, which can help you identify and categorize those resources\. You can tag only resources for which AWS CloudFormation supports tagging\. For information about which resources you can tag with AWS CloudFormation, see the individual resources in [AWS Resource and Property Types Reference](aws-template-resource-type-ref.md)\.

**Note**  
Tagging implementations might vary by resource\. For example, `AWS::AutoScaling::AutoScalingGroup` provides an additional, required `PropagateAtLaunch` property as part of its tagging scheme\.

In addition to any tags you define, AWS CloudFormation automatically creates the following stack\-level tags with the prefix `aws:`:
+ `aws:cloudformation:logical-id`
+ `aws:cloudformation:stack-id`
+ `aws:cloudformation:stack-name`

The `aws:` prefix is reserved for AWS use\. This prefix is case\-insensitive\. If you use this prefix in the `Key` or `Value` property, you cannot update or delete the tag\. Tags with this prefix don't count toward the number of tags per resource\.

All stack\-level tags, including automatically created tags, are propagated to resources that AWS CloudFormation supports\. Currently, tags are not propagated to Amazon EBS volumes that are created from block device mappings\.

## Syntax<a name="w4429ab1c21c10d204c13c15"></a>

### JSON<a name="aws-properties-resource-tags-syntax.json"></a>

```
{
  "[Key](#cfn-resource-tags-key)" : String,
  "[Value](#cfn-resource-tags-value)" : String
}
```

### YAML<a name="aws-properties-resource-tags-syntax.yaml"></a>

```
[Key](#cfn-resource-tags-key): String
[Value](#cfn-resource-tags-value): String
```

## Properties<a name="w4429ab1c21c10d204c13c17"></a>

`Key`  <a name="cfn-resource-tags-key"></a>
The key name of the tag\. You can specify a value that is 1 to 127 Unicode characters in length and cannot be prefixed with `aws:`\. You can use any of the following characters: the set of Unicode letters, digits, whitespace, `_`, `.`, `/`, `=`, `+`, and `-`\.  
*Required*: Yes  
*Type*: String

`Value`  <a name="cfn-resource-tags-value"></a>
The value for the tag\. You can specify a value that is 1 to 255 Unicode characters in length and cannot be prefixed with `aws:`\. You can use any of the following characters: the set of Unicode letters, digits, whitespace, `_`, `.`, `/`, `=`, `+`, and `-`\.  
*Required*: Yes  
*Type*: String

## Example<a name="aws-properties-resource-tags-examples"></a>

This example shows a `Tags` property\. You specify this property within the `Properties` section of a resource that supports it\. When the resource is created, it is tagged with the tags you declare\.

### JSON<a name="aws-properties-resource-tags-example.json"></a>

```
 1. "Tags" : [
 2.    {
 3.       "Key" : "keyname1",
 4.       "Value" : "value1"
 5.    },
 6.    {
 7.       "Key" : "keyname2",
 8.       "Value" : "value2"
 9.    }
10. ]
```

### YAML<a name="aws-properties-resource-tags-example.yaml"></a>

```
1. Tags: 
2.   - 
3.     Key: "keyname1"
4.     Value: "value1"
5.   - 
6.     Key: "keyname2"
7.     Value: "value2"
```

## See Also<a name="w4429ab1c21c10d204c13c21"></a>
+ [Setting AWS CloudFormation Stack Options](cfn-console-add-tags.md)
+ [Viewing AWS CloudFormation Stack Data and Resources on the AWS Management Console](cfn-console-view-stack-data-resources.md)