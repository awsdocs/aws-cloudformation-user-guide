# AWS::AppRunner::Service NetworkConfiguration<a name="aws-properties-apprunner-service-networkconfiguration"></a>

Describes configuration settings related to network traffic of an AWS App Runner service\. Consists of embedded objects for each configurable network feature\.

## Syntax<a name="aws-properties-apprunner-service-networkconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-apprunner-service-networkconfiguration-syntax.json"></a>

```
{
  "[EgressConfiguration](#cfn-apprunner-service-networkconfiguration-egressconfiguration)" : EgressConfiguration
}
```

### YAML<a name="aws-properties-apprunner-service-networkconfiguration-syntax.yaml"></a>

```
  [EgressConfiguration](#cfn-apprunner-service-networkconfiguration-egressconfiguration): 
    EgressConfiguration
```

## Properties<a name="aws-properties-apprunner-service-networkconfiguration-properties"></a>

`EgressConfiguration`  <a name="cfn-apprunner-service-networkconfiguration-egressconfiguration"></a>
Network configuration settings for outbound message traffic\.  
*Required*: Yes  
*Type*: [EgressConfiguration](aws-properties-apprunner-service-egressconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)