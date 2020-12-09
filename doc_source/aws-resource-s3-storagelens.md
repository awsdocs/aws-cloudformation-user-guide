# AWS::S3::StorageLens<a name="aws-resource-s3-storagelens"></a>

The AWS::S3::StorageLens resource creates an instance of an Amazon S3 Storage Lens configuration\.

## Syntax<a name="aws-resource-s3-storagelens-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-s3-storagelens-syntax.json"></a>

```
{
  "Type" : "AWS::S3::StorageLens",
  "Properties" : {
      "[StorageLensConfiguration](#cfn-s3-storagelens-storagelensconfiguration)" : StorageLensConfiguration,
      "[Tags](#cfn-s3-storagelens-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-s3-storagelens-syntax.yaml"></a>

```
Type: AWS::S3::StorageLens
Properties: 
  [StorageLensConfiguration](#cfn-s3-storagelens-storagelensconfiguration): 
    StorageLensConfiguration
  [Tags](#cfn-s3-storagelens-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-s3-storagelens-properties"></a>

`StorageLensConfiguration`  <a name="cfn-s3-storagelens-storagelensconfiguration"></a>
This resource contains the details Amazon S3 Storage Lens configuration\.  
*Required*: Yes  
*Type*: [StorageLensConfiguration](aws-properties-s3-storagelens-storagelensconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-s3-storagelens-tags"></a>
A set of tags \(key–value pairs\) to associate with the Storage Lens configuration\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-s3-storagelens-return-values"></a>

### Ref<a name="aws-resource-s3-storagelens-return-values-ref"></a>

When the logical ID of this resource is provided to the Ref intrinsic function, Ref returns the S3 Storage Lens configuration Id, such as `your-storage-lens-configuration-id`\. For more information about using the Ref function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-s3-storagelens-return-values-fn--getatt"></a>

Fn::GetAtt returns a value for a specified attribute of this type\. For more information, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\. The following are the available attributes and sample return values\.

#### <a name="aws-resource-s3-storagelens-return-values-fn--getatt-fn--getatt"></a>

`StorageLensArn`  <a name="StorageLensArn-fn::getatt"></a>
This resource contains the details of the S3 Storage Lens ARN\. This resource is read\-only\.