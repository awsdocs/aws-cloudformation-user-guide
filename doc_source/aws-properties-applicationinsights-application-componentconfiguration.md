# AWS::ApplicationInsights::Application ComponentConfiguration<a name="aws-properties-applicationinsights-application-componentconfiguration"></a>

The `AWS::ApplicationInsights::Application ComponentConfiguration` property type defines the configuration settings of the component\.

## Syntax<a name="aws-properties-applicationinsights-application-componentconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-applicationinsights-application-componentconfiguration-syntax.json"></a>

```
{
  "[ConfigurationDetails](#cfn-applicationinsights-application-componentconfiguration-configurationdetails)" : ConfigurationDetails,
  "[SubComponentTypeConfigurations](#cfn-applicationinsights-application-componentconfiguration-subcomponenttypeconfigurations)" : [ SubComponentTypeConfiguration, ... ]
}
```

### YAML<a name="aws-properties-applicationinsights-application-componentconfiguration-syntax.yaml"></a>

```
  [ConfigurationDetails](#cfn-applicationinsights-application-componentconfiguration-configurationdetails): 
    ConfigurationDetails
  [SubComponentTypeConfigurations](#cfn-applicationinsights-application-componentconfiguration-subcomponenttypeconfigurations): 
    - SubComponentTypeConfiguration
```

## Properties<a name="aws-properties-applicationinsights-application-componentconfiguration-properties"></a>

`ConfigurationDetails`  <a name="cfn-applicationinsights-application-componentconfiguration-configurationdetails"></a>
The configuration settings\.  
*Required*: No  
*Type*: [ConfigurationDetails](aws-properties-applicationinsights-application-configurationdetails.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubComponentTypeConfigurations`  <a name="cfn-applicationinsights-application-componentconfiguration-subcomponenttypeconfigurations"></a>
Sub\-component configurations of the component\.  
*Required*: No  
*Type*: List of [SubComponentTypeConfiguration](aws-properties-applicationinsights-application-subcomponenttypeconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)