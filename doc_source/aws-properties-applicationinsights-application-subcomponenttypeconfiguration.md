# AWS::ApplicationInsights::Application SubComponentTypeConfiguration<a name="aws-properties-applicationinsights-application-subcomponenttypeconfiguration"></a>

The `AWS::ApplicationInsights::Application SubComponentTypeConfiguration` property type specifies the sub\-component configurations for a component\.

## Syntax<a name="aws-properties-applicationinsights-application-subcomponenttypeconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-applicationinsights-application-subcomponenttypeconfiguration-syntax.json"></a>

```
{
  "[SubComponentConfigurationDetails](#cfn-applicationinsights-application-subcomponenttypeconfiguration-subcomponentconfigurationdetails)" : SubComponentConfigurationDetails,
  "[SubComponentType](#cfn-applicationinsights-application-subcomponenttypeconfiguration-subcomponenttype)" : String
}
```

### YAML<a name="aws-properties-applicationinsights-application-subcomponenttypeconfiguration-syntax.yaml"></a>

```
  [SubComponentConfigurationDetails](#cfn-applicationinsights-application-subcomponenttypeconfiguration-subcomponentconfigurationdetails): 
    SubComponentConfigurationDetails
  [SubComponentType](#cfn-applicationinsights-application-subcomponenttypeconfiguration-subcomponenttype): String
```

## Properties<a name="aws-properties-applicationinsights-application-subcomponenttypeconfiguration-properties"></a>

`SubComponentConfigurationDetails`  <a name="cfn-applicationinsights-application-subcomponenttypeconfiguration-subcomponentconfigurationdetails"></a>
The configuration settings of the sub\-components\.  
*Required*: Yes  
*Type*: [SubComponentConfigurationDetails](aws-properties-applicationinsights-application-subcomponentconfigurationdetails.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubComponentType`  <a name="cfn-applicationinsights-application-subcomponenttypeconfiguration-subcomponenttype"></a>
The sub\-component type\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)