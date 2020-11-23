# AWS::RDS::OptionGroup OptionSetting<a name="aws-properties-rds-optiongroup-optionconfigurations-optionsettings"></a>

The `OptionSetting` property type specifies the value for an option within an `OptionSetting` property\.

## Syntax<a name="aws-properties-rds-optiongroup-optionconfigurations-optionsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-rds-optiongroup-optionconfigurations-optionsettings-syntax.json"></a>

```
{
  "[Name](#cfn-rds-optiongroup-optionconfigurations-optionsettings-name)" : String,
  "[Value](#cfn-rds-optiongroup-optionconfigurations-optionsettings-value)" : String
}
```

### YAML<a name="aws-properties-rds-optiongroup-optionconfigurations-optionsettings-syntax.yaml"></a>

```
  [Name](#cfn-rds-optiongroup-optionconfigurations-optionsettings-name): String
  [Value](#cfn-rds-optiongroup-optionconfigurations-optionsettings-value): String
```

## Properties<a name="aws-properties-rds-optiongroup-optionconfigurations-optionsettings-properties"></a>

`Name`  <a name="cfn-rds-optiongroup-optionconfigurations-optionsettings-name"></a>
The name of the option that has settings that you can set\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-rds-optiongroup-optionconfigurations-optionsettings-value"></a>
The current value of the option setting\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)