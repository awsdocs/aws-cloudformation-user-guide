# AWS::EC2::LaunchTemplate Monitoring<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-monitoring"></a>

Specifies whether detailed monitoring is enabled for an instance\.

`Monitoring` is a property of [AWS::EC2::LaunchTemplate LaunchTemplateData](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-launchtemplate-launchtemplatedata.html)\.

## Syntax<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-monitoring-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-monitoring-syntax.json"></a>

```
{
  "[Enabled](#cfn-ec2-launchtemplate-launchtemplatedata-monitoring-enabled)" : Boolean
}
```

### YAML<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-monitoring-syntax.yaml"></a>

```
  [Enabled](#cfn-ec2-launchtemplate-launchtemplatedata-monitoring-enabled): Boolean
```

## Properties<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-monitoring-properties"></a>

`Enabled`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-monitoring-enabled"></a>
Specify `true` to enable detailed monitoring\. Otherwise, basic monitoring is enabled\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-monitoring--seealso"></a>
+  [ LaunchTemplatesMonitoringRequest](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_LaunchTemplatesMonitoringRequest.html) in the *Amazon Elastic Compute Cloud API Reference* 

