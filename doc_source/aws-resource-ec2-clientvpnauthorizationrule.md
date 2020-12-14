# AWS::EC2::ClientVpnAuthorizationRule<a name="aws-resource-ec2-clientvpnauthorizationrule"></a>

Specifies an ingress authorization rule to add to a Client VPN endpoint\. Ingress authorization rules act as firewall rules that grant access to networks\. You must configure ingress authorization rules to enable clients to access resources in AWS or on\-premises networks\.

## Syntax<a name="aws-resource-ec2-clientvpnauthorizationrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-clientvpnauthorizationrule-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::ClientVpnAuthorizationRule",
  "Properties" : {
      "[AccessGroupId](#cfn-ec2-clientvpnauthorizationrule-accessgroupid)" : String,
      "[AuthorizeAllGroups](#cfn-ec2-clientvpnauthorizationrule-authorizeallgroups)" : Boolean,
      "[ClientVpnEndpointId](#cfn-ec2-clientvpnauthorizationrule-clientvpnendpointid)" : String,
      "[Description](#cfn-ec2-clientvpnauthorizationrule-description)" : String,
      "[TargetNetworkCidr](#cfn-ec2-clientvpnauthorizationrule-targetnetworkcidr)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-clientvpnauthorizationrule-syntax.yaml"></a>

```
Type: AWS::EC2::ClientVpnAuthorizationRule
Properties: 
  [AccessGroupId](#cfn-ec2-clientvpnauthorizationrule-accessgroupid): String
  [AuthorizeAllGroups](#cfn-ec2-clientvpnauthorizationrule-authorizeallgroups): Boolean
  [ClientVpnEndpointId](#cfn-ec2-clientvpnauthorizationrule-clientvpnendpointid): String
  [Description](#cfn-ec2-clientvpnauthorizationrule-description): String
  [TargetNetworkCidr](#cfn-ec2-clientvpnauthorizationrule-targetnetworkcidr): String
```

## Properties<a name="aws-resource-ec2-clientvpnauthorizationrule-properties"></a>

`AccessGroupId`  <a name="cfn-ec2-clientvpnauthorizationrule-accessgroupid"></a>
The ID of the group to grant access to, for example, the Active Directory group or identity provider \(IdP\) group\. Required if `AuthorizeAllGroups` is `false` or not specified\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`AuthorizeAllGroups`  <a name="cfn-ec2-clientvpnauthorizationrule-authorizeallgroups"></a>
Indicates whether to grant access to all clients\. Specify `true` to grant all clients who successfully establish a VPN connection access to the network\. Must be set to `true` if `AccessGroupId` is not specified\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ClientVpnEndpointId`  <a name="cfn-ec2-clientvpnauthorizationrule-clientvpnendpointid"></a>
The ID of the Client VPN endpoint\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-ec2-clientvpnauthorizationrule-description"></a>
A brief description of the authorization rule\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TargetNetworkCidr`  <a name="cfn-ec2-clientvpnauthorizationrule-targetnetworkcidr"></a>
The IPv4 address range, in CIDR notation, of the network for which access is being authorized\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Examples<a name="aws-resource-ec2-clientvpnauthorizationrule--examples"></a>

### Adding an authorization rule to a Client VPN endpoint<a name="aws-resource-ec2-clientvpnauthorizationrule--examples--Adding_an_authorization_rule_to_a_Client_VPN_endpoint"></a>

The following example adds an authorization rule that grants all users access to the internet\.

#### YAML<a name="aws-resource-ec2-clientvpnauthorizationrule--examples--Adding_an_authorization_rule_to_a_Client_VPN_endpoint--yaml"></a>

```
myAuthRule:
  Type: "AWS::EC2::ClientVpnAuthorizationRule"
  Properties:
    ClientVpnEndpointId: 
      Ref: myClientVpnEndpoint
    AuthorizeAllGroups: true
    TargetNetworkCidr: "0.0.0.0/0"
    Description: "myAuthRule"
```

#### JSON<a name="aws-resource-ec2-clientvpnauthorizationrule--examples--Adding_an_authorization_rule_to_a_Client_VPN_endpoint--json"></a>

```
"myAuthRule": {
    "Type": "AWS::EC2::ClientVpnAuthorizationRule",
    "Properties": {
        "ClientVpnEndpointId": {
            "Ref": "myClientVpnEndpoint"
        },
        "AuthorizeAllGroups": true,
        "TargetNetworkCidr": "0.0.0.0/0",
        "Description": "myAuthRule"
    }
}
```

## See also<a name="aws-resource-ec2-clientvpnauthorizationrule--seealso"></a>
+ [Getting Started with Client VPN](https://docs.aws.amazon.com/vpn/latest/clientvpn-admin/cvpn-getting-started.html) in the *AWS Client VPN Administrator Guide*
+ [Authorization Rules](https://docs.aws.amazon.com/vpn/latest/clientvpn-admin/cvpn-working-rules.html) in the *AWS Client VPN Administrator Guide*

