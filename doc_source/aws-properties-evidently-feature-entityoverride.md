# AWS::Evidently::Feature EntityOverride<a name="aws-properties-evidently-feature-entityoverride"></a>

A set of key\-value pairs that specify users who should always be served a specific variation of a feature\. Each key specifies a user using their user ID, account ID, or some other identifier\. The value specifies the name of the variation that the user is to be served\.

## Syntax<a name="aws-properties-evidently-feature-entityoverride-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-evidently-feature-entityoverride-syntax.json"></a>

```
{
  "[EntityId](#cfn-evidently-feature-entityoverride-entityid)" : String,
  "[Variation](#cfn-evidently-feature-entityoverride-variation)" : String
}
```

### YAML<a name="aws-properties-evidently-feature-entityoverride-syntax.yaml"></a>

```
  [EntityId](#cfn-evidently-feature-entityoverride-entityid): String
  [Variation](#cfn-evidently-feature-entityoverride-variation): String
```

## Properties<a name="aws-properties-evidently-feature-entityoverride-properties"></a>

`EntityId`  <a name="cfn-evidently-feature-entityoverride-entityid"></a>
The entity ID to be served the variation specified in `Variation`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Variation`  <a name="cfn-evidently-feature-entityoverride-variation"></a>
The name of the variation to serve to the user session that matches the `EntityId`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)