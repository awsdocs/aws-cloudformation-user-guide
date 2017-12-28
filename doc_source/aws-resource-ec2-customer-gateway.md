# AWS::EC2::CustomerGateway<a name="aws-resource-ec2-customer-gateway"></a>

Provides information to AWS about your VPN customer gateway device\.


+ [Syntax](#aws-resource-ec2-customergateway-syntax)
+ [Properties](#w3ab2c21c10d342b9)
+ [Return Value](#w3ab2c21c10d342c11)
+ [Example](#w3ab2c21c10d342c13)
+ [See Also](#w3ab2c21c10d342c15)

## Syntax<a name="aws-resource-ec2-customergateway-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-customergateway-syntax.json"></a>

```
{
   "Type" : "AWS::EC2::CustomerGateway",
   "Properties" : {
      "BgpAsn" : Number,
      "IpAddress" : String,
      "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-customergateway-tags)" :  [ Resource Tag, ... ],
      "Type" : String
   }
}
```

### YAML<a name="aws-resource-ec2-customergateway-syntax.yaml"></a>

```
Type: "AWS::EC2::CustomerGateway"
Properties:
  BgpAsn: Number
  IpAddress: String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-customergateway-tags):
    Resource Tag
  Type: String
```

## Properties<a name="w3ab2c21c10d342b9"></a>

`BgpAsn`  
The customer gateway's Border Gateway Protocol \(BGP\) Autonomous System Number \(ASN\)\.  
*Required: *Yes  
*Type*: Number BgpAsn is always an integer value\.  
*Update requires*: Replacement

`IpAddress`  
The internet\-routable IP address for the customer gateway's outside interface\. The address must be static\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

`Tags`  
The tags that you want to attach to the resource\.  
*Required: *No  
*Type*: [AWS CloudFormation Resource Tags](aws-properties-resource-tags.md)\.  
*Update requires*: No interruption\.

`Type`  
The type of VPN connection that this customer gateway supports\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement  
*Example*: `ipsec.1`

## Return Value<a name="w3ab2c21c10d342c11"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\. For example:

```
{ "Ref": "MyResource" }
```

For the resource with the logical ID "MyResource", `Ref` will return the AWS resource name\.

For more information about using the `Ref` function, see Ref\.

## Example<a name="w3ab2c21c10d342c13"></a>

### JSON<a name="aws-resource-ec2-customergateway-example.json"></a>

```
{
   "AWSTemplateFormatVersion" : "2010-09-09",
   "Resources" : {
      "myCustomerGateway" : {
         "Type" : "AWS::EC2::CustomerGateway",
         "Properties" : {
            "Type" : "ipsec.1",
            "BgpAsn" : "64000",
            "IpAddress" : "1.1.1.1"
         }
      }
   }
}
```

### YAML<a name="aws-resource-ec2-customergateway-example.yaml"></a>

```
AWSTemplateFormatVersion: "2010-09-09"
Resources: 
  myCustomerGateway: 
    Type: "AWS::EC2::CustomerGateway"
    Properties: 
      Type: ipsec.1
      BgpAsn: 64000
      IpAddress: 1.1.1.1
```

## See Also<a name="w3ab2c21c10d342c15"></a>

+ [CreateCustomerGateway](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-CreateCustomerGateway.html) in the *Amazon EC2 API Reference*\.