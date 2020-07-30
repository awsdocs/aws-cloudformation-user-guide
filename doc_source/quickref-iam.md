# AWS Identity and Access Management template snippets<a name="quickref-iam"></a>

This section contains AWS Identity and Access Management template snippets\.

**Topics**
+ [Declaring an IAM user resource](#scenario-iam-user)
+ [Declaring an IAM access key resource](#scenario-iam-accesskey)
+ [Declaring an IAM group resource](#scenario-iam-group)
+ [Adding users to a group](#scenario-iam-addusertogroup)
+ [Declaring an IAM policy](#scenario-iam-policy)
+ [Declaring an Amazon S3 bucket policy](#scenario-bucket-policy)
+ [Declaring an Amazon SNS topic policy](#scenario-sns-policy)
+ [Declaring an Amazon SQS policy](#scenario-sqs-policy)
+ [IAM role template examples](#scenarios-iamroles)

**Important**  
When creating or updating a stack using a template containing IAM resources, you must acknowledge the use of IAM capabilities\. For more information about using IAM resources in templates, see [Controlling access with AWS Identity and Access Management](using-iam-template.md)\.

## Declaring an IAM user resource<a name="scenario-iam-user"></a>

This snippet shows how to declare an `[AWS::IAM::User](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-iam-user.html)` resource to create an IAM user\. The user is declared with the path \(`"/"`\) and a login profile with the password \(`myP@ssW0rd`\)\.

The policy document named `giveaccesstoqueueonly` gives the user permission to perform all Amazon SQS actions on the Amazon SQS queue resource `myqueue`, and denies access to all other Amazon SQS queue resources\. The `Fn::GetAtt` function gets the Arn attribute of the `[AWS::SQS::Queue](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-sqs-queues.html)` resource `myqueue`\. 

The policy document named `giveaccesstotopiconly` is added to the user to give the user permission to perform all Amazon SNS actions on the Amazon SNS topic resource `mytopic` and to deny access to all other Amazon SNS resources\. The [`Ref`](intrinsic-function-reference-ref.md) function gets the ARN of the `[AWS::SNS::Topic](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-sns-topic.html)` resource `mytopic`\.

### JSON<a name="quickref-iam-example-1.json"></a>

```
"myuser" : {
   "Type" : "AWS::IAM::User",
   "Properties" : {
      "Path" : "/",
      "LoginProfile" : {
         "Password" : "myP@ssW0rd"
      },
      "Policies" : [ {
         "PolicyName" : "giveaccesstoqueueonly",
         "PolicyDocument" : {
            "Version": "2012-10-17",
            "Statement" : [ {
               "Effect" : "Allow",
               "Action" : [ "sqs:*" ],
               "Resource" : [ {
                  "Fn::GetAtt" : [ "myqueue", "Arn" ]
               } ]
            }, {
               "Effect" : "Deny",
               "Action" : [ "sqs:*" ],
               "NotResource" : [ {
                  "Fn::GetAtt" : [ "myqueue", "Arn" ]
               } ]
            }
         ] }
      }, {
         "PolicyName" : "giveaccesstotopiconly",
         "PolicyDocument" : {
            "Version": "2012-10-17",
            "Statement" : [ {
               "Effect" : "Allow",
               "Action" : [ "sns:*" ],
               "Resource" : [ { "Ref" : "mytopic" } ]
            }, {
               "Effect" : "Deny",
               "Action" : [ "sns:*" ],
               "NotResource" : [ { "Ref" : "mytopic" } ]
            } ]
         }
      } ]
   }
}
```

### YAML<a name="quickref-iam-example-1.yaml"></a>

```
myuser:
  Type: AWS::IAM::User
  Properties:
    Path: "/"
    LoginProfile:
      Password: myP@ssW0rd
    Policies:
    - PolicyName: giveaccesstoqueueonly
      PolicyDocument:
        Version: '2012-10-17'
        Statement:
        - Effect: Allow
          Action:
          - sqs:*
          Resource:
          - !GetAtt myqueue.Arn
        - Effect: Deny
          Action:
          - sqs:*
          NotResource:
          - !GetAtt myqueue.Arn
    - PolicyName: giveaccesstotopiconly
      PolicyDocument:
        Version: '2012-10-17'
        Statement:
        - Effect: Allow
          Action:
          - sns:*
          Resource:
          - !Ref mytopic
        - Effect: Deny
          Action:
          - sns:*
          NotResource:
          - !Ref mytopic
```

## Declaring an IAM access key resource<a name="scenario-iam-accesskey"></a>

### <a name="quickref-iam-access-key"></a>

This snippet shows an `[AWS::IAM::AccessKey](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-iam-accesskey.html)` resource\. The `myaccesskey` resource creates an access key and assigns it to an IAM user that is declared as an `[AWS::IAM::User](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-iam-user.html)` resource in the template\.

#### JSON<a name="quickref-iam-example-2.json"></a>

```
1. "myaccesskey" : {
2.    "Type" : "AWS::IAM::AccessKey",
3.    "Properties" : {
4.       "UserName" : { "Ref" : "myuser" }
5.    }
6. }
```

#### YAML<a name="quickref-iam-example-2.yaml"></a>

```
1. myaccesskey:
2.   Type: AWS::IAM::AccessKey
3.   Properties:
4.     UserName:
5.       !Ref myuser
```

### <a name="quickref-iam-access-key-2"></a>

You can get the secret key for an `AWS::IAM::AccessKey` resource using the `Fn::GetAtt` function\. The only time that you can get the secret key for an AWS access key is when it is created\. One way to retrieve the secret key is to put it into an `Output` value\. You can get the access key using the `Ref` function\. The following `Output` value declarations get the access key and secret key for `myaccesskey`\.

#### JSON<a name="quickref-iam-example-3.json"></a>

```
1. "AccessKeyformyaccesskey" : {
2.    "Value" : { "Ref" : "myaccesskey" }
3. },
4. "SecretKeyformyaccesskey" : {
5.    "Value" : {
6.       "Fn::GetAtt" : [ "myaccesskey", "SecretAccessKey" ]
7.    }
8. }
```

#### YAML<a name="quickref-iam-example-3.yaml"></a>

```
1. AccessKeyformyaccesskey:
2.   Value:
3.     !Ref myaccesskey
4. SecretKeyformyaccesskey:
5.   Value: !GetAtt myaccesskey.SecretAccessKey
```

### <a name="quickref-iam-access-key-3"></a>

You can also pass the AWS access key and secret key to an EC2 instance or Auto Scaling group defined in the template\. The following `[AWS::EC2::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html)` declaration uses the `UserData` property to pass the access key and secret key for the `myaccesskey` resource\.

#### JSON<a name="quickref-iam-example-4.json"></a>

```
 1. "myinstance" : {
 2.    "Type" : "AWS::EC2::Instance",
 3.    "Properties" : {
 4.       "AvailabilityZone" : "us-east-1a",
 5.       "ImageId" : "ami-0ff8a91507f77f867",
 6.       "UserData" : {
 7.          "Fn::Base64" : {
 8.             "Fn::Join" : [
 9.                "", [
10.                   "ACCESS_KEY=", {
11.                      "Ref" : "myaccesskey"
12.                   },
13.                   "&",
14.                   "SECRET_KEY=",
15.                   {
16.                      "Fn::GetAtt" : [
17.                         "myaccesskey",
18.                         "SecretAccessKey"
19.                      ]
20.                   }
21.                ]
22.             ]
23.          }
24.       }
25.    }
26. }
```

#### YAML<a name="quickref-iam-example-4.yaml"></a>

```
1. myinstance:
2.   Type: AWS::EC2::Instance
3.   Properties:
4.     AvailabilityZone: "us-east-1a"
5.     ImageId: ami-0ff8a91507f77f867
6.     UserData:
7.       Fn::Base64: !Sub "ACCESS_KEY=${myaccesskey}&SECRET_KEY=${myaccesskey.SecretAccessKey}
```

## Declaring an IAM group resource<a name="scenario-iam-group"></a>

This snippet shows an `[AWS::IAM::Group](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-iam-group.html)` resource\. The group has a path \(`"/myapplication/"`\)\. The policy document named `myapppolicy` is added to the group to allow the group's users to perform all Amazon SQS actions on the Amazon SQS queue resource myqueue and deny access to all other Amazon SQS resources except `myqueue`\. 

To assign a policy to a resource, IAM requires the Amazon Resource Name \(ARN\) for the resource\. In the snippet, the `Fn::GetAtt` function gets the ARN of the `[AWS::SQS::Queue](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-sqs-queues.html)` resource queue\.

### JSON<a name="quickref-iam-example-5.json"></a>

```
 1. "mygroup" : {
 2.    "Type" : "AWS::IAM::Group",
 3.    "Properties" : {
 4.       "Path" : "/myapplication/",
 5.       "Policies" : [ {
 6.          "PolicyName" : "myapppolicy",
 7.          "PolicyDocument" : {
 8.             "Version": "2012-10-17",
 9.             "Statement" : [ {
10.                "Effect" : "Allow",
11.                "Action" : [ "sqs:*" ],
12.                "Resource" : [ {
13.                   "Fn::GetAtt" : [ "myqueue", "Arn" ]
14.                } ]
15.             },
16.             {
17.                "Effect" : "Deny",
18.                "Action" : [ "sqs:*" ],
19.                "NotResource" : [ { "Fn::GetAtt" : [ "myqueue", "Arn" ] } ]
20.             }
21.          ] }
22.       } ]
23.    }
24. }
```

### YAML<a name="quickref-iam-example-5.yaml"></a>

```
 1. mygroup:
 2.   Type: AWS::IAM::Group
 3.   Properties:
 4.     Path: "/myapplication/"
 5.     Policies:
 6.     - PolicyName: myapppolicy
 7.       PolicyDocument:
 8.         Version: '2012-10-17'
 9.         Statement:
10.         - Effect: Allow
11.           Action:
12.           - sqs:*
13.           Resource: !GetAtt myqueue.Arn
14.         - Effect: Deny
15.           Action:
16.           - sqs:*
17.           NotResource: !GetAtt myqueue.Arn
```

## Adding users to a group<a name="scenario-iam-addusertogroup"></a>

The `[AWS::IAM::UserToGroupAddition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-iam-addusertogroup.html)` resource adds users to a group\. In the following snippet, the `addUserToGroup` resource adds the following users to an existing group named `myexistinggroup2`: the existing user `existinguser1` and the user `myuser` which is declared as an `[AWS::IAM::User](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-iam-user.html)` resource in the template\.

### JSON<a name="quickref-iam-example-6.json"></a>

```
1. "addUserToGroup" : {
2.    "Type" : "AWS::IAM::UserToGroupAddition",
3.    "Properties" : {
4.       "GroupName" : "myexistinggroup2",
5.       "Users" : [ "existinguser1", { "Ref" : "myuser" } ]
6.    }
7. }
```

### YAML<a name="quickref-iam-example-6.yaml"></a>

```
1. addUserToGroup:
2.   Type: AWS::IAM::UserToGroupAddition
3.   Properties:
4.     GroupName: myexistinggroup2
5.     Users:
6.     - existinguser1
7.     - !Ref myuser
```

## Declaring an IAM policy<a name="scenario-iam-policy"></a>

This snippet shows how to create a policy and apply it to multiple groups using an `[AWS::IAM::Policy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iam-policy.html)` resource named `mypolicy`\. The `mypolicy` resource contains a `PolicyDocument` property that allows `GetObject`, `PutObject`, and `PutObjectAcl` actions on the objects in the S3 bucket represented by the ARN `arn:aws:s3:::myAWSBucket`\. The `mypolicy` resource applies the policy to an existing group named `myexistinggroup1` and a group `mygroup` that is declared in the template as an `[AWS::IAM::Group](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-iam-group.html)` resource\. This example shows how to apply a policy to a group using the `Groups` property; however, you can alternatively use the `Users` property to add a policy document to a list of users\.

**Important**  
The Amazon SNS policy actions that are [declared in the `AWS::IAM::Policy` resource](#scenario-iam-policy) differ from the Amazon SNS topic policy actions that are [declared in the `AWS::SNS::TopicPolicy` resource](#scenario-sns-policy)\. For example, the policy actions `sns:Unsubscribe` and `sns:SetSubscriptionAttributes` are valid for the `AWS::IAM::Policy` resource, but are invalid for the `AWS::SNS::TopicPolicy` resource\. For more information about valid Amazon SNS policy actions that you can use with the `AWS::IAM::Policy` resource, see [Special information for Amazon SNS policies](https://docs.aws.amazon.com/sns/latest/dg/AccessPolicyLanguage_SpecialInfo.html) in the *Amazon Simple Notification Service Developer Guide*\. 

### JSON<a name="quickref-iam-example-7.json"></a>

```
 1. "mypolicy" : {
 2.    "Type" : "AWS::IAM::Policy",
 3.    "Properties" : {
 4.       "PolicyName" : "mygrouppolicy",
 5.       "PolicyDocument" : {
 6.          "Version": "2012-10-17",
 7.          "Statement" : [ {
 8.             "Effect" : "Allow",
 9.             "Action" : [
10.                "s3:GetObject" , "s3:PutObject" , "s3:PutObjectAcl" ],
11.             "Resource" : "arn:aws:s3:::myAWSBucket/*"
12.          } ]
13.       },
14.       "Groups" : [ "myexistinggroup1", { "Ref" : "mygroup" } ]
15.    }
16. }
```

### YAML<a name="quickref-iam-example-7.yaml"></a>

```
 1. mypolicy:
 2.   Type: AWS::IAM::Policy
 3.   Properties:
 4.     PolicyName: mygrouppolicy
 5.     PolicyDocument:
 6.       Version: '2012-10-17'
 7.       Statement:
 8.       - Effect: Allow
 9.         Action:
10.         - s3:GetObject
11.         - s3:PutObject
12.         - s3:PutObjectAcl
13.         Resource: arn:aws:s3:::myAWSBucket/*
14.     Groups:
15.     - myexistinggroup1
16.     - !Ref mygroup
```

## Declaring an Amazon S3 bucket policy<a name="scenario-bucket-policy"></a>

This snippet shows how to create a policy and apply it to an Amazon S3 bucket using the `[AWS::S3::BucketPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.html)` resource\. The `mybucketpolicy` resource declares a policy document that allows the `user1` IAM user to perform the `GetObject` action on all objects in the S3 bucket to which this policy is applied\. In the snippet, the `Fn::GetAtt` function gets the ARN of the `user1` resource\. The `mybucketpolicy` resource applies the policy to the `[AWS::S3::BucketPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.html)` resource mybucket\. The `Ref` function gets the bucket name of the `mybucket` resource\. 

### JSON<a name="quickref-iam-example-8.json"></a>

```
 1. "mybucketpolicy" : {
 2.    "Type" : "AWS::S3::BucketPolicy",
 3.    "Properties" : {
 4.       "PolicyDocument" : {
 5.          "Id" : "MyPolicy",
 6.          "Version": "2012-10-17",
 7.          "Statement" : [ {
 8.             "Sid" : "ReadAccess",
 9.             "Action" : [ "s3:GetObject" ],
10.             "Effect" : "Allow",
11.             "Resource" : { "Fn::Join" : [
12.                   "", [ "arn:aws:s3:::", { "Ref" : "mybucket" } , "/*" ]
13.                ] },
14.             "Principal" : {
15.                "AWS" : { "Fn::GetAtt" : [ "user1", "Arn" ] }
16.             }
17.          } ]
18.       },
19.       "Bucket" : { "Ref" : "mybucket" }
20.    }
21. }
```

### YAML<a name="quickref-iam-example-8.yaml"></a>

```
 1. mybucketpolicy:
 2.   Type: AWS::S3::BucketPolicy
 3.   Properties:
 4.     PolicyDocument:
 5.       Id: MyPolicy
 6.       Version: '2012-10-17'
 7.       Statement:
 8.       - Sid: ReadAccess
 9.         Action:
10.         - s3:GetObject
11.         Effect: Allow
12.         Resource: !Sub "arn:aws:s3:::${mybucket}/*"
13.         Principal:
14.           AWS: !GetAtt user1.Arn
15.     Bucket: !Ref mybucket
```

## Declaring an Amazon SNS topic policy<a name="scenario-sns-policy"></a>

This snippet shows how to create a policy and apply it to an Amazon SNS topic using the `[AWS::SNS::TopicPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-sns-policy.html)` resource\. The `mysnspolicy` resource contains a `PolicyDocument` property that allows the `[AWS::IAM::User](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-iam-user.html)` resource `myuser` to perform the `Publish` action on an `[AWS::SNS::Topic](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-sns-topic.html)` resource `mytopic`\. In the snippet, the `Fn::GetAtt` function gets the ARN for the `myuser` resource and the `Ref` function gets the ARN for the `mytopic` resource\.

**Important**  
The Amazon SNS policy actions that are [declared in the `AWS::IAM::Policy` resource](#scenario-iam-policy) differ from the Amazon SNS topic policy actions that are [declared in the `AWS::SNS::TopicPolicy` resource](#scenario-sns-policy)\. For example, the policy actions `sns:Unsubscribe` and `sns:SetSubscriptionAttributes` are valid for the `AWS::IAM::Policy` resource, but are invalid for the `AWS::SNS::TopicPolicy` resource\. For more information about valid Amazon SNS policy actions that you can use with the `AWS::IAM::Policy` resource, see [Special information for Amazon SNS policies](https://docs.aws.amazon.com/sns/latest/dg/AccessPolicyLanguage_SpecialInfo.html) in the *Amazon Simple Notification Service Developer Guide*\. 

### JSON<a name="quickref-iam-example-9.json"></a>

```
 1. "mysnspolicy" : {
 2.    "Type" : "AWS::SNS::TopicPolicy",
 3.    "Properties" : {
 4.       "PolicyDocument" :  {
 5.          "Id" : "MyTopicPolicy",
 6.          "Version" : "2012-10-17",
 7.          "Statement" : [ {
 8.             "Sid" : "My-statement-id",
 9.             "Effect" : "Allow",
10.             "Principal" : {
11.                "AWS" : { "Fn::GetAtt" : [ "myuser", "Arn" ] }
12.             },
13.             "Action" : "sns:Publish",
14.             "Resource" : "*"
15.          } ]
16.       },
17.       "Topics" : [ { "Ref" : "mytopic" } ]
18.    }
19. }
```

### YAML<a name="quickref-iam-example-9.yaml"></a>

```
 1. mysnspolicy:
 2.   Type: AWS::SNS::TopicPolicy
 3.   Properties:
 4.     PolicyDocument:
 5.       Id: MyTopicPolicy
 6.       Version: '2012-10-17'
 7.       Statement:
 8.       - Sid: My-statement-id
 9.         Effect: Allow
10.         Principal:
11.           AWS: !GetAtt myuser.Arn
12.         Action: sns:Publish
13.         Resource: "*"
14.     Topics:
15.     - !Ref mytopic
```

## Declaring an Amazon SQS policy<a name="scenario-sqs-policy"></a>

This snippet shows how to create a policy and apply it to an Amazon SQS queue using the `[AWS::SQS::QueuePolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-sqs-policy.html)` resource\. The `PolicyDocument` property allows the existing user `myapp` \(specified by its ARN\) to perform the `SendMessage` action on an existing queue, which is specified by its URL, and an `[AWS::SQS::Queue](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-sqs-queues.html)` resource myqueue\. The [Ref](intrinsic-function-reference-ref.md) function gets the URL for the `myqueue` resource\. 

### JSON<a name="quickref-iam-example-10.json"></a>

```
 1. "mysqspolicy" : {
 2.    "Type" : "AWS::SQS::QueuePolicy",
 3.    "Properties" : {
 4.       "PolicyDocument" : {
 5.          "Id" : "MyQueuePolicy",
 6.          "Version" : "2012-10-17",
 7.          "Statement" : [ {
 8.             "Sid" : "Allow-User-SendMessage",
 9.             "Effect" : "Allow",
10.             "Principal" : {
11.                "AWS" : "arn:aws:iam::123456789012:user/myapp"
12.             },
13.             "Action" : [ "sqs:SendMessage" ],
14.             "Resource" : "*"
15.          } ]
16.       },
17.       "Queues" : [
18.          "https://sqs.us-east-2.amazonaws.com/123456789012/myexistingqueue",
19.          { "Ref" : "myqueue" }
20.       ]
21.    }
22. }
```

### YAML<a name="quickref-iam-example-10.yaml"></a>

```
 1. mysqspolicy:
 2.   Type: AWS::SQS::QueuePolicy
 3.   Properties:
 4.     PolicyDocument:
 5.       Id: MyQueuePolicy
 6.       Version: '2012-10-17'
 7.       Statement:
 8.       - Sid: Allow-User-SendMessage
 9.         Effect: Allow
10.         Principal:
11.           AWS: arn:aws:iam::123456789012:user/myapp
12.         Action:
13.         - sqs:SendMessage
14.         Resource: "*"
15.     Queues:
16.     - https://sqs.us-east-2.amazonaws.com/123456789012/myexistingqueue
17.     - !Ref myqueue
```

## IAM role template examples<a name="scenarios-iamroles"></a>

This section provides CloudFormation template examples for IAM Roles for EC2 Instances\.

For more information about IAM roles, see [Working with Roles](http://docs.aws.amazon.com/IAM/latest/UserGuide/WorkingWithRoles.html) in the *AWS Identity and Access Management User Guide*\.

### IAM role with EC2<a name="scenario-iamrole-ec2"></a>

In this example, the instance profile is referenced by the `IamInstanceProfile` property of the EC2 Instance\. Both the instance policy and role policy reference `[AWS::IAM::Role](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iam-role.html)`\.

#### JSON<a name="quickref-iam-example-11.json"></a>

```
{
   "AWSTemplateFormatVersion": "2010-09-09",
   "Resources": {
      "myEC2Instance": {
         "Type": "AWS::EC2::Instance",
         "Version": "2009-05-15",
         "Properties": {
            "ImageId": "ami-0ff8a91507f77f867",
            "InstanceType": "m1.small",
            "Monitoring": "true",
            "DisableApiTermination": "false",
            "IamInstanceProfile": {
               "Ref": "RootInstanceProfile"
            }
         }
      },
      "RootRole": {
         "Type": "AWS::IAM::Role",
         "Properties": {
            "AssumeRolePolicyDocument": {
               "Version" : "2012-10-17",
               "Statement": [ {
                  "Effect": "Allow",
                  "Principal": {
                     "Service": [ "ec2.amazonaws.com" ]
                  },
                  "Action": [ "sts:AssumeRole" ]
               } ]
            },
            "Path": "/"
         }
      },
      "RolePolicies": {
         "Type": "AWS::IAM::Policy",
         "Properties": {
            "PolicyName": "root",
            "PolicyDocument": {
               "Version" : "2012-10-17",
               "Statement": [ {
                  "Effect": "Allow",
                  "Action": "*",
                  "Resource": "*"
               } ]
            },
            "Roles": [ { "Ref": "RootRole" } ]
         }
      },
      "RootInstanceProfile": {
         "Type": "AWS::IAM::InstanceProfile",
         "Properties": {
            "Path": "/",
            "Roles": [ { "Ref": "RootRole" } ]
         }
      }
   }
}
```

#### YAML<a name="quickref-iam-example-11.yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Resources:
  myEC2Instance:
    Type: AWS::EC2::Instance
    Version: '2009-05-15'
    Properties:
      ImageId: ami-0ff8a91507f77f867
      InstanceType: m1.small
      Monitoring: 'true'
      DisableApiTermination: 'false'
      IamInstanceProfile:
        !Ref RootInstanceProfile
  RootRole:
    Type: AWS::IAM::Role
    Properties:
      AssumeRolePolicyDocument:
        Version: '2012-10-17'
        Statement:
        - Effect: Allow
          Principal:
            Service:
            - ec2.amazonaws.com
          Action:
          - sts:AssumeRole
      Path: "/"
  RolePolicies:
    Type: AWS::IAM::Policy
    Properties:
      PolicyName: root
      PolicyDocument:
        Version: '2012-10-17'
        Statement:
        - Effect: Allow
          Action: "*"
          Resource: "*"
      Roles:
      - !Ref RootRole
  RootInstanceProfile:
    Type: AWS::IAM::InstanceProfile
    Properties:
      Path: "/"
      Roles:
      - !Ref RootRole
```

### IAM role with AutoScaling group<a name="scenario-iamrole-asg"></a>

In this example, the instance profile is referenced by the `IamInstanceProfile` property of an AutoScaling Group Launch Configuration\.

#### JSON<a name="quickref-iam-example-12.json"></a>

```
{
   "AWSTemplateFormatVersion": "2010-09-09",
   "Resources": {
      "myLCOne": {
         "Type": "AWS::AutoScaling::LaunchConfiguration",
         "Version": "2009-05-15",
         "Properties": {
            "ImageId": "ami-0ff8a91507f77f867",
            "InstanceType": "m1.small",
            "InstanceMonitoring": "true",
            "IamInstanceProfile": { "Ref": "RootInstanceProfile" }
         }
      },
      "myASGrpOne": {
         "Type": "AWS::AutoScaling::AutoScalingGroup",
         "Version": "2009-05-15",
         "Properties": {
            "AvailabilityZones": [ "us-east-1a" ],
            "LaunchConfigurationName": { "Ref": "myLCOne" },
            "MinSize": "0",
            "MaxSize": "0",
            "HealthCheckType": "EC2",
            "HealthCheckGracePeriod": "120"
         }
      },
      "RootRole": {
         "Type": "AWS::IAM::Role",
         "Properties": {
            "AssumeRolePolicyDocument": {
               "Version" : "2012-10-17",
               "Statement": [ {
                  "Effect": "Allow",
                  "Principal": {
                     "Service": [ "ec2.amazonaws.com" ]
                  },
                  "Action": [ "sts:AssumeRole" ]
               } ]
            },
            "Path": "/"
         }
      },
      "RolePolicies": {
         "Type": "AWS::IAM::Policy",
         "Properties": {
            "PolicyName": "root",
            "PolicyDocument": {
               "Version" : "2012-10-17",
               "Statement": [ {
                  "Effect": "Allow",
                  "Action": "*",
                  "Resource": "*"
               } ]
            },
            "Roles": [ { "Ref": "RootRole" } ]
         }
      },
      "RootInstanceProfile": {
         "Type": "AWS::IAM::InstanceProfile",
         "Properties": {
            "Path": "/",
            "Roles": [ { "Ref": "RootRole" } ]
         }
      }
   }
}
```

#### YAML<a name="quickref-iam-example-12.yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Resources:
  myLCOne:
    Type: AWS::AutoScaling::LaunchConfiguration
    Version: '2009-05-15'
    Properties:
      ImageId: ami-0ff8a91507f77f867
      InstanceType: m1.small
      InstanceMonitoring: 'true'
      IamInstanceProfile:
        !Ref RootInstanceProfile
  myASGrpOne:
    Type: AWS::AutoScaling::AutoScalingGroup
    Version: '2009-05-15'
    Properties:
      AvailabilityZones:
      - "us-east-1a"
      LaunchConfigurationName:
        !Ref myLCOne
      MinSize: '0'
      MaxSize: '0'
      HealthCheckType: EC2
      HealthCheckGracePeriod: '120'
  RootRole:
    Type: AWS::IAM::Role
    Properties:
      AssumeRolePolicyDocument:
        Version: '2012-10-17'
        Statement:
        - Effect: Allow
          Principal:
            Service:
            - ec2.amazonaws.com
          Action:
          - sts:AssumeRole
      Path: "/"
  RolePolicies:
    Type: AWS::IAM::Policy
    Properties:
      PolicyName: root
      PolicyDocument:
        Version: '2012-10-17'
        Statement:
        - Effect: Allow
          Action: "*"
          Resource: "*"
      Roles:
      - !Ref RootRole
  RootInstanceProfile:
    Type: AWS::IAM::InstanceProfile
    Properties:
      Path: "/"
      Roles:
      - !Ref RootRole
```