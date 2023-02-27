# AWS::FSx::Snapshot<a name="aws-resource-fsx-snapshot"></a>

A snapshot of an Amazon FSx for OpenZFS volume\.

## Syntax<a name="aws-resource-fsx-snapshot-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-fsx-snapshot-syntax.json"></a>

```
{
  "Type" : "AWS::FSx::Snapshot",
  "Properties" : {
      "[Name](#cfn-fsx-snapshot-name)" : String,
      "[Tags](#cfn-fsx-snapshot-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VolumeId](#cfn-fsx-snapshot-volumeid)" : String
    }
}
```

### YAML<a name="aws-resource-fsx-snapshot-syntax.yaml"></a>

```
Type: AWS::FSx::Snapshot
Properties: 
  [Name](#cfn-fsx-snapshot-name): String
  [Tags](#cfn-fsx-snapshot-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VolumeId](#cfn-fsx-snapshot-volumeid): String
```

## Properties<a name="aws-resource-fsx-snapshot-properties"></a>

`Name`  <a name="cfn-fsx-snapshot-name"></a>
The name of the snapshot\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `203`  
*Pattern*: `^[a-zA-Z0-9_:.-]{1,203}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-fsx-snapshot-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VolumeId`  <a name="cfn-fsx-snapshot-volumeid"></a>
The ID of the volume that the snapshot is of\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `23`  
*Maximum*: `23`  
*Pattern*: `^(fsvol-[0-9a-f]{17,})$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-fsx-snapshot-return-values"></a>

### Ref<a name="aws-resource-fsx-snapshot-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the snapshot\. For example:

`{"Ref":"logical_snapshot_id"}`

Returns `fsvolsnap-0123456789abcedf5`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-fsx-snapshot-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-fsx-snapshot-return-values-fn--getatt-fn--getatt"></a>

`ResourceARN`  <a name="ResourceARN-fn::getatt"></a>
Returns the snapshot's Amazon Resource Name \(ARN\)\.  
Example: `arn:aws:fsx:us-east-2:111133334444:snapshot/fsvol-01234567890123456/fsvolsnap-0123456789abcedf5`