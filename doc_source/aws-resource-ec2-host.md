# AWS::EC2::Host<a name="aws-resource-ec2-host"></a>

The `AWS::EC2::Host` resource allocates a fully dedicated physical server for launching EC2 instances\. Because the host is fully dedicated for your use, it can help you address compliance requirements and reduce costs by allowing you to use your existing server\-bound software licenses\. For more information, see [Dedicated Hosts](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/dedicated-hosts-overview.html) in the *Amazon EC2 User Guide for Linux Instances*\.


+ [Syntax](#aws-resource-ec2-host-syntax)
+ [Properties](#w3ab2c21c10d368b9)
+ [Return Value](#w3ab2c21c10d368c11)
+ [Example](#w3ab2c21c10d368c13)

## Syntax<a name="aws-resource-ec2-host-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-host-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::Host",
  "Properties" : {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-host-autoplacement)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-host-availabilityzone)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-host-instancetype)" : String
  }
}
```

### YAML<a name="aws-resource-ec2-host-syntax.yaml"></a>

```
Type: "AWS::EC2::Host"
Properties: 
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-host-autoplacement): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-host-availabilityzone): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-host-instancetype): String
```

## Properties<a name="w3ab2c21c10d368b9"></a>

`AutoPlacement`  
Indicates if the host accepts EC2 instances with only matching configurations or if instances must also specify the host ID\. Instances that don't specify a host ID can't launch onto a host with `AutoPlacement` set to `off`\. By default, AWS CloudFormation sets this property to `on`\. For more information, see [Understanding Instance Placement and Host Affinity](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/dedicated-hosts-instance-placement.html) in the *Amazon EC2 User Guide for Linux Instances*\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`AvailabilityZone`  
The Availability Zone \(AZ\) in which to launch the dedicated host\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

`InstanceType`  
The instance type that the dedicated host accepts\. Only instances of this type can be launched onto the host\. For more information, see [Supported Instance Types](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/dedicated-hosts-overview.html#dedicated-hosts-supported-instance-types) in the *Amazon EC2 User Guide for Linux Instances*\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

## Return Value<a name="w3ab2c21c10d368c11"></a>

### Ref<a name="w3ab2c21c10d368c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the host ID, such as `h-0ab123c45d67ef89`\.

For more information about using the `Ref` function, see Ref\.

## Example<a name="w3ab2c21c10d368c13"></a>

The following example allocates a dedicated host for `c3.large` instances in the `us-east-1a` Availability Zone\.

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