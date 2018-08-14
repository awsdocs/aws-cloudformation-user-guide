# Amazon Relational Database Service OptionGroup OptionSetting<a name="aws-properties-rds-optiongroup-optionconfigurations-optionsettings"></a>

Use the `OptionSettings` property to specify settings for an option in the [`OptionConfigurations`](aws-properties-rds-optiongroup-optionconfigurations.md) property\.

## Syntax<a name="w3ab2c21c14e1634b5"></a>

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

## Properties<a name="w3ab2c21c14e1634b7"></a>

`Name`  <a name="cfn-rds-optiongroup-optionconfigurations-optionsettings-name"></a>
The name of the option setting that you want to specify\.  
*Required*: No  
*Type*: String

`Value`  <a name="cfn-rds-optiongroup-optionconfigurations-optionsettings-value"></a>
The value of the option setting\.  
*Required*: No  
*Type*: String

## See Also<a name="aws-properties-rds-optiongroup-optionsettings-seealso"></a>
+ [Working with Option Groups](http://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_WorkingWithOptionGroups.html) in the *Amazon RDS User Guide*