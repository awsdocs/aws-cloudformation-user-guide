# AWS::Lightsail::Instance MonthlyTransfer<a name="aws-properties-lightsail-instance-monthlytransfer"></a>

`MonthlyTransfer` is a property of the [Networking](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lightsail-instance-networking.html) property\. It describes the amount of allocated monthly data transfer \(in GB\) for an instance\.

## Syntax<a name="aws-properties-lightsail-instance-monthlytransfer-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lightsail-instance-monthlytransfer-syntax.json"></a>

```
{
  "[GbPerMonthAllocated](#cfn-lightsail-instance-monthlytransfer-gbpermonthallocated)" : String
}
```

### YAML<a name="aws-properties-lightsail-instance-monthlytransfer-syntax.yaml"></a>

```
  [GbPerMonthAllocated](#cfn-lightsail-instance-monthlytransfer-gbpermonthallocated): String
```

## Properties<a name="aws-properties-lightsail-instance-monthlytransfer-properties"></a>

`GbPerMonthAllocated`  <a name="cfn-lightsail-instance-monthlytransfer-gbpermonthallocated"></a>
The amount of allocated monthly data transfer \(in GB\) for an instance\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)