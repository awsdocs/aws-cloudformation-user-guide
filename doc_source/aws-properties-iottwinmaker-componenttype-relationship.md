# AWS::IoTTwinMaker::ComponentType Relationship<a name="aws-properties-iottwinmaker-componenttype-relationship"></a>

An object that specifies a relationship with another component type\.

## Syntax<a name="aws-properties-iottwinmaker-componenttype-relationship-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iottwinmaker-componenttype-relationship-syntax.json"></a>

```
{
  "[RelationshipType](#cfn-iottwinmaker-componenttype-relationship-relationshiptype)" : String,
  "[TargetComponentTypeId](#cfn-iottwinmaker-componenttype-relationship-targetcomponenttypeid)" : String
}
```

### YAML<a name="aws-properties-iottwinmaker-componenttype-relationship-syntax.yaml"></a>

```
  [RelationshipType](#cfn-iottwinmaker-componenttype-relationship-relationshiptype): String
  [TargetComponentTypeId](#cfn-iottwinmaker-componenttype-relationship-targetcomponenttypeid): String
```

## Properties<a name="aws-properties-iottwinmaker-componenttype-relationship-properties"></a>

`RelationshipType`  <a name="cfn-iottwinmaker-componenttype-relationship-relationshiptype"></a>
The type of the relationship\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetComponentTypeId`  <a name="cfn-iottwinmaker-componenttype-relationship-targetcomponenttypeid"></a>
The ID of the target component type associated with this relationship\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)