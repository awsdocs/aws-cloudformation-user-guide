# AWS::EC2::TransitGatewayMulticastDomain Options<a name="aws-properties-ec2-transitgatewaymulticastdomain-options"></a>

The options for the transit gateway multicast domain\.

## Syntax<a name="aws-properties-ec2-transitgatewaymulticastdomain-options-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-transitgatewaymulticastdomain-options-syntax.json"></a>

```
{
  "[AutoAcceptSharedAssociations](#cfn-ec2-transitgatewaymulticastdomain-options-autoacceptsharedassociations)" : String,
  "[Igmpv2Support](#cfn-ec2-transitgatewaymulticastdomain-options-igmpv2support)" : String,
  "[StaticSourcesSupport](#cfn-ec2-transitgatewaymulticastdomain-options-staticsourcessupport)" : String
}
```

### YAML<a name="aws-properties-ec2-transitgatewaymulticastdomain-options-syntax.yaml"></a>

```
  [AutoAcceptSharedAssociations](#cfn-ec2-transitgatewaymulticastdomain-options-autoacceptsharedassociations): String
  [Igmpv2Support](#cfn-ec2-transitgatewaymulticastdomain-options-igmpv2support): String
  [StaticSourcesSupport](#cfn-ec2-transitgatewaymulticastdomain-options-staticsourcessupport): String
```

## Properties<a name="aws-properties-ec2-transitgatewaymulticastdomain-options-properties"></a>

`AutoAcceptSharedAssociations`  <a name="cfn-ec2-transitgatewaymulticastdomain-options-autoacceptsharedassociations"></a>
Indicates whether to automatically accept cross\-account subnet associations that are associated with the transit gateway multicast domain\.  
*Required*: No  
*Type*: String  
*Allowed values*: `disable | enable`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Igmpv2Support`  <a name="cfn-ec2-transitgatewaymulticastdomain-options-igmpv2support"></a>
Specify whether to enable Internet Group Management Protocol \(IGMP\) version 2 for the transit gateway multicast domain\.  
*Required*: No  
*Type*: String  
*Allowed values*: `disable | enable`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StaticSourcesSupport`  <a name="cfn-ec2-transitgatewaymulticastdomain-options-staticsourcessupport"></a>
Specify whether to enable support for statically configuring multicast group sources for a domain\.  
*Required*: No  
*Type*: String  
*Allowed values*: `disable | enable`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)