# AWS::Rekognition::Collection<a name="aws-resource-rekognition-collection"></a>

The `AWS::Rekognition::Collection` type creates a server\-side container called a collection\. You can use a collection to store information about detected faces and search for known faces in images, stored videos, and streaming videos\.

## Syntax<a name="aws-resource-rekognition-collection-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-rekognition-collection-syntax.json"></a>

```
{
  "Type" : "AWS::Rekognition::Collection",
  "Properties" : {
      "[CollectionId](#cfn-rekognition-collection-collectionid)" : String,
      "[Tags](#cfn-rekognition-collection-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-rekognition-collection-syntax.yaml"></a>

```
Type: AWS::Rekognition::Collection
Properties: 
  [CollectionId](#cfn-rekognition-collection-collectionid): String
  [Tags](#cfn-rekognition-collection-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-rekognition-collection-properties"></a>

`CollectionId`  <a name="cfn-rekognition-collection-collectionid"></a>
ID for the collection that you are creating\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `[a-zA-Z0-9_.\-]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-rekognition-collection-tags"></a>
 A set of tags \(key\-value pairs\) that you want to attach to the collection\.   
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-rekognition-collection-return-values"></a>

### Ref<a name="aws-resource-rekognition-collection-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the collection ID\. For example: 

 `{ "Ref": "MyCollection" }` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-rekognition-collection-return-values-fn--getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. For more information about using `Fn::GetAtt`, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\. 

#### <a name="aws-resource-rekognition-collection-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Returns the Amazon Resource Name of the collection\.