# AWS::FraudDetector::EntityType<a name="aws-resource-frauddetector-entitytype"></a>

Manages an entity type\. An entity represents who is performing the event\. As part of a fraud prediction, you pass the entity ID to indicate the specific entity who performed the event\. An entity type classifies the entity\. Example classifications include customer, merchant, or account\.

## Syntax<a name="aws-resource-frauddetector-entitytype-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-frauddetector-entitytype-syntax.json"></a>

```
{
  "Type" : "AWS::FraudDetector::EntityType",
  "Properties" : {
      "[Description](#cfn-frauddetector-entitytype-description)" : String,
      "[Name](#cfn-frauddetector-entitytype-name)" : String,
      "[Tags](#cfn-frauddetector-entitytype-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-frauddetector-entitytype-syntax.yaml"></a>

```
Type: AWS::FraudDetector::EntityType
Properties: 
  [Description](#cfn-frauddetector-entitytype-description): String
  [Name](#cfn-frauddetector-entitytype-name): String
  [Tags](#cfn-frauddetector-entitytype-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-frauddetector-entitytype-properties"></a>

`Description`  <a name="cfn-frauddetector-entitytype-description"></a>
The entity type description\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-frauddetector-entitytype-name"></a>
The entity type name\.  
Pattern: `^[0-9a-z_-]+$`  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-frauddetector-entitytype-tags"></a>
A key and value pair\.   
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-frauddetector-entitytype-return-values"></a>

### Ref<a name="aws-resource-frauddetector-entitytype-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the primary identifier for the resource, which is the ARN\.

Example: `{ "Ref": "arn:aws:frauddetector:us-west-2:123123123123:outcome/outcome_name"}`

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-frauddetector-entitytype-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-frauddetector-entitytype-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The entity type ARN\.

`CreatedTime`  <a name="CreatedTime-fn::getatt"></a>
Timestamp of when entity type was created\.

`LastUpdatedTime`  <a name="LastUpdatedTime-fn::getatt"></a>
Timestamp of when entity type was last updated\.

## See also<a name="aws-resource-frauddetector-entitytype--seealso"></a>
+ [PutEntityType](https://docs.aws.amazon.com/frauddetector/latest/api/API_PutEntityType.html) in the *Amazon Fraud Detector API Reference*
+ [Create an entity type](https://docs.aws.amazon.com/frauddetector/latest/ug/create-an-entity-type.html) in the *Amazon Fraud Detector User Guide*