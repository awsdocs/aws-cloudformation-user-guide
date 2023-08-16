# AWS::SES::ConfigurationSet SuppressionOptions<a name="aws-properties-ses-configurationset-suppressionoptions"></a>

An object that contains information about the suppression list preferences for your account\.

## Syntax<a name="aws-properties-ses-configurationset-suppressionoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ses-configurationset-suppressionoptions-syntax.json"></a>

```
{
  "[SuppressedReasons](#cfn-ses-configurationset-suppressionoptions-suppressedreasons)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-ses-configurationset-suppressionoptions-syntax.yaml"></a>

```
  [SuppressedReasons](#cfn-ses-configurationset-suppressionoptions-suppressedreasons): 
    - String
```

## Properties<a name="aws-properties-ses-configurationset-suppressionoptions-properties"></a>

`SuppressedReasons`  <a name="cfn-ses-configurationset-suppressionoptions-suppressedreasons"></a>
A list that contains the reasons that email addresses are automatically added to the suppression list for your account\. This list can contain any or all of the following:  
+ `COMPLAINT` – Amazon SES adds an email address to the suppression list for your account when a message sent to that address results in a complaint\.
+ `BOUNCE` – Amazon SES adds an email address to the suppression list for your account when a message sent to that address results in a hard bounce\.
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)