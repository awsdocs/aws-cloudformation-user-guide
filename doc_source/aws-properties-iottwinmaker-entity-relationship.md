# AWS::IoTTwinMaker::Entity Relationship<a name="aws-properties-iottwinmaker-entity-relationship"></a>

The entity relationship\.

## Syntax<a name="aws-properties-iottwinmaker-entity-relationship-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iottwinmaker-entity-relationship-syntax.json"></a>

```
{
  "[RelationshipType](#cfn-iottwinmaker-entity-relationship-relationshiptype)" : String,
  "[TargetComponentTypeId](#cfn-iottwinmaker-entity-relationship-targetcomponenttypeid)" : String
}
```

### YAML<a name="aws-properties-iottwinmaker-entity-relationship-syntax.yaml"></a>

```
  [RelationshipType](#cfn-iottwinmaker-entity-relationship-relationshiptype): String
  [TargetComponentTypeId](#cfn-iottwinmaker-entity-relationship-targetcomponenttypeid): String
```

## Properties<a name="aws-properties-iottwinmaker-entity-relationship-properties"></a>

`RelationshipType`  <a name="cfn-iottwinmaker-entity-relationship-relationshiptype"></a>
The relationship type\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetComponentTypeId`  <a name="cfn-iottwinmaker-entity-relationship-targetcomponenttypeid"></a>
the component type Id target\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)