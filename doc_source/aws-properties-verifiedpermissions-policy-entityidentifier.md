# AWS::VerifiedPermissions::Policy EntityIdentifier<a name="aws-properties-verifiedpermissions-policy-entityidentifier"></a>

Contains the identifier of an entity in a policy, including its ID and type\.

## Syntax<a name="aws-properties-verifiedpermissions-policy-entityidentifier-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-verifiedpermissions-policy-entityidentifier-syntax.json"></a>

```
{
  "[EntityId](#cfn-verifiedpermissions-policy-entityidentifier-entityid)" : String,
  "[EntityType](#cfn-verifiedpermissions-policy-entityidentifier-entitytype)" : String
}
```

### YAML<a name="aws-properties-verifiedpermissions-policy-entityidentifier-syntax.yaml"></a>

```
  [EntityId](#cfn-verifiedpermissions-policy-entityidentifier-entityid): String
  [EntityType](#cfn-verifiedpermissions-policy-entityidentifier-entitytype): String
```

## Properties<a name="aws-properties-verifiedpermissions-policy-entityidentifier-properties"></a>

`EntityId`  <a name="cfn-verifiedpermissions-policy-entityidentifier-entityid"></a>
The identifier of an entity\.  
`"entityId":"identifier"`  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EntityType`  <a name="cfn-verifiedpermissions-policy-entityidentifier-entitytype"></a>
The type of an entity\.  
Example: `"entityType":"typeName"`  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)