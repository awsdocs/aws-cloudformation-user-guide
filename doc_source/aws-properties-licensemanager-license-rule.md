# AWS::LicenseManager::License Rule<a name="aws-properties-licensemanager-license-rule"></a>

The `Rule` property type defines a license rule\. The syntax is \#name=value \(for example, \#allowedTenancy=EC2\-DedicatedHost\)\. The available rules vary by dimension, as follows\.
+ `Cores` dimension: `allowedTenancy` \| `licenseAffinityToHost` \| `maximumCores` \| `minimumCores`
+ `Instances` dimension: `allowedTenancy` \| `maximumCores` \| `minimumCores` \| `maximumSockets` \| `minimumSockets` \| `maximumVcpus` \| `minimumVcpus`
+ `Sockets` dimension: `allowedTenancy` \| `licenseAffinityToHost` \| `maximumSockets` \| `minimumSockets`
+ `vCPUs` dimension: `allowedTenancy` \| `honorVcpuOptimization` \| `maximumVcpus` \| `minimumVcpus`

The unit for licenseAffinityToHost is days and the range is 1 to 180\. The possible values for allowedTenancy are EC2\-Default, EC2\-DedicatedHost, and EC2\-DedicatedInstance\. The possible values for honorVcpuOptimization are True and False\.

## Syntax<a name="aws-properties-licensemanager-license-rule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-licensemanager-license-rule-syntax.json"></a>

```
{
  "[Name](#cfn-licensemanager-license-rule-name)" : String,
  "[Unit](#cfn-licensemanager-license-rule-unit)" : String,
  "[Value](#cfn-licensemanager-license-rule-value)" : String
}
```

### YAML<a name="aws-properties-licensemanager-license-rule-syntax.yaml"></a>

```
  [Name](#cfn-licensemanager-license-rule-name): String
  [Unit](#cfn-licensemanager-license-rule-unit): String
  [Value](#cfn-licensemanager-license-rule-value): String
```

## Properties<a name="aws-properties-licensemanager-license-rule-properties"></a>

`Name`  <a name="cfn-licensemanager-license-rule-name"></a>
The license rule name\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Unit`  <a name="cfn-licensemanager-license-rule-unit"></a>
The license rule unit\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-licensemanager-license-rule-value"></a>
The license rule value\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)