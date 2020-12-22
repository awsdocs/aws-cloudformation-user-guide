# AWS::NetworkFirewall::RuleGroup<a name="aws-resource-networkfirewall-rulegroup"></a>

Use the [AWS::NetworkFirewall::RuleGroup](#aws-resource-networkfirewall-rulegroup) to define a reusable collection of stateless or stateful network traffic filtering rules\. You use rule groups in an [AWS::NetworkFirewall::FirewallPolicy](aws-resource-networkfirewall-firewallpolicy.md) to specify the filtering behavior of an [AWS::NetworkFirewall::Firewall](aws-resource-networkfirewall-firewall.md)\. 

## Syntax<a name="aws-resource-networkfirewall-rulegroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-networkfirewall-rulegroup-syntax.json"></a>

```
{
  "Type" : "AWS::NetworkFirewall::RuleGroup",
  "Properties" : {
      "[Capacity](#cfn-networkfirewall-rulegroup-capacity)" : Integer,
      "[Description](#cfn-networkfirewall-rulegroup-description)" : String,
      "[RuleGroup](#cfn-networkfirewall-rulegroup-rulegroup)" : RuleGroup,
      "[RuleGroupName](#cfn-networkfirewall-rulegroup-rulegroupname)" : String,
      "[Tags](#cfn-networkfirewall-rulegroup-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Type](#cfn-networkfirewall-rulegroup-type)" : String
    }
}
```

### YAML<a name="aws-resource-networkfirewall-rulegroup-syntax.yaml"></a>

```
Type: AWS::NetworkFirewall::RuleGroup
Properties: 
  [Capacity](#cfn-networkfirewall-rulegroup-capacity): Integer
  [Description](#cfn-networkfirewall-rulegroup-description): String
  [RuleGroup](#cfn-networkfirewall-rulegroup-rulegroup): 
    RuleGroup
  [RuleGroupName](#cfn-networkfirewall-rulegroup-rulegroupname): String
  [Tags](#cfn-networkfirewall-rulegroup-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Type](#cfn-networkfirewall-rulegroup-type): String
```

## Properties<a name="aws-resource-networkfirewall-rulegroup-properties"></a>

`Capacity`  <a name="cfn-networkfirewall-rulegroup-capacity"></a>
The maximum operating resources that this rule group can use\. You can't change a rule group's capacity setting after you create the rule group\. When you update a rule group, you are limited to this capacity\. When you reference a rule group from a firewall policy, Network Firewall reserves this capacity for the rule group\.   
*Required*: Yes  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-networkfirewall-rulegroup-description"></a>
A description of the rule group\.   
*Required*: No  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `^.*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RuleGroup`  <a name="cfn-networkfirewall-rulegroup-rulegroup"></a>
An object that defines the rule group rules\.   
You must provide either this rule group setting or a `Rules` setting, but not both\. 
*Required*: No  
*Type*: [RuleGroup](aws-properties-networkfirewall-rulegroup-rulegroup.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RuleGroupName`  <a name="cfn-networkfirewall-rulegroup-rulegroupname"></a>
The descriptive name of the rule group\. You can't change the name of a rule group after you create it\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `^[a-zA-Z0-9-]+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-networkfirewall-rulegroup-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-networkfirewall-rulegroup-type"></a>
Indicates whether the rule group is stateless or stateful\. If the rule group is stateless, it contains stateless rules\. If it is stateful, it contains stateful rules\.   
*Required*: Yes  
*Type*: String  
*Allowed values*: `STATEFUL | STATELESS`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-networkfirewall-rulegroup-return-values"></a>

### Ref<a name="aws-resource-networkfirewall-rulegroup-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Amazon Resource Name \(ARN\) of the rule group\. For example: 

 `{ "Ref": "arn:aws:network-firewall:us-east-1:012345678901:stateful-rulegroup/myStatefulRuleGroupName" }` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-networkfirewall-rulegroup-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-networkfirewall-rulegroup-return-values-fn--getatt-fn--getatt"></a>

`RuleGroupArn`  <a name="RuleGroupArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the [AWS::NetworkFirewall::RuleGroup](#aws-resource-networkfirewall-rulegroup)\. 

`RuleGroupId`  <a name="RuleGroupId-fn::getatt"></a>
The unique ID of the [AWS::NetworkFirewall::RuleGroup](#aws-resource-networkfirewall-rulegroup) resource\. 

## Examples<a name="aws-resource-networkfirewall-rulegroup--examples"></a>



### Create a stateful rule group<a name="aws-resource-networkfirewall-rulegroup--examples--Create_a_stateful_rule_group"></a>

The following shows example stateful rule group specifications\. 

#### JSON<a name="aws-resource-networkfirewall-rulegroup--examples--Create_a_stateful_rule_group--json"></a>

```
"SampleStatefulRulegroup": {
    "Type": "AWS::NetworkFirewall::RuleGroup",
    "Properties": {
        "RuleGroupName": "SampleStatefulRulegroupName",
        "Type": "STATEFUL",
        "RuleGroup": {
            "RulesSource": {
                "RulesString": "pass tcp 10.20.20.0/24 45400:45500 <> 10.10.10.0/24 5203 (msg:\"test\";sid:1;rev:1;)"
            }
        },
        "Capacity": 100,
        "Description": "Rulegroup description goes here",
        "Tags": [
            {
                "Key": "Foo",
                "Value": "Bar"
            }
        ]
    }
}
```

#### YAML<a name="aws-resource-networkfirewall-rulegroup--examples--Create_a_stateful_rule_group--yaml"></a>

```
SampleStatefulRulegroup:
  Type: 'AWS::NetworkFirewall::RuleGroup'
  Properties:
    RuleGroupName: SampleStatefulRulegroupName
    Type: STATEFUL
    RuleGroup:
      RulesSource:
        RulesString: >-
          pass tcp 10.20.20.0/24 45400:45500 <> 10.10.10.0/24 5203
          (msg:"test";sid:1;rev:1;)
    Capacity: 100
    Description: Rulegroup description goes here
    Tags:
      - Key: Foo
        Value: Bar
```

### Create a stateless rule group<a name="aws-resource-networkfirewall-rulegroup--examples--Create_a_stateless_rule_group"></a>

The following shows example stateless rule group specifications\. 

#### JSON<a name="aws-resource-networkfirewall-rulegroup--examples--Create_a_stateless_rule_group--json"></a>

```
"SampleStatelessRulegroup": {
    "Type": "AWS::NetworkFirewall::RuleGroup",
    "Properties": {
        "RuleGroupName": "SampleStatelessRulegroupName",
        "Type": "STATELESS",
        "RuleGroup": {
            "RulesSource": {
                "StatelessRulesAndCustomActions": {
                    "StatelessRules": [
                        {
                            "RuleDefinition": {
                                "MatchAttributes": {
                                    "Sources": [
                                        {
                                            "AddressDefinition": "0.0.0.0/0"
                                        }
                                    ],
                                    "Destinations": [
                                        {
                                            "AddressDefinition": "10.0.0.0/8"
                                        }
                                    ],
                                    "SourcePorts": [
                                        {
                                            "FromPort": 15000
                                        },
                                        {
                                            "ToPort": 30000
                                        }
                                    ],
                                    "DestinationPorts": [
                                        {
                                            "FromPort": 443
                                        },
                                        {
                                            "ToPort": 443
                                        }
                                    ],
                                    "Protocols": [
                                        6
                                    ]
                                },
                                "Actions": [
                                    "aws:pass"
                                ]
                            },
                            "Priority": 1
                        }
                    ]
                }
            }
        },
        "Capacity": 100,
        "Description": "Rulegroup description goes here",
        "Tags": [
            {
                "Key": "Foo",
                "Value": "Bar"
            }
        ]
    }
}
```

#### YAML<a name="aws-resource-networkfirewall-rulegroup--examples--Create_a_stateless_rule_group--yaml"></a>

```
SampleStatelessRulegroup:
    Type: 'AWS::NetworkFirewall::RuleGroup'
    Properties:
      RuleGroupName: SampleStatelessRulegroupName
      Type: STATELESS
      RuleGroup:
        RulesSource:
          StatelessRulesAndCustomActions:
            StatelessRules:
              - RuleDefinition:
                  MatchAttributes:
                    Sources:
                      - AddressDefinition: 0.0.0.0/0
                    Destinations:
                      - AddressDefinition: 10.0.0.0/8
                    SourcePorts:
                      - FromPort: 15000
                      - ToPort: 30000
                    DestinationPorts:
                      - FromPort: 443
                      - ToPort: 443
                    Protocols:
                      - 6
                  Actions:
                    - 'aws:pass'
                Priority: 1
      Capacity: 100
      Description: Rulegroup description goes here
      Tags:
        - Key: Foo
          Value: Bar
```