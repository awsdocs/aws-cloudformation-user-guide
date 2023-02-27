# AWS::Organizations::ResourcePolicy<a name="aws-resource-organizations-resourcepolicy"></a>

Creates or updates a resource\-based delegation policy that can be used to delegate policy management for AWS Organizations to specified member accounts to perform policy actions that are by default available only to the management account\.

For more information about delegated policy management, see [Delegated administrator for AWS Organizations](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_delegate_policies.html) in the *AWS Organizations User Guide*\.

You can only call this operation from the organization's management account\.

## Syntax<a name="aws-resource-organizations-resourcepolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-organizations-resourcepolicy-syntax.json"></a>

```
{
  "Type" : "AWS::Organizations::ResourcePolicy",
  "Properties" : {
      "[Content](#cfn-organizations-resourcepolicy-content)" : Json,
      "[Tags](#cfn-organizations-resourcepolicy-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-organizations-resourcepolicy-syntax.yaml"></a>

```
Type: AWS::Organizations::ResourcePolicy
Properties: 
  [Content](#cfn-organizations-resourcepolicy-content): Json
  [Tags](#cfn-organizations-resourcepolicy-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-organizations-resourcepolicy-properties"></a>

`Content`  <a name="cfn-organizations-resourcepolicy-content"></a>
The policy text of the organization resource policy\. You can specify the resource policy content as a JSON object or a JSON string\.  
When you specify the resource policy content as a JSON string, you can't perform drift detection on the CloudFormation stack\. For this reason, we recommend specifying the resource policy content as a JSON object instead\.
*Required*: Yes  
*Type*: Json  
*Minimum*: `1`  
*Maximum*: `40000`  
*Pattern*: `[\s\S]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-organizations-resourcepolicy-tags"></a>
A list of tags that you want to attach to the newly created resource policy\. For each tag in the list, you must specify both a tag key and a value\. You can set the value to an empty string, but you can't set it to `null`\. For more information about tagging, see [Tagging AWS Organizations resources](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_tagging.html) in the *AWS Organizations User Guide*\.  
If any one of the tags is not valid or if you exceed the allowed number of tags for the resource policy, then the entire request fails and the resource policy is not created\.
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-organizations-resourcepolicy-return-values"></a>

### Ref<a name="aws-resource-organizations-resourcepolicy-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `Id`\. For example: `rp-examplepolicyid111`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-organizations-resourcepolicy-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-organizations-resourcepolicy-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Returns the Amazon Resource Name \(ARN\) of the policy\. For example: `arn:aws:organizations::111111111111:resourcepolicy/o-exampleorgid/rp-examplepolicyid111`\.

`Id`  <a name="Id-fn::getatt"></a>
Returns the unique identifier \(ID\) of the resource policy\. For example: `rp-examplepolicyid111`\.

## Examples<a name="aws-resource-organizations-resourcepolicy--examples"></a>



### Organization Resource Policy Content Specified as a JSON Object<a name="aws-resource-organizations-resourcepolicy--examples--Organization_Resource_Policy_Content_Specified_as_a_JSON_Object"></a>

This example illustrates how to specify the organization resource policy content as a JSON object in `AWS::Organizations::ResourcePolicy`\. The organization resource policy is specified inline as a JSON object in the `Content` property of `AWS::Organizations::ResourcePolicy`\.

#### JSON<a name="aws-resource-organizations-resourcepolicy--examples--Organization_Resource_Policy_Content_Specified_as_a_JSON_Object--json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Description": "AWS CloudFormation Organizations Template Example",
  "Resources": {
    "ResourcePolicyTestTemplate": {
      "DeletionPolicy": "Retain",
      "Type": "AWS::Organizations::ResourcePolicy",
      "Properties": {
        "Content": {
          "Version": "2012-10-17",
          "Statement": [
            {
              "Sid": "AllowDescribeOrganization",
              "Effect": "Allow",
              "Principal": {
                "AWS": "arn:aws:iam::111122223333:root"
              },
              "Action": [
                "organizations:DescribeOrganization"
              ],
              "Resource": "*"
            }
          ]
        }
      }
    }
  }
}
```

#### YAML<a name="aws-resource-organizations-resourcepolicy--examples--Organization_Resource_Policy_Content_Specified_as_a_JSON_Object--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: AWS CloudFormation Organizations Template Example
Resources:
  ResourcePolicyTestTemplate:
    DeletionPolicy: Retain
    Type: 'AWS::Organizations::ResourcePolicy'
    Properties:
      Content:
        Version: 2012-10-17
        Statement:
          - Sid: AllowDescribeOrganization
            Effect: Allow
            Principal:
              AWS: 'arn:aws:iam::111122223333:root'
            Action:
              - 'organizations:DescribeOrganization'
            Resource: '*'
```

### Organization Resource Policy Content Specified as a JSON String<a name="aws-resource-organizations-resourcepolicy--examples--Organization_Resource_Policy_Content_Specified_as_a_JSON_String"></a>

This example illustrates how to specify the organization resource policy content as a JSON string in `AWS::Organizations::ResourcePolicy`\. The organization resource policy is specified inline as a JSON string in the `Content` property of `AWS::Organizations::ResourcePolicy`\.

#### JSON<a name="aws-resource-organizations-resourcepolicy--examples--Organization_Resource_Policy_Content_Specified_as_a_JSON_String--json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Description": "AWS CloudFormation Organizations Template Example",
  "Resources": {
    "ResourcePolicyExample": {
      "DeletionPolicy": "Retain",
      "Type": "AWS::Organizations::ResourcePolicy",
      "Properties": {
        "Content": "{\"Version\":\"2012-10-17\",\"Statement\":[{\"Sid\":\"AllowDescribeOrganization\",\"Effect\":\"Allow\",\"Principal\":{\"AWS\":\"arn:aws:iam::111122223333:root\"},\"Action\":[\"organizations:DescribeOrganization\"],\"Resource\":\"*\"}]}"
      }
    }
  }
}
```

#### YAML<a name="aws-resource-organizations-resourcepolicy--examples--Organization_Resource_Policy_Content_Specified_as_a_JSON_String--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: AWS CloudFormation Organizations Template Example
Resources:
  ResourcePolicyExample:
    DeletionPolicy: Retain
    Type: AWS::Organizations::ResourcePolicy
    Properties:
      Content: >-
        {"Version":"2012-10-17","Statement":[{"Sid":"AllowDescribeOrganization","Effect":"Allow","Principal":{"AWS":"arn:aws:iam::111122223333:root"},"Action":["organizations:DescribeOrganization"],"Resource":"*"}]}
```

#### YAML<a name="aws-resource-organizations-resourcepolicy--examples--Organization_Resource_Policy_Content_Specified_as_a_JSON_String--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: AWS CloudFormation Organizations Template Example
Resources:
  ResourcePolicyExample:
    DeletionPolicy: Retain
    Type: AWS::Organizations::ResourcePolicy
    Properties:
      Content: >-
        {
          "Version": "2012-10-17",
          "Statement": [
            {
              "Sid": "AllowDescribeOrganization",
              "Effect": "Allow",
              "Principal": {
                "AWS": "arn:aws:iam::111122223333:root"
              },
              "Action": [
                "organizations:DescribeOrganization"
              ],
              "Resource": "*"
            }
          ]
        }
```