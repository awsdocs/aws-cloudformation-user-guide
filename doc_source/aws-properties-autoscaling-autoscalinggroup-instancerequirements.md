# AWS::AutoScaling::AutoScalingGroup InstanceRequirements<a name="aws-properties-autoscaling-autoscalinggroup-instancerequirements"></a>

The attributes for the instance types for a mixed instances policy\. Amazon EC2 Auto Scaling uses your specified requirements to identify instance types\. Then, it uses your On\-Demand and Spot allocation strategies to launch instances from these instance types\.

When you specify multiple attributes, you get instance types that satisfy all of the specified attributes\. If you specify multiple values for an attribute, you get instance types that satisfy any of the specified values\.

To limit the list of instance types from which Amazon EC2 Auto Scaling can identify matching instance types, you can use one of the following parameters, but not both in the same request:
+ `AllowedInstanceTypes` \- The instance types to include in the list\. All other instance types are ignored, even if they match your specified attributes\.
+ `ExcludedInstanceTypes` \- The instance types to exclude from the list, even if they match your specified attributes\.

**Note**  
You must specify `VCpuCount` and `MemoryMiB`\. All other attributes are optional\. Any unspecified optional attribute is set to its default\.

For an example template, see [Auto scaling template snippets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-autoscaling.html)\.

