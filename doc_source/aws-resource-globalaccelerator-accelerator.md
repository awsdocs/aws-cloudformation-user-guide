# AWS::GlobalAccelerator::Accelerator<a name="aws-resource-globalaccelerator-accelerator"></a>

The `AWS::GlobalAccelerator::Accelerator` resource is a Global Accelerator resource type that contains information about how you create an accelerator\. An accelerator includes one or more listeners that process inbound connections and direct traffic to one or more endpoint groups, each of which includes endpoints, such as Application Load Balancers, Network Load Balancers, and Amazon EC2 instances\.

## Syntax<a name="aws-resource-globalaccelerator-accelerator-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-globalaccelerator-accelerator-syntax.json"></a>

```
{
  "Type" : "AWS::GlobalAccelerator::Accelerator",
  "Properties" : {
      "[Enabled](#cfn-globalaccelerator-accelerator-enabled)" : Boolean,
      "[IpAddresses](#cfn-globalaccelerator-accelerator-ipaddresses)" : [ String, ... ],
      "[IpAddressType](#cfn-globalaccelerator-accelerator-ipaddresstype)" : String,
      "[Name](#cfn-globalaccelerator-accelerator-name)" : String,
      "[Tags](#cfn-globalaccelerator-accelerator-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-globalaccelerator-accelerator-syntax.yaml"></a>

```
Type: AWS::GlobalAccelerator::Accelerator
Properties: 
  [Enabled](#cfn-globalaccelerator-accelerator-enabled): Boolean
  [IpAddresses](#cfn-globalaccelerator-accelerator-ipaddresses): 
    - String
  [IpAddressType](#cfn-globalaccelerator-accelerator-ipaddresstype): String
  [Name](#cfn-globalaccelerator-accelerator-name): String
  [Tags](#cfn-globalaccelerator-accelerator-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-globalaccelerator-accelerator-properties"></a>

`Enabled`  <a name="cfn-globalaccelerator-accelerator-enabled"></a>
Indicates whether the accelerator is enabled\. The value is true or false\. The default value is true\.   
If the value is set to true, the accelerator cannot be deleted\. If set to false, accelerator can be deleted\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IpAddresses`  <a name="cfn-globalaccelerator-accelerator-ipaddresses"></a>
Optionally, if you've added your own IP address pool to Global Accelerator \(BYOIP\), you can choose IP addresses from your own pool to use for the accelerator's static IP addresses when you create an accelerator\. You can specify one or two addresses, separated by a comma\. Do not include the /32 suffix\.  
Only one IP address from each of your IP address ranges can be used for each accelerator\. If you specify only one IP address from your IP address range, Global Accelerator assigns a second static IP address for the accelerator from the AWS IP address pool\.  
 Note that you can't update IP addresses for an existing accelerator\. To change them, you must create a new accelerator with the new addresses\.  
For more information, see [Bring Your Own IP Addresses \(BYOIP\)](https://docs.aws.amazon.com/global-accelerator/latest/dg/using-byoip.html) in the *AWS Global Accelerator Developer Guide*\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IpAddressType`  <a name="cfn-globalaccelerator-accelerator-ipaddresstype"></a>
The IP address type that an accelerator supports\. For a standard accelerator, the value can be IPV4 or DUAL\_STACK\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DUAL_STACK | IPV4`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-globalaccelerator-accelerator-name"></a>
The name of the accelerator\. The name must contain only alphanumeric characters or hyphens \(\-\), and must not begin or end with a hyphen\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `64`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-globalaccelerator-accelerator-tags"></a>
Create tags for an accelerator\.  
For more information, see [Tagging ](https://docs.aws.amazon.com/global-accelerator/latest/dg/tagging-in-global-accelerator.html) in the *AWS Global Accelerator Developer Guide*\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-globalaccelerator-accelerator-return-values"></a>

### Ref<a name="aws-resource-globalaccelerator-accelerator-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ARN of the accelerator, such as `arn:aws:globalaccelerator::012345678901:accelerator/1234abcd-abcd-1234-abcd-1234abcdefgh`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-globalaccelerator-accelerator-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-globalaccelerator-accelerator-return-values-fn--getatt-fn--getatt"></a>

`AcceleratorArn`  <a name="AcceleratorArn-fn::getatt"></a>
The ARN of the accelerator, such as `arn:aws:globalaccelerator::012345678901:accelerator/1234abcd-abcd-1234-abcd-1234abcdefgh`\.

`DnsName`  <a name="DnsName-fn::getatt"></a>
The Domain Name System \(DNS\) name that Global Accelerator creates that points to an accelerator's static IPv4 addresses\.

`DualStackDnsName`  <a name="DualStackDnsName-fn::getatt"></a>
The DNS name that Global Accelerator creates that points to a dual\-stack accelerator's four static IP addresses: two IPv4 addresses and two IPv6 addresses\.

`Ipv4Addresses`  <a name="Ipv4Addresses-fn::getatt"></a>
The array of IPv4 addresses in the IP address set\. An IP address set can have a maximum of two IP addresses\.

`Ipv6Addresses`  <a name="Ipv6Addresses-fn::getatt"></a>
The array of IPv6 addresses in the IP address set\. An IP address set can have a maximum of two IP addresses\.

## Examples<a name="aws-resource-globalaccelerator-accelerator--examples"></a>



### Add an accelerator<a name="aws-resource-globalaccelerator-accelerator--examples--Add_an_accelerator"></a>

These are examples to specify an accelerator\.

#### JSON<a name="aws-resource-globalaccelerator-accelerator--examples--Add_an_accelerator--json"></a>

```
"Resources": {
    "Accelerator": {
        "Type": "AWS::GlobalAccelerator::Accelerator",
        "Properties": {
            "Name": "SampleAccelerator",
            "Enabled": true
        }
    },
    "Outputs": {
        "AcceleratorDnsName": {
            "Description": "Accelerator DNS Name",
            "Value": {
                "Fn::GetAtt": [
                    "Accelerator",
                    "DnsName"
                ]
            }
        }
    }      
}
```

#### YAML<a name="aws-resource-globalaccelerator-accelerator--examples--Add_an_accelerator--yaml"></a>

```
Accelerator:
  Type: AWS::GlobalAccelerator::Accelerator
  Properties:
    Name: SampleAccelerator
    Enabled: true
Outputs:
  AcceleratorDnsName:
    Description: Accelerator DNS Name
    Value:
      Fn::GetAtt:
      - Accelerator
      - DnsName
```