# AWS::Route53Resolver::FirewallRuleGroup<a name="aws-resource-route53resolver-firewallrulegroup"></a>

High\-level information for a firewall rule group\. A firewall rule group is a collection of rules that DNS Firewall uses to filter DNS network traffic for a VPC\. To retrieve the rules for the rule group, call [ListFirewallRules](https://docs.aws.amazon.com/Route53/latest/APIReference/API_route53resolver_ListFirewallRules.html)\.

## Syntax<a name="aws-resource-route53resolver-firewallrulegroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-route53resolver-firewallrulegroup-syntax.json"></a>

```
{
  "Type" : "AWS::Route53Resolver::FirewallRuleGroup",
  "Properties" : {
      "[FirewallRules](#cfn-route53resolver-firewallrulegroup-firewallrules)" : [ FirewallRule, ... ],
      "[Name](#cfn-route53resolver-firewallrulegroup-name)" : String,
      "[Tags](#cfn-route53resolver-firewallrulegroup-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-route53resolver-firewallrulegroup-syntax.yaml"></a>

```
Type: AWS::Route53Resolver::FirewallRuleGroup
Properties: 
  [FirewallRules](#cfn-route53resolver-firewallrulegroup-firewallrules): 
    - FirewallRule
  [Name](#cfn-route53resolver-firewallrulegroup-name): String
  [Tags](#cfn-route53resolver-firewallrulegroup-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-route53resolver-firewallrulegroup-properties"></a>

`FirewallRules`  <a name="cfn-route53resolver-firewallrulegroup-firewallrules"></a>
A list of the rules that you have defined\.   
*Required*: No  
*Type*: List of [FirewallRule](aws-properties-route53resolver-firewallrulegroup-firewallrule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-route53resolver-firewallrulegroup-name"></a>
The name of the rule group\.  
*Required*: No  
*Type*: String  
*Maximum*: `64`  
*Pattern*: `(?!^[0-9]+$)([a-zA-Z0-9\-_' ']+)`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-route53resolver-firewallrulegroup-tags"></a>
A list of the tag keys and values that you want to associate with the rule group\.   
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-route53resolver-firewallrulegroup-return-values"></a>

### Ref<a name="aws-resource-route53resolver-firewallrulegroup-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returnsthe `FirewallRuleGroupId`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-route53resolver-firewallrulegroup-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-route53resolver-firewallrulegroup-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN \(Amazon Resource Name\) of the rule group\.

`CreationTime`  <a name="CreationTime-fn::getatt"></a>
The date and time that the rule group was created, in Unix time format and Coordinated Universal Time \(UTC\)\.

`CreatorRequestId`  <a name="CreatorRequestId-fn::getatt"></a>
A unique string defined by you to identify the request\. This allows you to retry failed requests without the risk of running the operation twice\. This can be any unique string, for example, a timestamp\.

`Id`  <a name="Id-fn::getatt"></a>
The ID of the rule group\.

`ModificationTime`  <a name="ModificationTime-fn::getatt"></a>
The date and time that the rule group was last modified, in Unix time format and Coordinated Universal Time \(UTC\)\.

`OwnerId`  <a name="OwnerId-fn::getatt"></a>
The AWS account ID for the account that created the rule group\. When a rule group is shared with your account, this is the account that has shared the rule group with you\.

`RuleCount`  <a name="RuleCount-fn::getatt"></a>
The number of rules in the rule group\.

`ShareStatus`  <a name="ShareStatus-fn::getatt"></a>
Whether the rule group is shared with other AWS accounts, or was shared with the current account by another AWS account\. Sharing is configured through AWS Resource Access Manager \(AWS RAM\)\.

`Status`  <a name="Status-fn::getatt"></a>
The status of the domain list\.

`StatusMessage`  <a name="StatusMessage-fn::getatt"></a>
Additional information about the status of the rule group, if available\.

## Examples<a name="aws-resource-route53resolver-firewallrulegroup--examples"></a>



### Create Firewall rule group<a name="aws-resource-route53resolver-firewallrulegroup--examples--Create_Firewall_rule_group"></a>

The following example creates a DNS Firewall rule group with associated rules for `ALLOW`, `ALERT`, and `BLOCK`\.

#### JSON<a name="aws-resource-route53resolver-firewallrulegroup--examples--Create_Firewall_rule_group--json"></a>

```
{"Type": "AWS::Route53Resolver::FirewallRuleGroup",
"Properties": {
     "FirewallRules": [
         {
            "Action": "ALERT",
            "FirewallDomainListId": "rslvr-fdl-sampleID1",
            "Priority": 1
         },
         {
            "Action": "BLOCK",
            "BlockResponse": "NODATA",
            "FirewallDomainListId": "rslvr-fdl-sampleID2",
            "Priority": 2
          },
          {
            "Action": "BLOCK",
            "BlockResponse": "NXDOMAIN",
            "FirewallDomainListId": "rslvr-fdl-sampleID3",
            "Priority": 3
          },
          {
            "Action": "BLOCK",
            "BlockResponse": "OVERRIDE",
            "BlockOverrideDnsType": "CNAME",
            "BlockOverrideDomain": "www.example.com",
            "BlockOverrideTtl": 300,
            "FirewallDomainListId": "rslvr-fdl-sampleID4",
            "Priority": 4
          },
          {
            "Action": "ALLOW",
            "FirewallDomainListId": "rslvr-fdl-sampleID5",
            "Priority": 5
          }
        ],
        "Name": "SampleFirewallRuleGroup",
        "Tags": [
          {
            "Key": "LineOfBusiness",
            "Value": "Engineering"
          }
      ]
   }
}
```

#### YAML<a name="aws-resource-route53resolver-firewallrulegroup--examples--Create_Firewall_rule_group--yaml"></a>

```
Type: AWS::Route53Resolver::FirewallRuleGroup
Properties:
   FirewallRules:
      -
        Action: ALERT
        FirewallDomainListId: rslvr-fdl-sampleID1
        Priority: 1
      -
        Action: BLOCK
        BlockResponse: NODATA
        FirewallDomainListId: rslvr-fdl-sampleID2
        Priority: 2
      -
        Action: BLOCK
        BlockResponse: NXDOMAIN
        FirewallDomainListId: rslvr-fdl-sampleID3
        Priority: 3
      -
        Action: BLOCK
        BlockResponse: OVERRIDE
        BlockOverrideDnsType: CNAME
        BlockOverrideDomain: "www.example.com"
        BlockOverrideTtl: 300
        FirewallDomainListId: rslvr-fdl-sampleID4
        Priority: 4
      -
        Action: ALLOW
        FirewallDomainListId: rslvr-fdl-sampleID5
        Priority: 5
        Name: SampleFirewallRuleGroup
    Tags:
      -
         Key: LineOfBusiness
         Value: Engineering
```