For more information, see [Creating an Auto Scaling group using attribute\-based instance type selection](https://docs.aws.amazon.com/autoscaling/ec2/userguide/create-asg-instance-type-requirements.html) in the *Amazon EC2 Auto Scaling User Guide*\. For help determining which instance types match your attributes before you apply them to your Auto Scaling group, see [Preview instance types with specified attributes](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-fleet-attribute-based-instance-type-selection.html#ec2fleet-get-instance-types-from-instance-requirements) in the *Amazon EC2 User Guide for Linux Instances*\.

`InstanceRequirements` is a property of the `LaunchTemplateOverrides` property of the [AWS::AutoScaling::AutoScalingGroup LaunchTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscaling-autoscalinggroup-launchtemplate.html) property type\.

## Syntax<a name="aws-properties-autoscaling-autoscalinggroup-instancerequirements-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscaling-autoscalinggroup-instancerequirements-syntax.json"></a>

```
{
  "[AcceleratorCount](#cfn-autoscaling-autoscalinggroup-instancerequirements-acceleratorcount)" : AcceleratorCountRequest,
  "[AcceleratorManufacturers](#cfn-autoscaling-autoscalinggroup-instancerequirements-acceleratormanufacturers)" : [ String, ... ],
  "[AcceleratorNames](#cfn-autoscaling-autoscalinggroup-instancerequirements-acceleratornames)" : [ String, ... ],
  "[AcceleratorTotalMemoryMiB](#cfn-autoscaling-autoscalinggroup-instancerequirements-acceleratortotalmemorymib)" : AcceleratorTotalMemoryMiBRequest,
  "[AcceleratorTypes](#cfn-autoscaling-autoscalinggroup-instancerequirements-acceleratortypes)" : [ String, ... ],
  "[AllowedInstanceTypes](#cfn-autoscaling-autoscalinggroup-instancerequirements-allowedinstancetypes)" : [ String, ... ],
  "[BareMetal](#cfn-autoscaling-autoscalinggroup-instancerequirements-baremetal)" : String,
  "[BaselineEbsBandwidthMbps](#cfn-autoscaling-autoscalinggroup-instancerequirements-baselineebsbandwidthmbps)" : BaselineEbsBandwidthMbpsRequest,
  "[BurstablePerformance](#cfn-autoscaling-autoscalinggroup-instancerequirements-burstableperformance)" : String,
  "[CpuManufacturers](#cfn-autoscaling-autoscalinggroup-instancerequirements-cpumanufacturers)" : [ String, ... ],
  "[ExcludedInstanceTypes](#cfn-autoscaling-autoscalinggroup-instancerequirements-excludedinstancetypes)" : [ String, ... ],
  "[InstanceGenerations](#cfn-autoscaling-autoscalinggroup-instancerequirements-instancegenerations)" : [ String, ... ],
  "[LocalStorage](#cfn-autoscaling-autoscalinggroup-instancerequirements-localstorage)" : String,
  "[LocalStorageTypes](#cfn-autoscaling-autoscalinggroup-instancerequirements-localstoragetypes)" : [ String, ... ],
  "[MemoryGiBPerVCpu](#cfn-autoscaling-autoscalinggroup-instancerequirements-memorygibpervcpu)" : MemoryGiBPerVCpuRequest,
  "[MemoryMiB](#cfn-autoscaling-autoscalinggroup-instancerequirements-memorymib)" : MemoryMiBRequest,
  "[NetworkBandwidthGbps](#cfn-autoscaling-autoscalinggroup-instancerequirements-networkbandwidthgbps)" : NetworkBandwidthGbpsRequest,
  "[NetworkInterfaceCount](#cfn-autoscaling-autoscalinggroup-instancerequirements-networkinterfacecount)" : NetworkInterfaceCountRequest,
  "[OnDemandMaxPricePercentageOverLowestPrice](#cfn-autoscaling-autoscalinggroup-instancerequirements-ondemandmaxpricepercentageoverlowestprice)" : Integer,
  "[RequireHibernateSupport](#cfn-autoscaling-autoscalinggroup-instancerequirements-requirehibernatesupport)" : Boolean,
  "[SpotMaxPricePercentageOverLowestPrice](#cfn-autoscaling-autoscalinggroup-instancerequirements-spotmaxpricepercentageoverlowestprice)" : Integer,
  "[TotalLocalStorageGB](#cfn-autoscaling-autoscalinggroup-instancerequirements-totallocalstoragegb)" : TotalLocalStorageGBRequest,
  "[VCpuCount](#cfn-autoscaling-autoscalinggroup-instancerequirements-vcpucount)" : VCpuCountRequest
}
```

### YAML<a name="aws-properties-autoscaling-autoscalinggroup-instancerequirements-syntax.yaml"></a>

```
  [AcceleratorCount](#cfn-autoscaling-autoscalinggroup-instancerequirements-acceleratorcount): 
    AcceleratorCountRequest
  [AcceleratorManufacturers](#cfn-autoscaling-autoscalinggroup-instancerequirements-acceleratormanufacturers): 
    - String
  [AcceleratorNames](#cfn-autoscaling-autoscalinggroup-instancerequirements-acceleratornames): 
    - String
  [AcceleratorTotalMemoryMiB](#cfn-autoscaling-autoscalinggroup-instancerequirements-acceleratortotalmemorymib): 
    AcceleratorTotalMemoryMiBRequest
  [AcceleratorTypes](#cfn-autoscaling-autoscalinggroup-instancerequirements-acceleratortypes): 
    - String
  [AllowedInstanceTypes](#cfn-autoscaling-autoscalinggroup-instancerequirements-allowedinstancetypes): 
    - String
  [BareMetal](#cfn-autoscaling-autoscalinggroup-instancerequirements-baremetal): String
  [BaselineEbsBandwidthMbps](#cfn-autoscaling-autoscalinggroup-instancerequirements-baselineebsbandwidthmbps): 
    BaselineEbsBandwidthMbpsRequest
  [BurstablePerformance](#cfn-autoscaling-autoscalinggroup-instancerequirements-burstableperformance): String
  [CpuManufacturers](#cfn-autoscaling-autoscalinggroup-instancerequirements-cpumanufacturers): 
    - String
  [ExcludedInstanceTypes](#cfn-autoscaling-autoscalinggroup-instancerequirements-excludedinstancetypes): 
    - String
  [InstanceGenerations](#cfn-autoscaling-autoscalinggroup-instancerequirements-instancegenerations): 
    - String
  [LocalStorage](#cfn-autoscaling-autoscalinggroup-instancerequirements-localstorage): String
  [LocalStorageTypes](#cfn-autoscaling-autoscalinggroup-instancerequirements-localstoragetypes): 
    - String
  [MemoryGiBPerVCpu](#cfn-autoscaling-autoscalinggroup-instancerequirements-memorygibpervcpu): 
    MemoryGiBPerVCpuRequest
  [MemoryMiB](#cfn-autoscaling-autoscalinggroup-instancerequirements-memorymib): 
    MemoryMiBRequest
  [NetworkBandwidthGbps](#cfn-autoscaling-autoscalinggroup-instancerequirements-networkbandwidthgbps): 
    NetworkBandwidthGbpsRequest
  [NetworkInterfaceCount](#cfn-autoscaling-autoscalinggroup-instancerequirements-networkinterfacecount): 
    NetworkInterfaceCountRequest
  [OnDemandMaxPricePercentageOverLowestPrice](#cfn-autoscaling-autoscalinggroup-instancerequirements-ondemandmaxpricepercentageoverlowestprice): Integer
  [RequireHibernateSupport](#cfn-autoscaling-autoscalinggroup-instancerequirements-requirehibernatesupport): Boolean
  [SpotMaxPricePercentageOverLowestPrice](#cfn-autoscaling-autoscalinggroup-instancerequirements-spotmaxpricepercentageoverlowestprice): Integer
  [TotalLocalStorageGB](#cfn-autoscaling-autoscalinggroup-instancerequirements-totallocalstoragegb): 
    TotalLocalStorageGBRequest
  [VCpuCount](#cfn-autoscaling-autoscalinggroup-instancerequirements-vcpucount): 
    VCpuCountRequest
```

## Properties<a name="aws-properties-autoscaling-autoscalinggroup-instancerequirements-properties"></a>

`AcceleratorCount`  <a name="cfn-autoscaling-autoscalinggroup-instancerequirements-acceleratorcount"></a>
The minimum and maximum number of accelerators \(GPUs, FPGAs, or AWS Inferentia chips\) for an instance type\.  
To exclude accelerator\-enabled instance types, set `Max` to `0`\.  
Default: No minimum or maximum limits  
*Required*: No  
*Type*: [AcceleratorCountRequest](aws-properties-autoscaling-autoscalinggroup-acceleratorcountrequest.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AcceleratorManufacturers`  <a name="cfn-autoscaling-autoscalinggroup-instancerequirements-acceleratormanufacturers"></a>
Indicates whether instance types must have accelerators by specific manufacturers\.  
+ For instance types with NVIDIA devices, specify `nvidia`\.
+ For instance types with AMD devices, specify `amd`\.
+ For instance types with AWS devices, specify `amazon-web-services`\.
+ For instance types with Xilinx devices, specify `xilinx`\.
Default: Any manufacturer  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AcceleratorNames`  <a name="cfn-autoscaling-autoscalinggroup-instancerequirements-acceleratornames"></a>
Lists the accelerators that must be on an instance type\.  
+ For instance types with NVIDIA A100 GPUs, specify `a100`\.
+ For instance types with NVIDIA V100 GPUs, specify `v100`\.
+ For instance types with NVIDIA K80 GPUs, specify `k80`\.
+ For instance types with NVIDIA T4 GPUs, specify `t4`\.
+ For instance types with NVIDIA M60 GPUs, specify `m60`\.
+ For instance types with AMD Radeon Pro V520 GPUs, specify `radeon-pro-v520`\.
+ For instance types with Xilinx VU9P FPGAs, specify `vu9p`\.
Default: Any accelerator  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AcceleratorTotalMemoryMiB`  <a name="cfn-autoscaling-autoscalinggroup-instancerequirements-acceleratortotalmemorymib"></a>
The minimum and maximum total memory size for the accelerators on an instance type, in MiB\.  
Default: No minimum or maximum limits  
*Required*: No  
*Type*: [AcceleratorTotalMemoryMiBRequest](aws-properties-autoscaling-autoscalinggroup-acceleratortotalmemorymibrequest.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AcceleratorTypes`  <a name="cfn-autoscaling-autoscalinggroup-instancerequirements-acceleratortypes"></a>
Lists the accelerator types that must be on an instance type\.  
+ For instance types with GPU accelerators, specify `gpu`\.
+ For instance types with FPGA accelerators, specify `fpga`\.
+ For instance types with inference accelerators, specify `inference`\.
Default: Any accelerator type  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AllowedInstanceTypes`  <a name="cfn-autoscaling-autoscalinggroup-instancerequirements-allowedinstancetypes"></a>
The instance types to apply your specified attributes against\. All other instance types are ignored, even if they match your specified attributes\.  
You can use strings with one or more wild cards, represented by an asterisk \(`*`\), to allow an instance type, size, or generation\. The following are examples: `m5.8xlarge`, `c5*.*`, `m5a.*`, `r*`, `*3*`\.  
For example, if you specify `c5*`, Amazon EC2 Auto Scaling will allow the entire C5 instance family, which includes all C5a and C5n instance types\. If you specify `m5a.*`, Amazon EC2 Auto Scaling will allow all the M5a instance types, but not the M5n instance types\.  
If you specify `AllowedInstanceTypes`, you can't specify `ExcludedInstanceTypes`\.
Default: All instance types  
*Required*: No  
*Type*: List of String  
*Maximum*: `400`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BareMetal`  <a name="cfn-autoscaling-autoscalinggroup-instancerequirements-baremetal"></a>
Indicates whether bare metal instance types are included, excluded, or required\.  
Default: `excluded`   
*Required*: No  
*Type*: String  
*Allowed values*: `excluded | included | required`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BaselineEbsBandwidthMbps`  <a name="cfn-autoscaling-autoscalinggroup-instancerequirements-baselineebsbandwidthmbps"></a>
The minimum and maximum baseline bandwidth performance for an instance type, in Mbps\. For more information, see [Amazon EBS–optimized instances](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-optimized.html) in the *Amazon EC2 User Guide for Linux Instances*\.  
Default: No minimum or maximum limits  
*Required*: No  
*Type*: [BaselineEbsBandwidthMbpsRequest](aws-properties-autoscaling-autoscalinggroup-baselineebsbandwidthmbpsrequest.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BurstablePerformance`  <a name="cfn-autoscaling-autoscalinggroup-instancerequirements-burstableperformance"></a>
Indicates whether burstable performance instance types are included, excluded, or required\. For more information, see [Burstable performance instances](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/burstable-performance-instances.html) in the *Amazon EC2 User Guide for Linux Instances*\.  
Default: `excluded`   
*Required*: No  
*Type*: String  
*Allowed values*: `excluded | included | required`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CpuManufacturers`  <a name="cfn-autoscaling-autoscalinggroup-instancerequirements-cpumanufacturers"></a>
Lists which specific CPU manufacturers to include\.  
+ For instance types with Intel CPUs, specify `intel`\.
+ For instance types with AMD CPUs, specify `amd`\.
+ For instance types with AWS CPUs, specify `amazon-web-services`\.
Don't confuse the CPU hardware manufacturer with the CPU hardware architecture\. Instances will be launched with a compatible CPU architecture based on the Amazon Machine Image \(AMI\) that you specify in your launch template\. 
Default: Any manufacturer  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExcludedInstanceTypes`  <a name="cfn-autoscaling-autoscalinggroup-instancerequirements-excludedinstancetypes"></a>
The instance types to exclude\. You can use strings with one or more wild cards, represented by an asterisk \(`*`\), to exclude an instance family, type, size, or generation\. The following are examples: `m5.8xlarge`, `c5*.*`, `m5a.*`, `r*`, `*3*`\.   
For example, if you specify `c5*`, you are excluding the entire C5 instance family, which includes all C5a and C5n instance types\. If you specify `m5a.*`, Amazon EC2 Auto Scaling will exclude all the M5a instance types, but not the M5n instance types\.  
If you specify `ExcludedInstanceTypes`, you can't specify `AllowedInstanceTypes`\.
Default: No excluded instance types  
*Required*: No  
*Type*: List of String  
*Maximum*: `400`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceGenerations`  <a name="cfn-autoscaling-autoscalinggroup-instancerequirements-instancegenerations"></a>
Indicates whether current or previous generation instance types are included\.  
+ For current generation instance types, specify `current`\. The current generation includes EC2 instance types currently recommended for use\. This typically includes the latest two to three generations in each instance family\. For more information, see [Instance types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-types.html) in the *Amazon EC2 User Guide for Linux Instances*\.
+ For previous generation instance types, specify `previous`\.
Default: Any current or previous generation  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LocalStorage`  <a name="cfn-autoscaling-autoscalinggroup-instancerequirements-localstorage"></a>
Indicates whether instance types with instance store volumes are included, excluded, or required\. For more information, see [Amazon EC2 instance store](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/InstanceStorage.html) in the *Amazon EC2 User Guide for Linux Instances*\.  
Default: `included`   
*Required*: No  
*Type*: String  
*Allowed values*: `excluded | included | required`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LocalStorageTypes`  <a name="cfn-autoscaling-autoscalinggroup-instancerequirements-localstoragetypes"></a>
Indicates the type of local storage that is required\.  
+ For instance types with hard disk drive \(HDD\) storage, specify `hdd`\.
+ For instance types with solid state drive \(SSD\) storage, specify `ssd`\.
Default: Any local storage type  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MemoryGiBPerVCpu`  <a name="cfn-autoscaling-autoscalinggroup-instancerequirements-memorygibpervcpu"></a>
The minimum and maximum amount of memory per vCPU for an instance type, in GiB\.  
Default: No minimum or maximum limits  
*Required*: No  
*Type*: [MemoryGiBPerVCpuRequest](aws-properties-autoscaling-autoscalinggroup-memorygibpervcpurequest.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MemoryMiB`  <a name="cfn-autoscaling-autoscalinggroup-instancerequirements-memorymib"></a>
The minimum and maximum instance memory size for an instance type, in MiB\.  
*Required*: No  
*Type*: [MemoryMiBRequest](aws-properties-autoscaling-autoscalinggroup-memorymibrequest.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NetworkBandwidthGbps`  <a name="cfn-autoscaling-autoscalinggroup-instancerequirements-networkbandwidthgbps"></a>
The minimum and maximum amount of network bandwidth, in gigabits per second \(Gbps\)\.  
Default: No minimum or maximum limits  
*Required*: No  
*Type*: [NetworkBandwidthGbpsRequest](aws-properties-autoscaling-autoscalinggroup-networkbandwidthgbpsrequest.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NetworkInterfaceCount`  <a name="cfn-autoscaling-autoscalinggroup-instancerequirements-networkinterfacecount"></a>
The minimum and maximum number of network interfaces for an instance type\.  
Default: No minimum or maximum limits  
*Required*: No  
*Type*: [NetworkInterfaceCountRequest](aws-properties-autoscaling-autoscalinggroup-networkinterfacecountrequest.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OnDemandMaxPricePercentageOverLowestPrice`  <a name="cfn-autoscaling-autoscalinggroup-instancerequirements-ondemandmaxpricepercentageoverlowestprice"></a>
The price protection threshold for On\-Demand Instances\. This is the maximum you’ll pay for an On\-Demand Instance, expressed as a percentage higher than the least expensive current generation M, C, or R instance type with your specified attributes\. When Amazon EC2 Auto Scaling selects instance types with your attributes, we will exclude instance types whose price is higher than your threshold\. The parameter accepts an integer, which Amazon EC2 Auto Scaling interprets as a percentage\. To turn off price protection, specify a high value, such as `999999`\.   
If you set `DesiredCapacityType` to `vcpu` or `memory-mib`, the price protection threshold is applied based on the per vCPU or per memory price instead of the per instance price\.   
Default: `20`   
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RequireHibernateSupport`  <a name="cfn-autoscaling-autoscalinggroup-instancerequirements-requirehibernatesupport"></a>
Indicates whether instance types must provide On\-Demand Instance hibernation support\.  
Default: `false`   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SpotMaxPricePercentageOverLowestPrice`  <a name="cfn-autoscaling-autoscalinggroup-instancerequirements-spotmaxpricepercentageoverlowestprice"></a>
The price protection threshold for Spot Instances\. This is the maximum you’ll pay for a Spot Instance, expressed as a percentage higher than the least expensive current generation M, C, or R instance type with your specified attributes\. When Amazon EC2 Auto Scaling selects instance types with your attributes, we will exclude instance types whose price is higher than your threshold\. The parameter accepts an integer, which Amazon EC2 Auto Scaling interprets as a percentage\. To turn off price protection, specify a high value, such as `999999`\.   
If you set `DesiredCapacityType` to `vcpu` or `memory-mib`, the price protection threshold is applied based on the per vCPU or per memory price instead of the per instance price\.   
Default: `100`   
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TotalLocalStorageGB`  <a name="cfn-autoscaling-autoscalinggroup-instancerequirements-totallocalstoragegb"></a>
The minimum and maximum total local storage size for an instance type, in GB\.  
Default: No minimum or maximum limits  
*Required*: No  
*Type*: [TotalLocalStorageGBRequest](aws-properties-autoscaling-autoscalinggroup-totallocalstoragegbrequest.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VCpuCount`  <a name="cfn-autoscaling-autoscalinggroup-instancerequirements-vcpucount"></a>
The minimum and maximum number of vCPUs for an instance type\.  
*Required*: No  
*Type*: [VCpuCountRequest](aws-properties-autoscaling-autoscalinggroup-vcpucountrequest.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)