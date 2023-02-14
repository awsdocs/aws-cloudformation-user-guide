# AWS::NetworkFirewall::Firewall SubnetMapping<a name="aws-properties-networkfirewall-firewall-subnetmapping"></a>

The ID for a subnet that you want to associate with the firewall\. AWS Network Firewall creates an instance of the associated firewall in each subnet that you specify, to filter traffic in the subnet's Availability Zone\.

## Syntax<a name="aws-properties-networkfirewall-firewall-subnetmapping-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkfirewall-firewall-subnetmapping-syntax.json"></a>

```
{
  "[SubnetId](#cfn-networkfirewall-firewall-subnetmapping-subnetid)" : String
}
```

### YAML<a name="aws-properties-networkfirewall-firewall-subnetmapping-syntax.yaml"></a>

```
  [SubnetId](#cfn-networkfirewall-firewall-subnetmapping-subnetid): String
```

## Properties<a name="aws-properties-networkfirewall-firewall-subnetmapping-properties"></a>

`SubnetId`  <a name="cfn-networkfirewall-firewall-subnetmapping-subnetid"></a>
The unique identifier for the subnet\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)