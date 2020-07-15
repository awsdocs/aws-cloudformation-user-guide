# AWS::Synthetics::Canary RunConfig<a name="aws-properties-synthetics-canary-runconfig"></a>

A structure that contains input information for a canary run\. This structure is required\.

## Syntax<a name="aws-properties-synthetics-canary-runconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-synthetics-canary-runconfig-syntax.json"></a>

```
{
  "[MemoryInMB](#cfn-synthetics-canary-runconfig-memoryinmb)" : Integer,
  "[TimeoutInSeconds](#cfn-synthetics-canary-runconfig-timeoutinseconds)" : Integer
}
```

### YAML<a name="aws-properties-synthetics-canary-runconfig-syntax.yaml"></a>

```
  [MemoryInMB](#cfn-synthetics-canary-runconfig-memoryinmb): Integer
  [TimeoutInSeconds](#cfn-synthetics-canary-runconfig-timeoutinseconds): Integer
```

## Properties<a name="aws-properties-synthetics-canary-runconfig-properties"></a>

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
*Minimum*: `60`  
*Maximum*: `900`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)