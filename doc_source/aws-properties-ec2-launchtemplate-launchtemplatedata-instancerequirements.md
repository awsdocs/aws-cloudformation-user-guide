# AWS::EC2::LaunchTemplate InstanceRequirements<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-instancerequirements"></a>

The attributes for the instance types\. When you specify instance attributes, Amazon EC2 will identify instance types with these attributes\.

When you specify multiple attributes, you get instance types that satisfy all of the specified attributes\. If you specify multiple values for an attribute, you get instance types that satisfy any of the specified values\.

To limit the list of instance types from which Amazon EC2 can identify matching instance types, you can use one of the following parameters, but not both in the same request:
+  `AllowedInstanceTypes` \- The instance types to include in the list\. All other instance types are ignored, even if they match your specified attributes\.
+  `ExcludedInstanceTypes` \- The instance types to exclude from the list, even if they match your specified attributes\.

**Note**  
You must specify `VCpuCount` and `MemoryMiB`\. All other attributes are optional\. Any unspecified optional attribute is set to its default\.

For more information, see [Attribute\-based instance type selection for EC2 Fleet](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-fleet-attribute-based-instance-type-selection.html), [Attribute\-based instance type selection for Spot Fleet](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/spot-fleet-attribute-based-instance-type-selection.html), and [Spot placement score](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/spot-placement-score.html) in the *Amazon EC2 User Guide*\.

## Syntax<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-instancerequirements-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-instancerequirements-syntax.json"></a>

```
{
  "[AcceleratorCount](#cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-acceleratorcount)" : AcceleratorCount,
  "[AcceleratorManufacturers](#cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-acceleratormanufacturers)" : [ String, ... ],
  "[AcceleratorNames](#cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-acceleratornames)" : [ String, ... ],
  "[AcceleratorTotalMemoryMiB](#cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-acceleratortotalmemorymib)" : AcceleratorTotalMemoryMiB,
  "[AcceleratorTypes](#cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-acceleratortypes)" : [ String, ... ],
  "[AllowedInstanceTypes](#cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-allowedinstancetypes)" : [ String, ... ],
  "[BareMetal](#cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-baremetal)" : String,
  "[BaselineEbsBandwidthMbps](#cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-baselineebsbandwidthmbps)" : BaselineEbsBandwidthMbps,
  "[BurstablePerformance](#cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-burstableperformance)" : String,
  "[CpuManufacturers](#cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-cpumanufacturers)" : [ String, ... ],
  "[ExcludedInstanceTypes](#cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-excludedinstancetypes)" : [ String, ... ],
  "[InstanceGenerations](#cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-instancegenerations)" : [ String, ... ],
  "[LocalStorage](#cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-localstorage)" : String,
  "[LocalStorageTypes](#cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-localstoragetypes)" : [ String, ... ],
  "[MemoryGiBPerVCpu](#cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-memorygibpervcpu)" : MemoryGiBPerVCpu,
  "[MemoryMiB](#cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-memorymib)" : MemoryMiB,
  "[NetworkBandwidthGbps](#cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-networkbandwidthgbps)" : NetworkBandwidthGbps,
  "[NetworkInterfaceCount](#cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-networkinterfacecount)" : NetworkInterfaceCount,
  "[OnDemandMaxPricePercentageOverLowestPrice](#cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-ondemandmaxpricepercentageoverlowestprice)" : Integer,
  "[RequireHibernateSupport](#cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-requirehibernatesupport)" : Boolean,
  "[SpotMaxPricePercentageOverLowestPrice](#cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-spotmaxpricepercentageoverlowestprice)" : Integer,
  "[TotalLocalStorageGB](#cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-totallocalstoragegb)" : TotalLocalStorageGB,
  "[VCpuCount](#cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-vcpucount)" : VCpuCount
}
```

### YAML<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-instancerequirements-syntax.yaml"></a>

