# AWS::SES::EmailIdentity ConfigurationSetAttributes<a name="aws-properties-ses-emailidentity-configurationsetattributes"></a>

Used to associate a configuration set with an email identity\.

## Syntax<a name="aws-properties-ses-emailidentity-configurationsetattributes-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ses-emailidentity-configurationsetattributes-syntax.json"></a>

```
{
  "[ConfigurationSetName](#cfn-ses-emailidentity-configurationsetattributes-configurationsetname)" : String
}
```

### YAML<a name="aws-properties-ses-emailidentity-configurationsetattributes-syntax.yaml"></a>

```
  [ConfigurationSetName](#cfn-ses-emailidentity-configurationsetattributes-configurationsetname): String
```

## Properties<a name="aws-properties-ses-emailidentity-configurationsetattributes-properties"></a>

`ConfigurationSetName`  <a name="cfn-ses-emailidentity-configurationsetattributes-configurationsetname"></a>
The configuration set to associate with an email identity\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)