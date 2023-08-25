# AWS::EMRServerless::Application MaximumAllowedResources<a name="aws-properties-emrserverless-application-maximumallowedresources"></a>

The maximum allowed cumulative resources for an application\. No new resources will be created once the limit is hit\.

## Syntax<a name="aws-properties-emrserverless-application-maximumallowedresources-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-emrserverless-application-maximumallowedresources-syntax.json"></a>

```
{
  "[Cpu](#cfn-emrserverless-application-maximumallowedresources-cpu)" : String,
  "[Disk](#cfn-emrserverless-application-maximumallowedresources-disk)" : String,
  "[Memory](#cfn-emrserverless-application-maximumallowedresources-memory)" : String
}
```

### YAML<a name="aws-properties-emrserverless-application-maximumallowedresources-syntax.yaml"></a>

```
  [Cpu](#cfn-emrserverless-application-maximumallowedresources-cpu): String
  [Disk](#cfn-emrserverless-application-maximumallowedresources-disk): String
  [Memory](#cfn-emrserverless-application-maximumallowedresources-memory): String
```

## Properties<a name="aws-properties-emrserverless-application-maximumallowedresources-properties"></a>

`Cpu`  <a name="cfn-emrserverless-application-maximumallowedresources-cpu"></a>
The maximum allowed CPU for an application\.  
*Minimum*: 1  
*Maximum*: 15  
*Pattern*: `^[1-9][0-9]*(\\s)?(vCPU|vcpu|VCPU)?$`  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `15`  
*Pattern*: `[1-9][0-9]*(\s)?(vCPU|vcpu|VCPU)?`  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`Disk`  <a name="cfn-emrserverless-application-maximumallowedresources-disk"></a>
The maximum allowed disk for an application\.  
*Minimum*: 1  
*Maximum*: 15  
*Pattern*: `^[1-9][0-9]*(\\s)?(GB|gb|gB|Gb)$"`  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `15`  
*Pattern*: `[1-9][0-9]*(\s)?(GB|gb|gB|Gb)`  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`Memory`  <a name="cfn-emrserverless-application-maximumallowedresources-memory"></a>
The maximum allowed resources for an application\.  
*Minimum*: 1  
*Maximum*: 15  
*Pattern*: `^[1-9][0-9]*(\\s)?(GB|gb|gB|Gb)?$`  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `15`  
*Pattern*: `[1-9][0-9]*(\s)?(GB|gb|gB|Gb)?`  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)