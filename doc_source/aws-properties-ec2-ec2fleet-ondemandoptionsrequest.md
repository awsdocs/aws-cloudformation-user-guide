# Amazon EC2 EC2Fleet OnDemandOptionsRequest<a name="aws-properties-ec2-ec2fleet-ondemandoptionsrequest"></a>

<a name="aws-properties-ec2-ec2fleet-ondemandoptionsrequest-description"></a>The `OnDemandOptionsRequest` property type specifies the allocation strategy of On\-Demand Instances in an EC2 Fleet\.

<a name="aws-properties-ec2-ec2fleet-ondemandoptionsrequest-inheritance"></a> `OnDemandOptionsRequest` is a property of the [AWS::EC2::EC2Fleet](aws-resource-ec2-ec2fleet.md) resource\.

## Syntax<a name="aws-properties-ec2-ec2fleet-ondemandoptionsrequest-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-ec2fleet-ondemandoptionsrequest-syntax.json"></a>

```
{
  "[AllocationStrategy](#cfn-ec2-ec2fleet-ondemandoptionsrequest-allocationstrategy)" : String
}
```

### YAML<a name="aws-properties-ec2-ec2fleet-ondemandoptionsrequest-syntax.yaml"></a>

```
[AllocationStrategy](#cfn-ec2-ec2fleet-ondemandoptionsrequest-allocationstrategy): String
```

## Properties<a name="aws-properties-ec2-ec2fleet-ondemandoptionsrequest-properties"></a>

`AllocationStrategy`  <a name="cfn-ec2-ec2fleet-ondemandoptionsrequest-allocationstrategy"></a>
The order of the launch template overrides to use in fulfilling On\-Demand capacity\. If you specify `lowest-price`, EC2 Fleet uses price to determine the order, launching the lowest price first\. If you specify `prioritized`, EC2 Fleet uses the priority that you assigned to each launch template override, launching the highest priority first\. If you do not specify a value, EC2 Fleet defaults to `lowest-price.`  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-ec2-ec2fleet-ondemandoptionsrequest-seealso"></a>
+ [OnDemandOptionsRequest](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_OnDemandOptionsRequest.html) in the *Amazon EC2 API Reference*