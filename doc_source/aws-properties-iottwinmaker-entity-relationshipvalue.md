# AWS::IoTTwinMaker::Entity RelationshipValue<a name="aws-properties-iottwinmaker-entity-relationshipvalue"></a>

The entity relationship\.

## Syntax<a name="aws-properties-iottwinmaker-entity-relationshipvalue-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iottwinmaker-entity-relationshipvalue-syntax.json"></a>

```
{
  "[TargetComponentName](#cfn-iottwinmaker-entity-relationshipvalue-targetcomponentname)" : String,
  "[TargetEntityId](#cfn-iottwinmaker-entity-relationshipvalue-targetentityid)" : String
}
```

### YAML<a name="aws-properties-iottwinmaker-entity-relationshipvalue-syntax.yaml"></a>

```
  [TargetComponentName](#cfn-iottwinmaker-entity-relationshipvalue-targetcomponentname): String
  [TargetEntityId](#cfn-iottwinmaker-entity-relationshipvalue-targetentityid): String
```

## Properties<a name="aws-properties-iottwinmaker-entity-relationshipvalue-properties"></a>

`TargetComponentName`  <a name="cfn-iottwinmaker-entity-relationshipvalue-targetcomponentname"></a>
The target component name\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetEntityId`  <a name="cfn-iottwinmaker-entity-relationshipvalue-targetentityid"></a>
The target entity Id\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)