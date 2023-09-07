# AWS::EC2::EIPAssociation<a name="aws-resource-ec2-eipassociation"></a>

Associates an Elastic IP address with an instance or a network interface\. Before you can use an Elastic IP address, you must allocate it to your account\. For more information about working with Elastic IP addresses, see [ Elastic IP address concepts and rules](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-eips.html#vpc-eip-overview)\.

You must specify `AllocationId` and either `InstanceId`, `NetworkInterfaceId`, or `PrivateIpAddress`\.

## Syntax<a name="aws-resource-ec2-eipassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-eipassociation-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::EIPAssociation",
  "Properties" : {
      "[AllocationId](#cfn-ec2-eipassociation-allocationid)" : String,
      "[InstanceId](#cfn-ec2-eipassociation-instanceid)" : String,
      "[NetworkInterfaceId](#cfn-ec2-eipassociation-networkinterfaceid)" : String,
      "[PrivateIpAddress](#cfn-ec2-eipassociation-privateipaddress)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-eipassociation-syntax.yaml"></a>

```
Type: AWS::EC2::EIPAssociation
Properties: 
  [AllocationId](#cfn-ec2-eipassociation-allocationid): String
  [InstanceId](#cfn-ec2-eipassociation-instanceid): String
  [NetworkInterfaceId](#cfn-ec2-eipassociation-networkinterfaceid): String
  [PrivateIpAddress](#cfn-ec2-eipassociation-privateipaddress): String
```

## Properties<a name="aws-resource-ec2-eipassociation-properties"></a>

`AllocationId`  <a name="cfn-ec2-eipassociation-allocationid"></a>
The allocation ID\. This is required\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InstanceId`  <a name="cfn-ec2-eipassociation-instanceid"></a>
The ID of the instance\. The instance must have exactly one attached network interface\. You can specify either the instance ID or the network interface ID, but not both\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`NetworkInterfaceId`  <a name="cfn-ec2-eipassociation-networkinterfaceid"></a>
The ID of the network interface\. If the instance has more than one network interface, you must specify a network interface ID\.  
You can specify either the instance ID or the network interface ID, but not both\.   
*Required*: Conditional  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PrivateIpAddress`  <a name="cfn-ec2-eipassociation-privateipaddress"></a>
The primary or secondary private IP address to associate with the Elastic IP address\. If no private IP address is specified, the Elastic IP address is associated with the primary private IP address\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ec2-eipassociation-return-values"></a>

### Ref<a name="aws-resource-ec2-eipassociation-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the resource name\.

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ec2-eipassociation-return-values-fn--getatt"></a>

#### <a name="aws-resource-ec2-eipassociation-return-values-fn--getatt-fn--getatt"></a>

`Id`  <a name="Id-fn::getatt"></a>
Property description not available\.

## Examples<a name="aws-resource-ec2-eipassociation--examples"></a>

### Associate an Elastic IP address to an instance<a name="aws-resource-ec2-eipassociation--examples--Associate_an_Elastic_IP_address_to_an_instance"></a>

The following example creates an Elastic IP address and a network interface, and associates the Elastic IP address with the network interface\. The example uses the ID of an existing subnet and an example IP address from the subnet CIDR range\.

#### JSON<a name="aws-resource-ec2-eipassociation--examples--Associate_an_Elastic_IP_address_to_an_instance--json"></a>

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

### <a name="aws-resource-ec2-eipassociation--examples--"></a>

#### YAML<a name="aws-resource-ec2-eipassociation--examples----yaml"></a>

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