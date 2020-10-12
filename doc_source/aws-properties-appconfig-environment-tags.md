# AWS::AppConfig::Environment Tags<a name="aws-properties-appconfig-environment-tags"></a>

Metadata to assign to the environment\. Tags help organize and categorize your AWS AppConfig resources\. Each tag consists of a key and an optional value, both of which you define\.

## Syntax<a name="aws-properties-appconfig-environment-tags-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appconfig-environment-tags-syntax.json"></a>

```
{
  "[Key](#cfn-appconfig-environment-tags-key)" : String,
  "[Value](#cfn-appconfig-environment-tags-value)" : String
}
```

### YAML<a name="aws-properties-appconfig-environment-tags-syntax.yaml"></a>

```
  [Key](#cfn-appconfig-environment-tags-key): String
  [Value](#cfn-appconfig-environment-tags-value): String
```

## Properties<a name="aws-properties-appconfig-environment-tags-properties"></a>

`Key`  <a name="cfn-appconfig-environment-tags-key"></a>
The key\-value string map\. The valid character set is `[a-zA-Z+-=._:/]`\. The tag key can be up to 128 characters and must not start with `aws:`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-appconfig-environment-tags-value"></a>
The tag value can be up to 256 characters\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)