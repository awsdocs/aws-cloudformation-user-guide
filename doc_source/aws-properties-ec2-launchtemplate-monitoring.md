# Amazon EC2 LaunchTemplate Monitoring<a name="aws-properties-ec2-launchtemplate-monitoring"></a>

<a name="aws-properties-ec2-launchtemplate-monitoring-description"></a>The `Monitoring` property type describes the monitoring for the instance of an Amazon EC2 launch template\.

<a name="aws-properties-ec2-launchtemplate-monitoring-inheritance"></a> `Monitoring` is a property of the [Amazon EC2 LaunchTemplate LaunchTemplateData](aws-properties-ec2-launchtemplate-launchtemplatedata.md) property type\.

## Syntax<a name="aws-properties-ec2-launchtemplate-monitoring-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-monitoring-syntax.json"></a>

```
{
  "[Enabled](#cfn-ec2-launchtemplate-monitoring-enabled)" : Boolean
}
```

### YAML<a name="aws-properties-ec2-launchtemplate-monitoring-syntax.yaml"></a>

```
[Enabled](#cfn-ec2-launchtemplate-monitoring-enabled): Boolean
```

## Properties<a name="aws-properties-ec2-launchtemplate-monitoring-properties"></a>

`Enabled`  <a name="cfn-ec2-launchtemplate-monitoring-enabled"></a>
Specify `true` to enable detailed monitoring\. Otherwise, basic monitoring is enabled\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-ec2-launchtemplate-monitoring-seealso"></a>
+ [LaunchTemplatesMonitoringRequest](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_LaunchTemplatesMonitoringRequest.html) in the *Amazon EC2 API Reference*