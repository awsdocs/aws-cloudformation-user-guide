# AWS::Shield::DRTAccess<a name="aws-resource-shield-drtaccess"></a>

Provides permissions for the AWS Shield Advanced Shield response team \(SRT\) to access your account and your resource protections, to help you mitigate potential distributed denial of service \(DDoS\) attacks\.

**Note**  
To configure this resource through AWS CloudFormation, you must be subscribed to AWS Shield Advanced\. You can subscribe through the [Shield Advanced console](https://console.aws.amazon.com/wafv2/shieldv2#/) and through the APIs\. For more information, see [Subscribe to AWS Shield Advanced](https://docs.aws.amazon.com/waf/latest/developerguide/enable-ddos-prem.html)\. 

## Syntax<a name="aws-resource-shield-drtaccess-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-shield-drtaccess-syntax.json"></a>

```
{
  "Type" : "AWS::Shield::DRTAccess",
  "Properties" : {
      "[LogBucketList](#cfn-shield-drtaccess-logbucketlist)" : [ String, ... ],
      "[RoleArn](#cfn-shield-drtaccess-rolearn)" : String
    }
}
```

### YAML<a name="aws-resource-shield-drtaccess-syntax.yaml"></a>

```
Type: AWS::Shield::DRTAccess
Properties: 
  [LogBucketList](#cfn-shield-drtaccess-logbucketlist): 
    - String
  [RoleArn](#cfn-shield-drtaccess-rolearn): String
```

## Properties<a name="aws-resource-shield-drtaccess-properties"></a>

`LogBucketList`  <a name="cfn-shield-drtaccess-logbucketlist"></a>
Authorizes the Shield Response Team \(SRT\) to access the specified Amazon S3 bucket containing log data such as Application Load Balancer access logs, CloudFront logs, or logs from third party sources\. You can associate up to 10 Amazon S3 buckets with your subscription\.  
Use this to share information with the SRT that's not available in AWS WAF logs\.   
To use the services of the SRT, you must be subscribed to the [Business Support plan](http://aws.amazon.com/premiumsupport/business-support/) or the [Enterprise Support plan](http://aws.amazon.com/premiumsupport/enterprise-support/)\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-shield-drtaccess-rolearn"></a>
Authorizes the Shield Response Team \(SRT\) using the specified role, to access your AWS account to assist with DDoS attack mitigation during potential attacks\. This enables the SRT to inspect your AWS WAF configuration and logs and to create or update AWS WAF rules and web ACLs\.  
You can associate only one `RoleArn` with your subscription\. If you submit this update for an account that already has an associated role, the new `RoleArn` will replace the existing `RoleArn`\.   
This change requires the following:   
+ You must be subscribed to the [Business Support plan](http://aws.amazon.com/premiumsupport/business-support/) or the [Enterprise Support plan](http://aws.amazon.com/premiumsupport/enterprise-support/)\. 
+ You must have the `iam:PassRole` permission\. For more information, see [Granting a user permissions to pass a role to an AWS service](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_use_passrole.html)\. 
+ The `AWSShieldDRTAccessPolicy` managed policy must be attached to the role that you specify in the request\. You can access this policy in the IAM console at [AWSShieldDRTAccessPolicy](https://console.aws.amazon.com/iam/home?#/policies/arn:aws:iam::aws:policy/service-role/AWSShieldDRTAccessPolicy)\. For information, see [Adding and removing IAM identity permissions](https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies_manage-attach-detach.html)\. 
+ The role must trust the service principal `drt.shield.amazonaws.com`\. For information, see [IAM JSON policy elements: Principal](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_elements_principal.html)\.
The SRT will have access only to your AWS WAF and Shield resources\. By submitting this request, you provide permissions to the SRT to inspect your AWS WAF and Shield configuration and logs, and to create and update AWS WAF rules and web ACLs on your behalf\. The SRT takes these actions only if explicitly authorized by you\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-shield-drtaccess-return-values"></a>

### Ref<a name="aws-resource-shield-drtaccess-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the ID of the account that submitted the template\.

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-shield-drtaccess-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-shield-drtaccess-return-values-fn--getatt-fn--getatt"></a>

`AccountId`  <a name="AccountId-fn::getatt"></a>
The ID of the account that submitted the template\.

## Examples<a name="aws-resource-shield-drtaccess--examples"></a>



### Configure access for the Shield response team<a name="aws-resource-shield-drtaccess--examples--Configure_access_for_the_Shield_response_team"></a>

The following shows an example configuration to provide access to the Shield response team \(SRT\)\. 

#### YAML<a name="aws-resource-shield-drtaccess--examples--Configure_access_for_the_Shield_response_team--yaml"></a>

```
Resources:
  DRTAccess:
    Type: AWS::Shield::DRTAccess
    Properties:
      RoleArn: !GetAtt DRTAccessRole.Arn
      
  # support resources
  DRTAccessRole:
    Type: AWS::IAM::Role
    Properties:
      ManagedPolicyArns:
        - 'arn:aws:iam::aws:policy/service-role/AWSShieldDRTAccessPolicy'
      AssumeRolePolicyDocument:
        Version: "2012-10-17"
        Statement:
          - Effect: Allow
            Principal:
              Service:
                - 'drt.shield.amazonaws.com'
            Action:
              - 'sts:AssumeRole'
```

#### JSON<a name="aws-resource-shield-drtaccess--examples--Configure_access_for_the_Shield_response_team--json"></a>

```
{
    "Resources": {
        "DRTAccess": {
            "Type": "AWS::Shield::DRTAccess",
            "Properties": {
                "RoleArn": {
                    "Fn::GetAtt": [
                        "DRTAccessRole",
                        "Arn"
                    ]
                }
            }
        },
        "DRTAccessRole": {
            "Type": "AWS::IAM::Role",
            "Properties": {
                "ManagedPolicyArns": [
                    "arn:aws:iam::aws:policy/service-role/AWSShieldDRTAccessPolicy"
                ],
                "AssumeRolePolicyDocument": {
                    "Version": "2012-10-17",
                    "Statement": [
                        {
                            "Effect": "Allow",
                            "Principal": {
                                "Service": [
                                    "drt.shield.amazonaws.com"
                                ]
                            },
                            "Action": [
                                "sts:AssumeRole"
                            ]
                        }
                    ]
                }
            }
        }
    }
}
```

### Configure access for the Shield response team with additional data access<a name="aws-resource-shield-drtaccess--examples--Configure_access_for_the_Shield_response_team_with_additional_data_access"></a>

The following shows an example configuration to provide access to the Shield response team \(SRT\), including granting access to additional data that's outside of the web ACL logs\. The SRT is automatically granted access to the web ACL logs based on the provided `RoleArn`\.

#### YAML<a name="aws-resource-shield-drtaccess--examples--Configure_access_for_the_Shield_response_team_with_additional_data_access--yaml"></a>

```
Resources:
  DRTAccess:
    Type: AWS::Shield::DRTAccess
    Properties:
      LogBucketList:
        - !Ref DRTLogBucket1
        - !Ref DRTLogBucket2
      RoleArn: !GetAtt DRTAccessRole.Arn
  
  # support resources
  DRTLogBucket1:
    Type: AWS::S3::Bucket
    Properties:
      AccessControl: BucketOwnerFullControl
  DRTLogBucket2:
    Type: AWS::S3::Bucket
    Properties:
      AccessControl: BucketOwnerFullControl
  DRTAccessRole:
    Type: AWS::IAM::Role
    Properties:
      ManagedPolicyArns:
        - 'arn:aws:iam::aws:policy/service-role/AWSShieldDRTAccessPolicy'
      AssumeRolePolicyDocument:
        Version: "2012-10-17"
        Statement:
          - Effect: Allow
            Principal:
              Service:
                - 'drt.shield.amazonaws.com'
            Action:
              - 'sts:AssumeRole'
```

#### JSON<a name="aws-resource-shield-drtaccess--examples--Configure_access_for_the_Shield_response_team_with_additional_data_access--json"></a>

```
{
    "Resources": {
        "DRTAccess": {
            "Type": "AWS::Shield::DRTAccess",
            "Properties": {
                "LogBucketList": [
                    {
                        "Ref": "DRTLogBucket1"
                    },
                    {
                        "Ref": "DRTLogBucket2"
                    }
                ],
                "RoleArn": {
                    "Fn::GetAtt": [
                        "DRTAccessRole",
                        "Arn"
                    ]
                }
            }
        },
        "DRTLogBucket1": {
            "Type": "AWS::S3::Bucket",
            "Properties": {
                "AccessControl": "BucketOwnerFullControl"
            }
        },
        "DRTLogBucket2": {
            "Type": "AWS::S3::Bucket",
            "Properties": {
                "AccessControl": "BucketOwnerFullControl"
            }
        },
        "DRTAccessRole": {
            "Type": "AWS::IAM::Role",
            "Properties": {
                "ManagedPolicyArns": [
                    "arn:aws:iam::aws:policy/service-role/AWSShieldDRTAccessPolicy"
                ],
                "AssumeRolePolicyDocument": {
                    "Version": "2012-10-17",
                    "Statement": [
                        {
                            "Effect": "Allow",
                            "Principal": {
                                "Service": [
                                    "drt.shield.amazonaws.com"
                                ]
                            },
                            "Action": [
                                "sts:AssumeRole"
                            ]
                        }
                    ]
                }
            }
        }
    }
}
```