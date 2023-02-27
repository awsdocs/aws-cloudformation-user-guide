# AWS::GreengrassV2::Deployment IoTJobRateIncreaseCriteria<a name="aws-properties-greengrassv2-deployment-iotjobrateincreasecriteria"></a>

Contains information about criteria to meet before a job increases its rollout rate\. Specify either `numberOfNotifiedThings` or `numberOfSucceededThings`\.

## Syntax<a name="aws-properties-greengrassv2-deployment-iotjobrateincreasecriteria-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrassv2-deployment-iotjobrateincreasecriteria-syntax.json"></a>

```
{
  "[NumberOfNotifiedThings](#cfn-greengrassv2-deployment-iotjobrateincreasecriteria-numberofnotifiedthings)" : Integer,
  "[NumberOfSucceededThings](#cfn-greengrassv2-deployment-iotjobrateincreasecriteria-numberofsucceededthings)" : Integer
}
```

### YAML<a name="aws-properties-greengrassv2-deployment-iotjobrateincreasecriteria-syntax.yaml"></a>

```
  [NumberOfNotifiedThings](#cfn-greengrassv2-deployment-iotjobrateincreasecriteria-numberofnotifiedthings): Integer
  [NumberOfSucceededThings](#cfn-greengrassv2-deployment-iotjobrateincreasecriteria-numberofsucceededthings): Integer
```

## Properties<a name="aws-properties-greengrassv2-deployment-iotjobrateincreasecriteria-properties"></a>

`NumberOfNotifiedThings`  <a name="cfn-greengrassv2-deployment-iotjobrateincreasecriteria-numberofnotifiedthings"></a>
The number of devices to receive the job notification before the rollout rate increases\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`NumberOfSucceededThings`  <a name="cfn-greengrassv2-deployment-iotjobrateincreasecriteria-numberofsucceededthings"></a>
The number of devices to successfully run the configuration job before the rollout rate increases\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)