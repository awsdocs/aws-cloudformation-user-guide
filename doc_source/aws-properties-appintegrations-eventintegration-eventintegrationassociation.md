# AWS::AppIntegrations::EventIntegration EventIntegrationAssociation<a name="aws-properties-appintegrations-eventintegration-eventintegrationassociation"></a>

The event integration association\.

## Syntax<a name="aws-properties-appintegrations-eventintegration-eventintegrationassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appintegrations-eventintegration-eventintegrationassociation-syntax.json"></a>

```
{
  "[ClientAssociationMetadata](#cfn-appintegrations-eventintegration-eventintegrationassociation-clientassociationmetadata)" : [ Metadata, ... ],
  "[ClientId](#cfn-appintegrations-eventintegration-eventintegrationassociation-clientid)" : String,
  "[EventBridgeRuleName](#cfn-appintegrations-eventintegration-eventintegrationassociation-eventbridgerulename)" : String,
  "[EventIntegrationAssociationArn](#cfn-appintegrations-eventintegration-eventintegrationassociation-eventintegrationassociationarn)" : String,
  "[EventIntegrationAssociationId](#cfn-appintegrations-eventintegration-eventintegrationassociation-eventintegrationassociationid)" : String
}
```

### YAML<a name="aws-properties-appintegrations-eventintegration-eventintegrationassociation-syntax.yaml"></a>

```
  [ClientAssociationMetadata](#cfn-appintegrations-eventintegration-eventintegrationassociation-clientassociationmetadata): 
    - Metadata
  [ClientId](#cfn-appintegrations-eventintegration-eventintegrationassociation-clientid): String
  [EventBridgeRuleName](#cfn-appintegrations-eventintegration-eventintegrationassociation-eventbridgerulename): String
  [EventIntegrationAssociationArn](#cfn-appintegrations-eventintegration-eventintegrationassociation-eventintegrationassociationarn): String
  [EventIntegrationAssociationId](#cfn-appintegrations-eventintegration-eventintegrationassociation-eventintegrationassociationid): String
```

## Properties<a name="aws-properties-appintegrations-eventintegration-eventintegrationassociation-properties"></a>

`ClientAssociationMetadata`  <a name="cfn-appintegrations-eventintegration-eventintegrationassociation-clientassociationmetadata"></a>
The metadata associated with the client\.  
*Required*: No  
*Type*: List of [Metadata](aws-properties-appintegrations-eventintegration-metadata.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ClientId`  <a name="cfn-appintegrations-eventintegration-eventintegrationassociation-clientid"></a>
The identifier for the client that is associated with the event integration\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EventBridgeRuleName`  <a name="cfn-appintegrations-eventintegration-eventintegrationassociation-eventbridgerulename"></a>
The name of the EventBridge rule\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EventIntegrationAssociationArn`  <a name="cfn-appintegrations-eventintegration-eventintegrationassociation-eventintegrationassociationarn"></a>
The Amazon Resource Name \(ARN\) for the event integration association\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EventIntegrationAssociationId`  <a name="cfn-appintegrations-eventintegration-eventintegrationassociation-eventintegrationassociationid"></a>
The identifier for the event integration association\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)