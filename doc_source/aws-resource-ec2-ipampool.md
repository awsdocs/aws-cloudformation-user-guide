# AWS::EC2::IPAMPool<a name="aws-resource-ec2-ipampool"></a>

In IPAM, a pool is a collection of contiguous IP addresses CIDRs\. Pools enable you to organize your IP addresses according to your routing and security needs\. For example, if you have separate routing and security needs for development and production applications, you can create a pool for each\.

## Syntax<a name="aws-resource-ec2-ipampool-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-ipampool-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::IPAMPool",
  "Properties" : {
      "[AddressFamily](#cfn-ec2-ipampool-addressfamily)" : String,
      "[AllocationDefaultNetmaskLength](#cfn-ec2-ipampool-allocationdefaultnetmasklength)" : Integer,
      "[AllocationMaxNetmaskLength](#cfn-ec2-ipampool-allocationmaxnetmasklength)" : Integer,
      "[AllocationMinNetmaskLength](#cfn-ec2-ipampool-allocationminnetmasklength)" : Integer,
      "[AllocationResourceTags](#cfn-ec2-ipampool-allocationresourcetags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[AutoImport](#cfn-ec2-ipampool-autoimport)" : Boolean,
      "[AwsService](#cfn-ec2-ipampool-awsservice)" : String,
      "[Description](#cfn-ec2-ipampool-description)" : String,
      "[IpamScopeId](#cfn-ec2-ipampool-ipamscopeid)" : String,
      "[Locale](#cfn-ec2-ipampool-locale)" : String,
      "[ProvisionedCidrs](#cfn-ec2-ipampool-provisionedcidrs)" : [ ProvisionedCidr, ... ],
      "[PublicIpSource](#cfn-ec2-ipampool-publicipsource)" : String,
      "[PubliclyAdvertisable](#cfn-ec2-ipampool-publiclyadvertisable)" : Boolean,
      "[SourceIpamPoolId](#cfn-ec2-ipampool-sourceipampoolid)" : String,
      "[Tags](#cfn-ec2-ipampool-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-ec2-ipampool-syntax.yaml"></a>

```
Type: AWS::EC2::IPAMPool
Properties: 
  [AddressFamily](#cfn-ec2-ipampool-addressfamily): String
  [AllocationDefaultNetmaskLength](#cfn-ec2-ipampool-allocationdefaultnetmasklength): Integer
  [AllocationMaxNetmaskLength](#cfn-ec2-ipampool-allocationmaxnetmasklength): Integer
  [AllocationMinNetmaskLength](#cfn-ec2-ipampool-allocationminnetmasklength): Integer
  [AllocationResourceTags](#cfn-ec2-ipampool-allocationresourcetags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [AutoImport](#cfn-ec2-ipampool-autoimport): Boolean
  [AwsService](#cfn-ec2-ipampool-awsservice): String
  [Description](#cfn-ec2-ipampool-description): String
  [IpamScopeId](#cfn-ec2-ipampool-ipamscopeid): String
  [Locale](#cfn-ec2-ipampool-locale): String
  [ProvisionedCidrs](#cfn-ec2-ipampool-provisionedcidrs): 
    - ProvisionedCidr
  [PublicIpSource](#cfn-ec2-ipampool-publicipsource): String
  [PubliclyAdvertisable](#cfn-ec2-ipampool-publiclyadvertisable): Boolean
  [SourceIpamPoolId](#cfn-ec2-ipampool-sourceipampoolid): String
  [Tags](#cfn-ec2-ipampool-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-ec2-ipampool-properties"></a>

`AddressFamily`  <a name="cfn-ec2-ipampool-addressfamily"></a>
The address family of the pool\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `ipv4 | ipv6`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`AllocationDefaultNetmaskLength`  <a name="cfn-ec2-ipampool-allocationdefaultnetmasklength"></a>
The default netmask length for allocations added to this pool\. If, for example, the CIDR assigned to this pool is 10\.0\.0\.0/8 and you enter 16 here, new allocations will default to 10\.0\.0\.0/16\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AllocationMaxNetmaskLength`  <a name="cfn-ec2-ipampool-allocationmaxnetmasklength"></a>
The maximum netmask length possible for CIDR allocations in this IPAM pool to be compliant\. The maximum netmask length must be greater than the minimum netmask length\. Possible netmask lengths for IPv4 addresses are 0 \- 32\. Possible netmask lengths for IPv6 addresses are 0 \- 128\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AllocationMinNetmaskLength`  <a name="cfn-ec2-ipampool-allocationminnetmasklength"></a>
The minimum netmask length required for CIDR allocations in this IPAM pool to be compliant\. The minimum netmask length must be less than the maximum netmask length\. Possible netmask lengths for IPv4 addresses are 0 \- 32\. Possible netmask lengths for IPv6 addresses are 0 \- 128\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AllocationResourceTags`  <a name="cfn-ec2-ipampool-allocationresourcetags"></a>
Tags that are required for resources that use CIDRs from this IPAM pool\. Resources that do not have these tags will not be allowed to allocate space from the pool\. If the resources have their tags changed after they have allocated space or if the allocation tagging requirements are changed on the pool, the resource may be marked as noncompliant\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AutoImport`  <a name="cfn-ec2-ipampool-autoimport"></a>
If selected, IPAM will continuously look for resources within the CIDR range of this pool and automatically import them as allocations into your IPAM\. The CIDRs that will be allocated for these resources must not already be allocated to other resources in order for the import to succeed\. IPAM will import a CIDR regardless of its compliance with the pool's allocation rules, so a resource might be imported and subsequently marked as noncompliant\. If IPAM discovers multiple CIDRs that overlap, IPAM will import the largest CIDR only\. If IPAM discovers multiple CIDRs with matching CIDRs, IPAM will randomly import one of them only\.   
A locale must be set on the pool for this feature to work\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AwsService`  <a name="cfn-ec2-ipampool-awsservice"></a>
Limits which service in AWS that the pool can be used in\. "ec2", for example, allows users to use space for Elastic IP addresses and VPCs\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ec2`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-ec2-ipampool-description"></a>
The description of the IPAM pool\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IpamScopeId`  <a name="cfn-ec2-ipampool-ipamscopeid"></a>
The ID of the scope in which you would like to create the IPAM pool\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Locale`  <a name="cfn-ec2-ipampool-locale"></a>
The locale of the IPAM pool\. In IPAM, the locale is the AWS Region where you want to make an IPAM pool available for allocations\. Only resources in the same Region as the locale of the pool can get IP address allocations from the pool\. You can only allocate a CIDR for a VPC, for example, from an IPAM pool that shares a locale with the VPC’s Region\. Note that once you choose a Locale for a pool, you cannot modify it\. If you choose an AWS Region for locale that has not been configured as an operating Region for the IPAM, you'll get an error\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ProvisionedCidrs`  <a name="cfn-ec2-ipampool-provisionedcidrs"></a>
Information about the CIDRs provisioned to an IPAM pool\.  
*Required*: No  
*Type*: List of [ProvisionedCidr](aws-properties-ec2-ipampool-provisionedcidr.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PublicIpSource`  <a name="cfn-ec2-ipampool-publicipsource"></a>
The IP address source for pools in the public scope\. Only used for provisioning IP address CIDRs to pools in the public scope\. Default is `BYOIP`\. For more information, see [Create IPv6 pools](https://docs.aws.amazon.com/vpc/latest/ipam/intro-create-ipv6-pools.html) in the *Amazon VPC IPAM User Guide*\. By default, you can add only one Amazon\-provided IPv6 CIDR block to a top\-level IPv6 pool\. For information on increasing the default limit, see [ Quotas for your IPAM](https://docs.aws.amazon.com/vpc/latest/ipam/quotas-ipam.html) in the *Amazon VPC IPAM User Guide*\.  
*Required*: No  
*Type*: String  
*Allowed values*: `amazon | byoip`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PubliclyAdvertisable`  <a name="cfn-ec2-ipampool-publiclyadvertisable"></a>
Determines if a pool is publicly advertisable\. This option is not available for pools with AddressFamily set to `ipv4`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SourceIpamPoolId`  <a name="cfn-ec2-ipampool-sourceipampoolid"></a>
The ID of the source IPAM pool\. You can use this option to create an IPAM pool within an existing source pool\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-ec2-ipampool-tags"></a>
The key/value combination of a tag assigned to the resource\. Use the tag key in the filter name and the tag value as the filter value\. For example, to find all resources that have a tag with the key `Owner` and the value `TeamA`, specify `tag:Owner` for the filter name and `TeamA` for the filter value\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ec2-ipampool-return-values"></a>

### Ref<a name="aws-resource-ec2-ipampool-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the IPAM pool ID\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ec2-ipampool-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ec2-ipampool-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the IPAM pool\.

`IpamArn`  <a name="IpamArn-fn::getatt"></a>
The ARN of the IPAM\.

`IpamPoolId`  <a name="IpamPoolId-fn::getatt"></a>
The ID of the IPAM pool\.

`IpamScopeArn`  <a name="IpamScopeArn-fn::getatt"></a>
The ARN of the scope of the IPAM pool\.

`IpamScopeType`  <a name="IpamScopeType-fn::getatt"></a>
The scope of the IPAM\.

`PoolDepth`  <a name="PoolDepth-fn::getatt"></a>
The depth of pools in your IPAM pool\. The pool depth quota is 10\.

`State`  <a name="State-fn::getatt"></a>
The state of the IPAM pool\.

`StateMessage`  <a name="StateMessage-fn::getatt"></a>
A message related to the failed creation of an IPAM pool\.