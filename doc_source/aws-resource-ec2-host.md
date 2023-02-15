# AWS::EC2::Host<a name="aws-resource-ec2-host"></a>

Allocates a fully dedicated physical server for launching EC2 instances\. Because the host is fully dedicated for your use, it can help you address compliance requirements and reduce costs by allowing you to use your existing server\-bound software licenses\. For more information, see [ Dedicated Hosts](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/dedicated-hosts-overview.html) in the *Amazon EC2 User Guide for Linux Instances*\.

## Syntax<a name="aws-resource-ec2-host-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-host-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::Host",
  "Properties" : {
      "[AutoPlacement](#cfn-ec2-host-autoplacement)" : String,
      "[AvailabilityZone](#cfn-ec2-host-availabilityzone)" : String,
      "[HostRecovery](#cfn-ec2-host-hostrecovery)" : String,
      "[InstanceFamily](#cfn-ec2-host-instancefamily)" : String,
      "[InstanceType](#cfn-ec2-host-instancetype)" : String,
      "[OutpostArn](#cfn-ec2-host-outpostarn)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-host-syntax.yaml"></a>

```
Type: AWS::EC2::Host
Properties: 
  [AutoPlacement](#cfn-ec2-host-autoplacement): String
  [AvailabilityZone](#cfn-ec2-host-availabilityzone): String
  [HostRecovery](#cfn-ec2-host-hostrecovery): String
  [InstanceFamily](#cfn-ec2-host-instancefamily): String
  [InstanceType](#cfn-ec2-host-instancetype): String
  [OutpostArn](#cfn-ec2-host-outpostarn): String
```

## Properties<a name="aws-resource-ec2-host-properties"></a>

`AutoPlacement`  <a name="cfn-ec2-host-autoplacement"></a>
Indicates whether the host accepts any untargeted instance launches that match its instance type configuration, or if it only accepts Host tenancy instance launches that specify its unique host ID\. For more information, see [ Understanding auto\-placement and affinity](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/how-dedicated-hosts-work.html#dedicated-hosts-understanding) in the *Amazon EC2 User Guide*\.  
Default: `on`   
*Required*: No  
*Type*: String  
*Allowed values*: `off | on`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AvailabilityZone`  <a name="cfn-ec2-host-availabilityzone"></a>
The Availability Zone in which to allocate the Dedicated Host\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`HostRecovery`  <a name="cfn-ec2-host-hostrecovery"></a>
Indicates whether to enable or disable host recovery for the Dedicated Host\. Host recovery is disabled by default\. For more information, see [ Host recovery](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/dedicated-hosts-recovery.html) in the *Amazon EC2 User Guide*\.  
Default: `off`   
*Required*: No  
*Type*: String  
*Allowed values*: `off | on`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceFamily`  <a name="cfn-ec2-host-instancefamily"></a>
The instance family supported by the Dedicated Host\. For example, `m5`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InstanceType`  <a name="cfn-ec2-host-instancetype"></a>
Specifies the instance type to be supported by the Dedicated Hosts\. If you specify an instance type, the Dedicated Hosts support instances of the specified instance type only\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`OutpostArn`  <a name="cfn-ec2-host-outpostarn"></a>
The Amazon Resource Name \(ARN\) of the AWS Outpost on which the Dedicated Host is allocated\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ec2-host-return-values"></a>

### Ref<a name="aws-resource-ec2-host-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the host ID, such as `h-0ab123c45d67ef89`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ec2-host-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ec2-host-return-values-fn--getatt-fn--getatt"></a>

`HostId`  <a name="HostId-fn::getatt"></a>
The ID of the host\.

## Examples<a name="aws-resource-ec2-host--examples"></a>

### Allocate a Dedicated Host<a name="aws-resource-ec2-host--examples--Allocate_a_Dedicated_Host"></a>

The following example allocates a dedicated host for `c3.large` instances in the `us-east-1a` Availability Zone\.

#### JSON<a name="aws-resource-ec2-host--examples--Allocate_a_Dedicated_Host--json"></a>

```
"Host" : {
  "Type" : "AWS::EC2::Host",
  "Properties" : {
    "AutoPlacement" : "on",
    "AvailabilityZone" : "us-east-1a",
    "InstanceType" : "c3.large"
  }
}
```

#### YAML<a name="aws-resource-ec2-host--examples--Allocate_a_Dedicated_Host--yaml"></a>

```
Host:
  Type: AWS::EC2::Host
  Properties: 
    AutoPlacement: on
    AvailabilityZone: us-east-1a
    InstanceType: c3.large
```