# AWS::EC2::VPCDHCPOptionsAssociation<a name="aws-resource-ec2-vpcdhcpoptionsassociation"></a>

Associates a set of DHCP options with a VPC, or associates no DHCP options with the VPC\.

After you associate the options with the VPC, any existing instances and all new instances that you launch in that VPC use the options\. You don't need to restart or relaunch the instances\. They automatically pick up the changes within a few hours, depending on how frequently the instance renews its DHCP lease\. You can explicitly renew the lease using the operating system on the instance\.

## Syntax<a name="aws-resource-ec2-vpcdhcpoptionsassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-vpcdhcpoptionsassociation-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::VPCDHCPOptionsAssociation",
  "Properties" : {
      "[DhcpOptionsId](#cfn-ec2-vpcdhcpoptionsassociation-dhcpoptionsid)" : String,
      "[VpcId](#cfn-ec2-vpcdhcpoptionsassociation-vpcid)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-vpcdhcpoptionsassociation-syntax.yaml"></a>

```
Type: AWS::EC2::VPCDHCPOptionsAssociation
Properties: 
  [DhcpOptionsId](#cfn-ec2-vpcdhcpoptionsassociation-dhcpoptionsid): String
  [VpcId](#cfn-ec2-vpcdhcpoptionsassociation-vpcid): String
```

## Properties<a name="aws-resource-ec2-vpcdhcpoptionsassociation-properties"></a>

`DhcpOptionsId`  <a name="cfn-ec2-vpcdhcpoptionsassociation-dhcpoptionsid"></a>
The ID of the DHCP options set, or `default` to associate no DHCP options with the VPC\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VpcId`  <a name="cfn-ec2-vpcdhcpoptionsassociation-vpcid"></a>
The ID of the VPC\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ec2-vpcdhcpoptionsassociation-return-values"></a>

### Ref<a name="aws-resource-ec2-vpcdhcpoptionsassociation-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the DHCP options association\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ec2-vpcdhcpoptionsassociation-return-values-fn--getatt"></a>

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

#### <a name="aws-resource-ec2-vpcdhcpoptionsassociation-return-values-fn--getatt-fn--getatt"></a>

`Id`  <a name="Id-fn::getatt"></a>
The ID of the DHCP options set\.

## Examples<a name="aws-resource-ec2-vpcdhcpoptionsassociation--examples"></a>



### VPC DHCP options association<a name="aws-resource-ec2-vpcdhcpoptionsassociation--examples--VPC_DHCP_options_association"></a>

The following example uses the `Ref` intrinsic function to associate the myDHCPOptions DHCP options with the myVPC VPC\. The VPC and DHCP options can be declared in the same template or added as input parameters\. For more information about the VPC or the DHCP options resources, see AWS::EC2::VPC or AWS::EC2::DHCPOptions\. 

#### JSON<a name="aws-resource-ec2-vpcdhcpoptionsassociation--examples--VPC_DHCP_options_association--json"></a>

```
"myVPCDHCPOptionsAssociation" : {
     "Type" : "AWS::EC2::VPCDHCPOptionsAssociation",
      "Properties" : {
         "VpcId" : {"Ref" : "myVPC"},
         "DhcpOptionsId" : {"Ref" : "myDHCPOptions"}
         }
}
```

#### YAML<a name="aws-resource-ec2-vpcdhcpoptionsassociation--examples--VPC_DHCP_options_association--yaml"></a>

```
myVPCDHCPOptionsAssociation:
  Type: AWS::EC2::VPCDHCPOptionsAssociation
  Properties:
    VpcId:
       Ref: myVPC
    DhcpOptionsId:
       Ref: myDHCPOptions
```

## See also<a name="aws-resource-ec2-vpcdhcpoptionsassociation--seealso"></a>
+  [AssociateDhcpOptions](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_AssociateDhcpOptions.html) in the *Amazon EC2 API Reference*
+ [DHCP options sets](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_DHCP_Options.html) in the *Amazon VPC User Guide*

