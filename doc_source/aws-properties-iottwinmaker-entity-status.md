# AWS::IoTTwinMaker::Entity Status<a name="aws-properties-iottwinmaker-entity-status"></a>

The current status of the entity\.

## Syntax<a name="aws-properties-iottwinmaker-entity-status-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iottwinmaker-entity-status-syntax.json"></a>

```
{
  "[Error](#cfn-iottwinmaker-entity-status-error)" : Error,
  "[State](#cfn-iottwinmaker-entity-status-state)" : String
}
```

### YAML<a name="aws-properties-iottwinmaker-entity-status-syntax.yaml"></a>

```
  [Error](#cfn-iottwinmaker-entity-status-error): 
    Error
  [State](#cfn-iottwinmaker-entity-status-state): String
```

## Properties<a name="aws-properties-iottwinmaker-entity-status-properties"></a>

`Error`  <a name="cfn-iottwinmaker-entity-status-error"></a>
The error message\.  
*Required*: No  
*Type*: [Error](aws-properties-iottwinmaker-entity-error.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`State`  <a name="cfn-iottwinmaker-entity-status-state"></a>
The current state of the entity, component, component type, or workspace\.  
Valid Values: `CREATING | UPDATING | DELETING | ACTIVE | ERROR`  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)