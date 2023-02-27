# AWS::CustomerProfiles::Integration ObjectTypeMapping<a name="aws-properties-customerprofiles-integration-objecttypemapping"></a>

A map in which each key is an event type from an external application such as Segment or Shopify, and each value is an `ObjectTypeName` \(template\) used to ingest the event\.

## Syntax<a name="aws-properties-customerprofiles-integration-objecttypemapping-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-customerprofiles-integration-objecttypemapping-syntax.json"></a>

```
{
  "[Key](#cfn-customerprofiles-integration-objecttypemapping-key)" : String,
  "[Value](#cfn-customerprofiles-integration-objecttypemapping-value)" : String
}
```

### YAML<a name="aws-properties-customerprofiles-integration-objecttypemapping-syntax.yaml"></a>

```
  [Key](#cfn-customerprofiles-integration-objecttypemapping-key): String
  [Value](#cfn-customerprofiles-integration-objecttypemapping-value): String
```

## Properties<a name="aws-properties-customerprofiles-integration-objecttypemapping-properties"></a>

`Key`  <a name="cfn-customerprofiles-integration-objecttypemapping-key"></a>
The key\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-customerprofiles-integration-objecttypemapping-value"></a>
The value\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)