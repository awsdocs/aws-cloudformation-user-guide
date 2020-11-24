# AWS::S3::StorageLens SelectionCriteria<a name="aws-properties-s3-storagelens-selectioncriteria"></a>

This resource contains the details of the Amazon S3 Storage Lens selection criteria\.

## Syntax<a name="aws-properties-s3-storagelens-selectioncriteria-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-storagelens-selectioncriteria-syntax.json"></a>

```
{
  "[Delimiter](#cfn-s3-storagelens-selectioncriteria-delimiter)" : String,
  "[MaxDepth](#cfn-s3-storagelens-selectioncriteria-maxdepth)" : Integer,
  "[MinStorageBytesPercentage](#cfn-s3-storagelens-selectioncriteria-minstoragebytespercentage)" : Double
}
```

### YAML<a name="aws-properties-s3-storagelens-selectioncriteria-syntax.yaml"></a>

```
  [Delimiter](#cfn-s3-storagelens-selectioncriteria-delimiter): String
  [MaxDepth](#cfn-s3-storagelens-selectioncriteria-maxdepth): Integer
  [MinStorageBytesPercentage](#cfn-s3-storagelens-selectioncriteria-minstoragebytespercentage): Double
```

## Properties<a name="aws-properties-s3-storagelens-selectioncriteria-properties"></a>

`Delimiter`  <a name="cfn-s3-storagelens-selectioncriteria-delimiter"></a>
This property contains the details of the S3 Storage Lens delimiter being used\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxDepth`  <a name="cfn-s3-storagelens-selectioncriteria-maxdepth"></a>
This property contains the details of the max depth that S3 Storage Lens will collect metrics up to\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinStorageBytesPercentage`  <a name="cfn-s3-storagelens-selectioncriteria-minstoragebytespercentage"></a>
This property contains the details of the minimum storage bytes percentage threshold that S3 Storage Lens will collect metrics up to\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)