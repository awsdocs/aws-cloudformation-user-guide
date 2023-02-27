# AWS::NimbleStudio::LaunchProfile VolumeConfiguration<a name="aws-properties-nimblestudio-launchprofile-volumeconfiguration"></a>

Custom volume configuration for the root volumes that are attached to streaming sessions\.

This parameter is only allowed when `sessionPersistenceMode` is `ACTIVATED`\.

## Syntax<a name="aws-properties-nimblestudio-launchprofile-volumeconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-nimblestudio-launchprofile-volumeconfiguration-syntax.json"></a>

```
{
  "[Iops](#cfn-nimblestudio-launchprofile-volumeconfiguration-iops)" : Double,
  "[Size](#cfn-nimblestudio-launchprofile-volumeconfiguration-size)" : Double,
  "[Throughput](#cfn-nimblestudio-launchprofile-volumeconfiguration-throughput)" : Double
}
```

### YAML<a name="aws-properties-nimblestudio-launchprofile-volumeconfiguration-syntax.yaml"></a>

```
  [Iops](#cfn-nimblestudio-launchprofile-volumeconfiguration-iops): Double
  [Size](#cfn-nimblestudio-launchprofile-volumeconfiguration-size): Double
  [Throughput](#cfn-nimblestudio-launchprofile-volumeconfiguration-throughput): Double
```

## Properties<a name="aws-properties-nimblestudio-launchprofile-volumeconfiguration-properties"></a>

`Iops`  <a name="cfn-nimblestudio-launchprofile-volumeconfiguration-iops"></a>
The number of I/O operations per second for the root volume that is attached to streaming session\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Size`  <a name="cfn-nimblestudio-launchprofile-volumeconfiguration-size"></a>
The size of the root volume that is attached to the streaming session\. The root volume size is measured in GiBs\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Throughput`  <a name="cfn-nimblestudio-launchprofile-volumeconfiguration-throughput"></a>
The throughput to provision for the root volume that is attached to the streaming session\. The throughput is measured in MiB/s\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)