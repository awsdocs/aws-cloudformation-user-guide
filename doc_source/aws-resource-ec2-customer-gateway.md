# AWS::EC2::CustomerGateway<a name="aws-resource-ec2-customer-gateway"></a>

Specifies a customer gateway\.

## Syntax<a name="aws-resource-ec2-customer-gateway-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-customer-gateway-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::CustomerGateway",
  "Properties" : {
      "[BgpAsn](#cfn-ec2-customergateway-bgpasn)" : Integer,
      "[IpAddress](#cfn-ec2-customergateway-ipaddress)" : String,
      "[Tags](#cfn-ec2-customergateway-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Type](#cfn-ec2-customergateway-type)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-customer-gateway-syntax.yaml"></a>

```
Type: AWS::EC2::CustomerGateway
Properties: 
  [BgpAsn](#cfn-ec2-customergateway-bgpasn): Integer
  [IpAddress](#cfn-ec2-customergateway-ipaddress): String
  [Tags](#cfn-ec2-customergateway-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Type](#cfn-ec2-customergateway-type): String
```

## Properties<a name="aws-resource-ec2-customer-gateway-properties"></a>

`BgpAsn`  <a name="cfn-ec2-customergateway-bgpasn"></a>
For devices that support BGP, the customer gateway's BGP ASN\.  
Default: 65000  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`IpAddress`  <a name="cfn-ec2-customergateway-ipaddress"></a>
The Internet\-routable IP address for the customer gateway's outside interface\. The address must be static\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-ec2-customergateway-tags"></a>
One or more tags for the customer gateway\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-ec2-customergateway-type"></a>
The type of VPN connection that this customer gateway supports \(`ipsec.1`\)\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `ipsec.1`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ec2-customer-gateway-return-values"></a>

### Ref<a name="aws-resource-ec2-customer-gateway-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the customer gateway\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-ec2-customer-gateway--examples"></a>

### <a name="aws-resource-ec2-customer-gateway--examples--"></a>



#### YAML<a name="aws-resource-ec2-customer-gateway--examples----yaml"></a>

```
myCustomerGateway: 
    Type: AWS::EC2::CustomerGateway
    Properties: 
        Type: ipsec.1
        BgpAsn: 65534
        IpAddress: 12.1.2.3
```

### <a name="aws-resource-ec2-customer-gateway--examples--"></a>



#### JSON<a name="aws-resource-ec2-customer-gateway--examples----json"></a>

```
{
    "myCustomerGateway" : {
        "Type" : "AWS::EC2::CustomerGateway",
        "Properties" : {
            "Type" : "ipsec.1",
            "BgpAsn" : "65534",
            "IpAddress" : "12.1.2.3"
        }
    }
}
```

## See also<a name="aws-resource-ec2-customer-gateway--seealso"></a>
+  [CreateCustomerGateway](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-CreateCustomerGateway.html) in the *Amazon Elastic Compute Cloud API Reference* 

