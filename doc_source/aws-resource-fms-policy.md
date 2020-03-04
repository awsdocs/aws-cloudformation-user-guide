# AWS::FMS::Policy<a name="aws-resource-fms-policy"></a>

An AWS Firewall Manager policy\.

Firewall Manager provides the following types of policies: 
+ A Shield Advanced policy, which applies Shield Advanced protection to specified accounts and resources\.
+ An AWS WAF policy, which contains a rule group and defines which resources are to be protected by that rule group\.
+ A security group policy, which manages VPC security groups across your AWS organization\. 

Each policy is specific to one of the types\. If you want to enforce more than one policy type across accounts, create multiple policies\. You can create multiple policies for each type\.

These policies require some setup to use\. For more information, see the sections on prerequisites and getting started under [AWS Firewall Manager](https://docs.aws.amazon.com/waf/latest/developerguide/fms-prereq.html)\.

## Syntax<a name="aws-resource-fms-policy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-fms-policy-syntax.json"></a>

```
{
  "Type" : "AWS::FMS::Policy",
  "Properties" : {
      "[DeleteAllPolicyResources](#cfn-fms-policy-deleteallpolicyresources)" : Boolean,
      "[ExcludeMap](#cfn-fms-policy-excludemap)" : [IEMap](aws-properties-fms-policy-iemap.md),
      "[ExcludeResourceTags](#cfn-fms-policy-excluderesourcetags)" : Boolean,
      "[IncludeMap](#cfn-fms-policy-includemap)" : [IEMap](aws-properties-fms-policy-iemap.md),
      "[PolicyName](#cfn-fms-policy-policyname)" : String,
      "[RemediationEnabled](#cfn-fms-policy-remediationenabled)" : Boolean,
      "[ResourceTags](#cfn-fms-policy-resourcetags)" : [ [ResourceTag](aws-properties-fms-policy-resourcetag.md), ... ],
      "[ResourceType](#cfn-fms-policy-resourcetype)" : String,
      "[ResourceTypeList](#cfn-fms-policy-resourcetypelist)" : [ String, ... ],
      "[SecurityServicePolicyData](#cfn-fms-policy-securityservicepolicydata)" : Json,
      "[Tags](#cfn-fms-policy-tags)" : [ [PolicyTag](aws-properties-fms-policy-policytag.md), ... ]
    }
}
```

### YAML<a name="aws-resource-fms-policy-syntax.yaml"></a>

```
Type: AWS::FMS::Policy
Properties: 
  [DeleteAllPolicyResources](#cfn-fms-policy-deleteallpolicyresources): Boolean
  [ExcludeMap](#cfn-fms-policy-excludemap): 
    [IEMap](aws-properties-fms-policy-iemap.md)
  [ExcludeResourceTags](#cfn-fms-policy-excluderesourcetags): Boolean
  [IncludeMap](#cfn-fms-policy-includemap): 
    [IEMap](aws-properties-fms-policy-iemap.md)
  [PolicyName](#cfn-fms-policy-policyname): String
  [RemediationEnabled](#cfn-fms-policy-remediationenabled): Boolean
  [ResourceTags](#cfn-fms-policy-resourcetags): 
    - [ResourceTag](aws-properties-fms-policy-resourcetag.md)
  [ResourceType](#cfn-fms-policy-resourcetype): String
  [ResourceTypeList](#cfn-fms-policy-resourcetypelist): 
    - String
  [SecurityServicePolicyData](#cfn-fms-policy-securityservicepolicydata): Json
  [Tags](#cfn-fms-policy-tags): 
    - [PolicyTag](aws-properties-fms-policy-policytag.md)
```

## Properties<a name="aws-resource-fms-policy-properties"></a>

`DeleteAllPolicyResources`  <a name="cfn-fms-policy-deleteallpolicyresources"></a>
Used when deleting a policy\. If `true`, Firewall Manager performs cleanup according to the policy type\.  
For AWS WAF and Shield Advanced policies, Firewall Manager does the following:  
+ Deletes rule groups created by AWS Firewall Manager
+ Removes web ACLs from in\-scope resources 
+ Deletes web ACLs that contain no rules or rule groups 
For security group policies, Firewall Manager does the following for each security group in the policy:  
+ Disassociates the security group from in\-scope resources 
+ Deletes the security group if it was created through Firewall Manager and if it's no longer associated with any resources through another policy 
After the cleanup, in\-scope resources are no longer protected by web ACLs in this policy\. Protection of out\-of\-scope resources remains unchanged\. Scope is determined by tags that you create and accounts that you associate with the policy\. When creating the policy, if you specify that only resources in specific accounts or with specific tags are in scope of the policy, those accounts and resources are handled by the policy\. All others are out of scope\. If you don't specify tags or accounts, all resources are in scope\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExcludeMap`  <a name="cfn-fms-policy-excludemap"></a>
Specifies the AWS account IDs to exclude from the policy\. The `IncludeMap` values are evaluated first, with all the appropriate account IDs added to the policy\. Then the accounts listed in `ExcludeMap` are removed, resulting in the final list of accounts to add to the policy\.  
The key to the map is `ACCOUNT`\. For example, a valid `ExcludeMap` would be `{“ACCOUNT” : [“accountID1”, “accountID2”]}`\.  
*Required*: No  
*Type*: [IEMap](aws-properties-fms-policy-iemap.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExcludeResourceTags`  <a name="cfn-fms-policy-excluderesourcetags"></a>
Used only when tags are specified in the `ResourceTags` property\. If this property is `True`, resources with the specified tags are not in scope of the policy\. If it's `False`, only resources with the specified tags are in scope of the policy\.   
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludeMap`  <a name="cfn-fms-policy-includemap"></a>
Specifies the AWS account IDs to include in the policy\. If `IncludeMap` is not set, all accounts in the organization in AWS Organizations are included in the policy\. If `IncludeMap` is set, only values listed in `IncludeMap` are included in the policy\.  
The key to the map is `ACCOUNT`\. For example, a valid `IncludeMap` would be `{“ACCOUNT” : [“accountID1”, “accountID2”]}`\.  
*Required*: No  
*Type*: [IEMap](aws-properties-fms-policy-iemap.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PolicyName`  <a name="cfn-fms-policy-policyname"></a>
The friendly name of the AWS Firewall Manager policy\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `^([\p{L}\p{Z}\p{N}_.:/=+\-@]*)$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RemediationEnabled`  <a name="cfn-fms-policy-remediationenabled"></a>
Indicates if the policy should be automatically applied to new resources\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceTags`  <a name="cfn-fms-policy-resourcetags"></a>
An array of `ResourceTag` objects, used to explicitly include resources in the policy scope or explicitly exclude them\. If this isn't set, then tags aren't used to modify policy scope\. See also `ExcludeResourceTags`\.  
*Required*: No  
*Type*: List of [ResourceTag](aws-properties-fms-policy-resourcetag.md)  
*Maximum*: `8`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceType`  <a name="cfn-fms-policy-resourcetype"></a>
The type of resource protected by or in scope of the policy\. This is in the format shown in the [AWS Resource Types Reference](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-template-resource-type-ref.html)\. For AWS WAF and Shield Advanced, examples include `AWS::ElasticLoadBalancingV2::LoadBalancer` and `AWS::CloudFront::Distribution`\. For a security group common policy, valid values are `AWS::EC2::NetworkInterface` and `AWS::EC2::Instance`\. For a security group content audit policy, valid values are `AWS::EC2::SecurityGroup`, `AWS::EC2::NetworkInterface`, and `AWS::EC2::Instance`\. For a security group usage audit policy, the value is `AWS::EC2::SecurityGroup`\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `^([\p{L}\p{Z}\p{N}_.:/=+\-@]*)$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceTypeList`  <a name="cfn-fms-policy-resourcetypelist"></a>
An array of `ResourceType`\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityServicePolicyData`  <a name="cfn-fms-policy-securityservicepolicydata"></a>
Details about the security service that is being used to protect the resources\.  
*Required*: Yes  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-fms-policy-tags"></a>
A collection of key:value pairs associated with an AWS resource\. The key:value pair can be anything you define\. Typically, the tag key represents a category \(such as "environment"\) and the tag value represents a specific value within that category \(such as "test," "development," or "production"\)\. You can add up to 50 tags to each AWS resource\.   
*Required*: No  
*Type*: List of [PolicyTag](aws-properties-fms-policy-policytag.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-fms-policy-return-values"></a>

### Ref<a name="aws-resource-fms-policy-return-values-ref"></a>

The `Ref` for this resource returns the `PolicyId`\. 

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource physical ID, such as 1234a1a\-a1b1\-12a1\-abcd\-a123b123456\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-fms-policy-return-values-fn--getatt"></a>

#### <a name="aws-resource-fms-policy-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the policy\.

`Id`  <a name="Id-fn::getatt"></a>
The ID of the policy\.

## Examples<a name="aws-resource-fms-policy--examples"></a>

### Create a Firewall Manager Shield Advanced policy<a name="aws-resource-fms-policy--examples--Create_a_Firewall_Manager_Shield_Advanced_policy"></a>

The following shows an example Firewall Manager Shield Advanced policy\. This example uses account and resource tag specifications to limit the scope of the policy\. 

#### YAML<a name="aws-resource-fms-policy--examples--Create_a_Firewall_Manager_Shield_Advanced_policy--yaml"></a>

```
Policy:
    Type: AWS::FMS::Policy
    Properties:
      ExcludeResourceTags: true
      ResourceTags:
        - Key: resourceTag1
          Value: value
        - Key: resourceTag2
          Value: value
      IncludeMap:
        ACCOUNT:
          - !Ref AWS::AccountId
      PolicyName: TaggedPolicy
      RemediationEnabled: false
      ResourceType: ResourceTypeList
      ResourceTypeList:
        - AWS::ElasticLoadBalancingV2::LoadBalancer
        - AWS::EC2::EIP
      SecurityServicePolicyData:
        Type: SHIELD_ADVANCED
      DeleteAllPolicyResources: false
      Tags:
        - Key: tag1
          Value: value
        - Key: tag2
          Value: value
```

#### JSON<a name="aws-resource-fms-policy--examples--Create_a_Firewall_Manager_Shield_Advanced_policy--json"></a>

```
"Policy": {
    "Type": "AWS::FMS::Policy",
    "Properties": {
        "ExcludeResourceTags": true,
        "ResourceTags": [
            {
                "Key": "resourceTag1",
                "Value": "value"
            },
            {
                "Key": "resourceTag2",
                "Value": "value"
            }
          ],
          "IncludeMap": {
              "ACCOUNT": [
                {
                  "Ref": "AWS::AccountId"
                }
              ]
          },
          "PolicyName": "TaggedPolicy",
          "RemediationEnabled": false,
          "ResourceType": "ResourceTypeList",
          "ResourceTypeList": [
              "AWS::ElasticLoadBalancingV2::LoadBalancer",
              "AWS::EC2::EIP"
          ],
          "SecurityServicePolicyData": {
              "Type": "SHIELD_ADVANCED"
          },
          "Tags": [
              {
                "Key": "tag1",
                "Value": "value"
              },
              {
              "Key": "tag2",
              "Value": "value"
            }
        ]
    }
}
```

### Create a Firewall Manager common security group policy<a name="aws-resource-fms-policy--examples--Create_a_Firewall_Manager_common_security_group_policy_"></a>

The following shows an example Firewall Manager common security group policy\. 

#### YAML<a name="aws-resource-fms-policy--examples--Create_a_Firewall_Manager_common_security_group_policy_--yaml"></a>

```
Policy:
    Type: AWS::FMS::Policy
    Properties:
      ExcludeResourceTags: false
      PolicyName: SecurityGroupsCommonsPolicy
      RemediationEnabled: false
      ResourceType: AWS::EC2::Instance
      SecurityServicePolicyData:
        Type: SECURITY_GROUPS_COMMON
        ManagedServiceData: !Sub '{"type":"SECURITY_GROUPS_COMMON",
                                  "revertManualSecurityGroupChanges":true,
                                  "securityGroups":[{"id":"${SecurityGroup.GroupId}"}]}'
```

#### JSON<a name="aws-resource-fms-policy--examples--Create_a_Firewall_Manager_common_security_group_policy_--json"></a>

```
"Policy": {
    "Type": "AWS::FMS::Policy",
    "Properties": {
        "ExcludeResourceTags": false,
        "PolicyName": "SecurityGroupsCommonsPolicy",
        "RemediationEnabled": false,
        "ResourceType": "AWS::EC2::Instance",
        "SecurityServicePolicyData": {
            "Type": "SECURITY_GROUPS_COMMON",
            "ManagedServiceData": {
                "Fn::Sub": "{\"type\":\"SECURITY_GROUPS_COMMON\",\"revertManualSecurityGroupChanges\":true,\"securityGroups\":[{\"id\":\"${SecurityGroup.GroupId}\"}]}"
            }
        }
    }
}
```