```
  [AcceleratorCount](#cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-acceleratorcount): 
    AcceleratorCount
  [AcceleratorManufacturers](#cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-acceleratormanufacturers): 
    - String
  [AcceleratorNames](#cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-acceleratornames): 
    - String
  [AcceleratorTotalMemoryMiB](#cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-acceleratortotalmemorymib): 
    AcceleratorTotalMemoryMiB
  [AcceleratorTypes](#cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-acceleratortypes): 
    - String
  [AllowedInstanceTypes](#cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-allowedinstancetypes): 
    - String
  [BareMetal](#cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-baremetal): String
  [BaselineEbsBandwidthMbps](#cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-baselineebsbandwidthmbps): 
    BaselineEbsBandwidthMbps
  [BurstablePerformance](#cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-burstableperformance): String
  [CpuManufacturers](#cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-cpumanufacturers): 
    - String
  [ExcludedInstanceTypes](#cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-excludedinstancetypes): 
    - String
  [InstanceGenerations](#cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-instancegenerations): 
    - String
  [LocalStorage](#cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-localstorage): String
  [LocalStorageTypes](#cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-localstoragetypes): 
    - String
  [MemoryGiBPerVCpu](#cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-memorygibpervcpu): 
    MemoryGiBPerVCpu
  [MemoryMiB](#cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-memorymib): 
    MemoryMiB
  [NetworkBandwidthGbps](#cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-networkbandwidthgbps): 
    NetworkBandwidthGbps
  [NetworkInterfaceCount](#cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-networkinterfacecount): 
    NetworkInterfaceCount
  [OnDemandMaxPricePercentageOverLowestPrice](#cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-ondemandmaxpricepercentageoverlowestprice): Integer
  [RequireHibernateSupport](#cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-requirehibernatesupport): Boolean
  [SpotMaxPricePercentageOverLowestPrice](#cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-spotmaxpricepercentageoverlowestprice): Integer
  [TotalLocalStorageGB](#cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-totallocalstoragegb): 
    TotalLocalStorageGB
  [VCpuCount](#cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-vcpucount): 
    VCpuCount
```

## Properties<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-instancerequirements-properties"></a>

