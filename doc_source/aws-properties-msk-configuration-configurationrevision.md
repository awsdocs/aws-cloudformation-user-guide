# AWS::MSK::Configuration ConfigurationRevision<a name="aws-properties-msk-configuration-configurationrevision"></a>

Describes a configuration revision\.

## Syntax<a name="aws-properties-msk-configuration-configurationrevision-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-msk-configuration-configurationrevision-syntax.json"></a>

```
{
  "[CreationTime](#cfn-msk-configuration-configurationrevision-creationtime)" : String,
  "[Description](#cfn-msk-configuration-configurationrevision-description)" : String,
  "[Revision](#cfn-msk-configuration-configurationrevision-revision)" : Integer
}
```

### YAML<a name="aws-properties-msk-configuration-configurationrevision-syntax.yaml"></a>

```
  [CreationTime](#cfn-msk-configuration-configurationrevision-creationtime): String
  [Description](#cfn-msk-configuration-configurationrevision-description): String
  [Revision](#cfn-msk-configuration-configurationrevision-revision): Integer
```

## Properties<a name="aws-properties-msk-configuration-configurationrevision-properties"></a>

`CreationTime`  <a name="cfn-msk-configuration-configurationrevision-creationtime"></a>
The time when the configuration revision was created\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-msk-configuration-configurationrevision-description"></a>
The description of the configuration revision\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Revision`  <a name="cfn-msk-configuration-configurationrevision-revision"></a>
The revision number\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)