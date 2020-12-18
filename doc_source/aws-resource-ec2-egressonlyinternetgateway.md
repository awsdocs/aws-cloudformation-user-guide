# AWS::EC2::EgressOnlyInternetGateway<a name="aws-resource-ec2-egressonlyinternetgateway"></a>

\[IPv6 only\] Specifies an egress\-only internet gateway for your VPC\. An egress\-only internet gateway is used to enable outbound communication over IPv6 from instances in your VPC to the internet, and prevents hosts outside of your VPC from initiating an IPv6 connection with your instance\.

## Syntax<a name="aws-resource-ec2-egressonlyinternetgateway-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-egressonlyinternetgateway-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::EgressOnlyInternetGateway",
  "Properties" : {
      "[VpcId](#cfn-ec2-egressonlyinternetgateway-vpcid)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-egressonlyinternetgateway-syntax.yaml"></a>

```
Type: AWS::EC2::EgressOnlyInternetGateway
Properties: 
  [VpcId](#cfn-ec2-egressonlyinternetgateway-vpcid): String
```

## Properties<a name="aws-resource-ec2-egressonlyinternetgateway-properties"></a>

`VpcId`  <a name="cfn-ec2-egressonlyinternetgateway-vpcid"></a>
The ID of the VPC for which to create the egress\-only internet gateway\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ec2-egressonlyinternetgateway-return-values"></a>

### Ref<a name="aws-resource-ec2-egressonlyinternetgateway-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the egress\-only Internet gateway \(the physical resource ID\)\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-ec2-egressonlyinternetgateway--examples"></a>

### <a name="aws-resource-ec2-egressonlyinternetgateway--examples--"></a>



#### YAML<a name="aws-resource-ec2-egressonlyinternetgateway--examples----yaml"></a>

```
myEgressOnlyInternetGateway: 
    Type: AWS::EC2::EgressOnlyInternetGateway
    Properties: 
        VpcId: vpc-1a2b3c4d
```

### <a name="aws-resource-ec2-egressonlyinternetgateway--examples--"></a>



#### JSON<a name="aws-resource-ec2-egressonlyinternetgateway--examples----json"></a>

```
{
    "myEgressOnlyInternetGateway" : {
        "Type" : "AWS::EC2::EgressOnlyInternetGateway",
        "Properties" : {
            "VpcId" : "vpc-1a2b3c4d"
        }
    }
}
```

## See also<a name="aws-resource-ec2-egressonlyinternetgateway--seealso"></a>
+  [CreateEgressOnlyInternetGateway](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-CreateEgressOnlyInternetGateway.html) in the *Amazon Elastic Compute Cloud API Reference* 