`AcceleratorCount`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-acceleratorcount"></a>
The minimum and maximum number of accelerators \(GPUs, FPGAs, or AWS Inferentia chips\) on an instance\.  
To exclude accelerator\-enabled instance types, set `Max` to `0`\.  
Default: No minimum or maximum limits  
*Required*: No  
*Type*: [AcceleratorCount](aws-properties-ec2-launchtemplate-acceleratorcount.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AcceleratorManufacturers`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-acceleratormanufacturers"></a>
Indicates whether instance types must have accelerators by specific manufacturers\.  
+ For instance types with NVIDIA devices, specify `nvidia`\.
+ For instance types with AMD devices, specify `amd`\.
+ For instance types with AWS devices, specify `amazon-web-services`\.
+ For instance types with Xilinx devices, specify `xilinx`\.
Default: Any manufacturer  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AcceleratorNames`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-acceleratornames"></a>
The accelerators that must be on the instance type\.  
+ For instance types with NVIDIA A100 GPUs, specify `a100`\.
+ For instance types with NVIDIA V100 GPUs, specify `v100`\.
+ For instance types with NVIDIA K80 GPUs, specify `k80`\.
+ For instance types with NVIDIA T4 GPUs, specify `t4`\.
+ For instance types with NVIDIA M60 GPUs, specify `m60`\.
+ For instance types with AMD Radeon Pro V520 GPUs, specify `radeon-pro-v520`\.
+ For instance types with Xilinx VU9P FPGAs, specify `vu9p`\.
+ For instance types with AWS Inferentia chips, specify `inferentia`\.
+ For instance types with NVIDIA GRID K520 GPUs, specify `k520`\.
Default: Any accelerator  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AcceleratorTotalMemoryMiB`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-acceleratortotalmemorymib"></a>
The minimum and maximum amount of total accelerator memory, in MiB\.  
Default: No minimum or maximum limits  
*Required*: No  
*Type*: [AcceleratorTotalMemoryMiB](aws-properties-ec2-launchtemplate-acceleratortotalmemorymib.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AcceleratorTypes`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-acceleratortypes"></a>
The accelerator types that must be on the instance type\.  
+ For instance types with GPU accelerators, specify `gpu`\.
+ For instance types with FPGA accelerators, specify `fpga`\.
+ For instance types with inference accelerators, specify `inference`\.
Default: Any accelerator type  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AllowedInstanceTypes`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-allowedinstancetypes"></a>
The instance types to apply your specified attributes against\. All other instance types are ignored, even if they match your specified attributes\.  
You can use strings with one or more wild cards, represented by an asterisk \(`*`\), to allow an instance type, size, or generation\. The following are examples: `m5.8xlarge`, `c5*.*`, `m5a.*`, `r*`, `*3*`\.  
For example, if you specify `c5*`,Amazon EC2 will allow the entire C5 instance family, which includes all C5a and C5n instance types\. If you specify `m5a.*`, Amazon EC2 will allow all the M5a instance types, but not the M5n instance types\.  
If you specify `AllowedInstanceTypes`, you can't specify `ExcludedInstanceTypes`\.
Default: All instance types  
*Required*: No  
*Type*: List of String  
*Maximum*: `400`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BareMetal`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-baremetal"></a>
Indicates whether bare metal instance types must be included, excluded, or required\.  
+ To include bare metal instance types, specify `included`\.
+ To require only bare metal instance types, specify `required`\.
+ To exclude bare metal instance types, specify `excluded`\.
Default: `excluded`   
*Required*: No  
*Type*: String  
*Allowed values*: `excluded | included | required`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BaselineEbsBandwidthMbps`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-baselineebsbandwidthmbps"></a>
The minimum and maximum baseline bandwidth to Amazon EBS, in Mbps\. For more information, see [Amazon EBS–optimized instances](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-optimized.html) in the *Amazon EC2 User Guide*\.  
Default: No minimum or maximum limits  
*Required*: No  
*Type*: [BaselineEbsBandwidthMbps](aws-properties-ec2-launchtemplate-baselineebsbandwidthmbps.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BurstablePerformance`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-burstableperformance"></a>
Indicates whether burstable performance T instance types are included, excluded, or required\. For more information, see [Burstable performance instances](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/burstable-performance-instances.html)\.  
+ To include burstable performance instance types, specify `included`\.
+ To require only burstable performance instance types, specify `required`\.
+ To exclude burstable performance instance types, specify `excluded`\.
Default: `excluded`   
*Required*: No  
*Type*: String  
*Allowed values*: `excluded | included | required`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CpuManufacturers`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-cpumanufacturers"></a>
The CPU manufacturers to include\.  
+ For instance types with Intel CPUs, specify `intel`\.
+ For instance types with AMD CPUs, specify `amd`\.
+ For instance types with AWS CPUs, specify `amazon-web-services`\.
Don't confuse the CPU manufacturer with the CPU architecture\. Instances will be launched with a compatible CPU architecture based on the Amazon Machine Image \(AMI\) that you specify in your launch template\.
Default: Any manufacturer  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExcludedInstanceTypes`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-excludedinstancetypes"></a>
The instance types to exclude\.  
You can use strings with one or more wild cards, represented by an asterisk \(`*`\), to exclude an instance type, size, or generation\. The following are examples: `m5.8xlarge`, `c5*.*`, `m5a.*`, `r*`, `*3*`\.  
For example, if you specify `c5*`,Amazon EC2 will exclude the entire C5 instance family, which includes all C5a and C5n instance types\. If you specify `m5a.*`, Amazon EC2 will exclude all the M5a instance types, but not the M5n instance types\.  
If you specify `ExcludedInstanceTypes`, you can't specify `AllowedInstanceTypes`\.
Default: No excluded instance types  
*Required*: No  
*Type*: List of String  
*Maximum*: `400`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceGenerations`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-instancegenerations"></a>
Indicates whether current or previous generation instance types are included\. The current generation instance types are recommended for use\. Current generation instance types are typically the latest two to three generations in each instance family\. For more information, see [Instance types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-types.html) in the *Amazon EC2 User Guide*\.  
For current generation instance types, specify `current`\.  
For previous generation instance types, specify `previous`\.  
Default: Current and previous generation instance types  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LocalStorage`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-localstorage"></a>
Indicates whether instance types with instance store volumes are included, excluded, or required\. For more information, [Amazon EC2 instance store](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/InstanceStorage.html) in the *Amazon EC2 User Guide*\.  
+ To include instance types with instance store volumes, specify `included`\.
+ To require only instance types with instance store volumes, specify `required`\.
+ To exclude instance types with instance store volumes, specify `excluded`\.
Default: `included`   
*Required*: No  
*Type*: String  
*Allowed values*: `excluded | included | required`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LocalStorageTypes`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-localstoragetypes"></a>
The type of local storage that is required\.  
+ For instance types with hard disk drive \(HDD\) storage, specify `hdd`\.
+ For instance types with solid state drive \(SSD\) storage, specify `ssd`\.
Default: `hdd` and `ssd`   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MemoryGiBPerVCpu`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-memorygibpervcpu"></a>
The minimum and maximum amount of memory per vCPU, in GiB\.  
Default: No minimum or maximum limits  
*Required*: No  
*Type*: [MemoryGiBPerVCpu](aws-properties-ec2-launchtemplate-memorygibpervcpu.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MemoryMiB`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-memorymib"></a>
The minimum and maximum amount of memory, in MiB\.  
*Required*: No  
*Type*: [MemoryMiB](aws-properties-ec2-launchtemplate-memorymib.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NetworkBandwidthGbps`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-networkbandwidthgbps"></a>
The minimum and maximum amount of network bandwidth, in gigabits per second \(Gbps\)\.  
Default: No minimum or maximum limits  
*Required*: No  
*Type*: [NetworkBandwidthGbps](aws-properties-ec2-launchtemplate-networkbandwidthgbps.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NetworkInterfaceCount`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-networkinterfacecount"></a>
The minimum and maximum number of network interfaces\.  
Default: No minimum or maximum limits  
*Required*: No  
*Type*: [NetworkInterfaceCount](aws-properties-ec2-launchtemplate-networkinterfacecount.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OnDemandMaxPricePercentageOverLowestPrice`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-ondemandmaxpricepercentageoverlowestprice"></a>
The price protection threshold for On\-Demand Instances\. This is the maximum you’ll pay for an On\-Demand Instance, expressed as a percentage above the least expensive current generation M, C, or R instance type with your specified attributes\. When Amazon EC2 selects instance types with your attributes, it excludes instance types priced above your threshold\.  
The parameter accepts an integer, which Amazon EC2 interprets as a percentage\.  
To turn off price protection, specify a high value, such as `999999`\.  
This parameter is not supported for [GetSpotPlacementScores](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_GetSpotPlacementScores.html) and [GetInstanceTypesFromInstanceRequirements](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_GetInstanceTypesFromInstanceRequirements.html)\.  
If you set `TargetCapacityUnitType` to `vcpu` or `memory-mib`, the price protection threshold is applied based on the per\-vCPU or per\-memory price instead of the per\-instance price\.
Default: `20`   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RequireHibernateSupport`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-requirehibernatesupport"></a>
Indicates whether instance types must support hibernation for On\-Demand Instances\.  
This parameter is not supported for [GetSpotPlacementScores](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_GetSpotPlacementScores.html)\.  
Default: `false`   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SpotMaxPricePercentageOverLowestPrice`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-spotmaxpricepercentageoverlowestprice"></a>
The price protection threshold for Spot Instances\. This is the maximum you’ll pay for a Spot Instance, expressed as a percentage above the least expensive current generation M, C, or R instance type with your specified attributes\. When Amazon EC2 selects instance types with your attributes, it excludes instance types priced above your threshold\.  
The parameter accepts an integer, which Amazon EC2 interprets as a percentage\.  
To turn off price protection, specify a high value, such as `999999`\.  
This parameter is not supported for [GetSpotPlacementScores](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_GetSpotPlacementScores.html) and [GetInstanceTypesFromInstanceRequirements](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_GetInstanceTypesFromInstanceRequirements.html)\.  
If you set `TargetCapacityUnitType` to `vcpu` or `memory-mib`, the price protection threshold is applied based on the per\-vCPU or per\-memory price instead of the per\-instance price\.
Default: `100`   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TotalLocalStorageGB`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-totallocalstoragegb"></a>
The minimum and maximum amount of total local storage, in GB\.  
Default: No minimum or maximum limits  
*Required*: No  
*Type*: [TotalLocalStorageGB](aws-properties-ec2-launchtemplate-totallocalstoragegb.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VCpuCount`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements-vcpucount"></a>
The minimum and maximum number of vCPUs\.  
*Required*: No  
*Type*: [VCpuCount](aws-properties-ec2-launchtemplate-vcpucount.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)