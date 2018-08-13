# AWS::EC2::EgressOnlyInternetGateway<a name="aws-resource-ec2-egressonlyinternetgateway"></a>

The `AWS::EC2::EgressOnlyInternetGateway` resource creates an egress\-only Internet gateway for your VPC \(over IPv6 only\)\. An egress\-only Internet gateway enables outbound communication over IPv6 from instances in your VPC to the Internet\. It also prevents hosts outside of your VPC from initiating an IPv6 connection with your instance\.

**Topics**
+ [Syntax](#aws-resource-ec2-egressonlyinternetgateway-syntax)
+ [Properties](#aws-resource-ec2-egressonlyinternetgateway-properties)
+ [Return Values](#w3ab2c21c10d387c11)
+ [Example](#aws-resource-ec2-egressonlyinternetgateway-examples)
+ [More Info](#w3ab2c21c10d387c15)

## Syntax<a name="aws-resource-ec2-egressonlyinternetgateway-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-egressonlyinternetgateway-syntax.json"></a>

```
{
  "Type": "AWS::EC2::EgressOnlyInternetGateway",
  "Properties": {
    "[VpcId](#cfn-ec2-egressonlyinternetgateway-vpcid)": String
  }
}
```

### YAML<a name="aws-resource-ec2-egressonlyinternetgateway-syntax.yaml"></a>

```
Type: "AWS::EC2::EgressOnlyInternetGateway"
Properties: 
  [VpcId](#cfn-ec2-egressonlyinternetgateway-vpcid): String
```

## Properties<a name="aws-resource-ec2-egressonlyinternetgateway-properties"></a>

`VpcId`  <a name="cfn-ec2-egressonlyinternetgateway-vpcid"></a>
The ID of the VPC for which to create the egress\-only Internet gateway\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Values<a name="w3ab2c21c10d387c11"></a>

### Ref<a name="w3ab2c21c10d387c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the ID of the egress\-only Internet gateway \(the physical resource ID\)\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="aws-resource-ec2-egressonlyinternetgateway-examples"></a>

The following example creates an egress\-only Internet gateway for the specified VPC\.

### JSON<a name="aws-resource-ec2-egressonlyinternetgateway-example.json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Resources": {
    "myEgressOnlyInternetGateway": {
      "Type": "AWS::EC2::EgressOnlyInternetGateway",
      "Properties": {
        "VpcId": "vpc-1a2b3c4d"
      }
    }
  }
}
```

### YAML<a name="aws-resource-ec2-egressonlyinternetgateway-example.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  myEgressOnlyInternetGateway:
    Type: "AWS::EC2::EgressOnlyInternetGateway"
    Properties:
      VpcId: vpc-1a2b3c4d
```

## More Info<a name="w3ab2c21c10d387c15"></a>
+ [CreateEgressOnlyInternetGateway](http://docs.aws.amazon.com//AWSEC2/latest/APIReference/API_CreateEgressOnlyInternetGateway.html) in the *Amazon EC2 API Reference*\.