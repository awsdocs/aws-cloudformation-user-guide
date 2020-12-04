# AWS::Synthetics::Canary RunConfig<a name="aws-properties-synthetics-canary-runconfig"></a>

A structure that contains input information for a canary run\. This structure is required\.

## Syntax<a name="aws-properties-synthetics-canary-runconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-synthetics-canary-runconfig-syntax.json"></a>

```
{
  "[ActiveTracing](#cfn-synthetics-canary-runconfig-activetracing)" : Boolean,
  "[MemoryInMB](#cfn-synthetics-canary-runconfig-memoryinmb)" : Integer,
  "[TimeoutInSeconds](#cfn-synthetics-canary-runconfig-timeoutinseconds)" : Integer
}
```

### YAML<a name="aws-properties-synthetics-canary-runconfig-syntax.yaml"></a>

```
  [ActiveTracing](#cfn-synthetics-canary-runconfig-activetracing): Boolean
  [MemoryInMB](#cfn-synthetics-canary-runconfig-memoryinmb): Integer
  [TimeoutInSeconds](#cfn-synthetics-canary-runconfig-timeoutinseconds): Integer
```

## Properties<a name="aws-properties-synthetics-canary-runconfig-properties"></a>

`ActiveTracing`  <a name="cfn-synthetics-canary-runconfig-activetracing"></a>
Specifies whether this canary is to use active AWS X\-Ray tracing when it runs\. Active tracing enables this canary run to be displayed in the ServiceLens and X\-Ray service maps even if the canary does not hit an endpoint that has X\-ray tracing enabled\. Using X\-Ray tracing incurs charges\. For more information, see [Canaries and X\-Ray tracing](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch_Synthetics_Canaries_tracing.html)\.  
 You can enable active tracing only for canaries that use version `syn-nodejs-2.0` or later for their canary runtime\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MemoryInMB`  <a name="cfn-synthetics-canary-runconfig-memoryinmb"></a>
The maximum amount of memory that the canary can use while running\. This value must be a multiple of 64\. The range is 960 to 3008\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `960`  
*Maximum*: `3008`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeoutInSeconds`  <a name="cfn-synthetics-canary-runconfig-timeoutinseconds"></a>
How long the canary is allowed to run before it must stop\. You can't set this time to be longer than the frequency of the runs of this canary\.  
If you omit this field, the frequency of the canary is used as this value, up to a maximum of 900 seconds\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `3`  
*Maximum*: `840`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)