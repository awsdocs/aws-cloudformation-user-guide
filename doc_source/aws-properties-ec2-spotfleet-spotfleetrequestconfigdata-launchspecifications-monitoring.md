# AWS::EC2::SpotFleet SpotFleetMonitoring<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-monitoring"></a>

Describes whether monitoring is enabled\.

## Syntax<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-monitoring-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-monitoring-syntax.json"></a>

```
{
  "[Enabled](#cfn-ec2-spotfleet-spotfleetmonitoring-enabled)" : Boolean
}
```

### YAML<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-monitoring-syntax.yaml"></a>

```
  [Enabled](#cfn-ec2-spotfleet-spotfleetmonitoring-enabled): Boolean
```

## Properties<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-monitoring-properties"></a>

`Enabled`  <a name="cfn-ec2-spotfleet-spotfleetmonitoring-enabled"></a>
Enables monitoring for the instance\.  
Default: `false`   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)