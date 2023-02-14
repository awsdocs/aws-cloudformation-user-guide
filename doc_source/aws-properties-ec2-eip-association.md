# AWS::EC2::EIPAssociation<a name="aws-properties-ec2-eip-association"></a>

Associates an Elastic IP address with an instance or a network interface\. Before you can use an Elastic IP address, you must allocate it to your account\. For more information about working with Elastic IP addresses, see [ Elastic IP address concepts and rules](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-eips.html#vpc-eip-overview)\.

An Elastic IP address can be used in EC2\-Classic and EC2\-VPC accounts\. There are differences between an Elastic IP address that you use in a VPC and one that you use in EC2\-Classic\. For more information, see [ Differences between instances in EC2\-Classic and a VPC](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-classic-platform.html#differences-ec2-classic-vpc)\.

\[EC2\-VPC\] You must specify `AllocationId` and either `InstanceId`, `NetworkInterfaceId`, or `PrivateIpAddress`\.

\[EC2\-Classic\] You must specify `EIP` and `InstanceId`\.

## Syntax<a name="aws-properties-ec2-eip-association-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-eip-association-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::EIPAssociation",
  "Properties" : {
      "[AllocationId](#cfn-ec2-eipassociation-allocationid)" : String,
      "[EIP](#cfn-ec2-eipassociation-eip)" : String,
      "[InstanceId](#cfn-ec2-eipassociation-instanceid)" : String,
      "[NetworkInterfaceId](#cfn-ec2-eipassociation-networkinterfaceid)" : String,
      "[PrivateIpAddress](#cfn-ec2-eipassociation-PrivateIpAddress)" : String
    }
}
```

### YAML<a name="aws-properties-ec2-eip-association-syntax.yaml"></a>

```
Type: AWS::EC2::EIPAssociation
Properties: 
  [AllocationId](#cfn-ec2-eipassociation-allocationid): String
  [EIP](#cfn-ec2-eipassociation-eip): String
  [InstanceId](#cfn-ec2-eipassociation-instanceid): String
  [NetworkInterfaceId](#cfn-ec2-eipassociation-networkinterfaceid): String
  [PrivateIpAddress](#cfn-ec2-eipassociation-PrivateIpAddress): String
```

## Properties<a name="aws-properties-ec2-eip-association-properties"></a>

`AllocationId`  <a name="cfn-ec2-eipassociation-allocationid"></a>
\[EC2\-VPC\] The allocation ID\. This is required for EC2\-VPC\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`EIP`  <a name="cfn-ec2-eipassociation-eip"></a>
\[EC2\-Classic\] The Elastic IP address to associate with the instance\. This is required for EC2\-Classic\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`InstanceId`  <a name="cfn-ec2-eipassociation-instanceid"></a>
The ID of the instance\. The instance must have exactly one attached network interface\. For EC2\-VPC, you can specify either the instance ID or the network interface ID, but not both\. For EC2\-Classic, you must specify an instance ID and the instance must be in the running state\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`NetworkInterfaceId`  <a name="cfn-ec2-eipassociation-networkinterfaceid"></a>
\[EC2\-VPC\] The ID of the network interface\. If the instance has more than one network interface, you must specify a network interface ID\.  
For EC2\-VPC, you can specify either the instance ID or the network interface ID, but not both\.   
*Required*: Conditional  
*Type*: String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`PrivateIpAddress`  <a name="cfn-ec2-eipassociation-PrivateIpAddress"></a>
\[EC2\-VPC\] The primary or secondary private IP address to associate with the Elastic IP address\. If no private IP address is specified, the Elastic IP address is associated with the primary private IP address\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-properties-ec2-eip-association-return-values"></a>

### Ref<a name="aws-properties-ec2-eip-association-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-properties-ec2-eip-association--examples"></a>

### Associate an Elastic IP address to an instance<a name="aws-properties-ec2-eip-association--examples--Associate_an_Elastic_IP_address_to_an_instance"></a>

The following example creates an Elastic IP address and a network interface, and associates the Elastic IP address with the network interface\. The example uses the ID of an existing subnet and an example IP address from the subnet CIDR range\.

#### JSON<a name="aws-properties-ec2-eip-association--examples--Associate_an_Elastic_IP_address_to_an_instance--json"></a>

```
  "Resources" : {
    "myEIP" : {
        "Type" : "AWS::EC2::EIP",
        "Properties" : {
            "Domain" : "vpc"
        }
    },
    "myENI" : {
        "Type" : "AWS::EC2::NetworkInterface",
        "Properties" : {
            "SubnetId" : "subnet-0231a7e21ca967d2c",
            "PrivateIpAddress": "10.0.0.16"
        }
    },
    "eniAssociation" : {
        "Type" : "AWS::EC2::EIPAssociation",
        "Properties" : {
            "AllocationId" : { 
                "Fn::GetAtt" : [ "myEIP", "AllocationId" ]
            },
            "NetworkInterfaceId" : { 
                "Ref" : "myENI" 
            }
        }
    }
}
```

### <a name="aws-properties-ec2-eip-association--examples--"></a>

#### YAML<a name="aws-properties-ec2-eip-association--examples----yaml"></a>

```
Resources:
  myEIP:
    Type: AWS::EC2::EIP
    Properties:
      Domain: vpc
  myENI:
    Type: AWS::EC2::NetworkInterface
    Properties:
      SubnetId: subnet-0231a7e21ca967d2c
      PrivateIpAddress: 10.0.0.16
  eniAssociation:
    Type: AWS::EC2::EIPAssociation
    Properties:
      AllocationId: !GetAtt myEIP.AllocationId
      NetworkInterfaceId: !Ref myENI
```