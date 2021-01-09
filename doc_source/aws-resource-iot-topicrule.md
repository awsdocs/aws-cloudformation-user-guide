# AWS::IoT::TopicRule<a name="aws-resource-iot-topicrule"></a>

Use the `AWS::IoT::TopicRule` resource to declare an AWS IoT rule\. For information about working with AWS IoT rules, see [Rules for AWS IoT](https://docs.aws.amazon.com/iot/latest/developerguide/iot-rules.html) in the *AWS IoT Developer Guide*\.

## Syntax<a name="aws-resource-iot-topicrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iot-topicrule-syntax.json"></a>

```
{
  "Type" : "AWS::IoT::TopicRule",
  "Properties" : {
      "[RuleName](#cfn-iot-topicrule-rulename)" : String,
      "[TopicRulePayload](#cfn-iot-topicrule-topicrulepayload)" : TopicRulePayload
    }
}
```

### YAML<a name="aws-resource-iot-topicrule-syntax.yaml"></a>

```
Type: AWS::IoT::TopicRule
Properties: 
  [RuleName](#cfn-iot-topicrule-rulename): String
  [TopicRulePayload](#cfn-iot-topicrule-topicrulepayload): 
    TopicRulePayload
```

## Properties<a name="aws-resource-iot-topicrule-properties"></a>

`RuleName`  <a name="cfn-iot-topicrule-rulename"></a>
The name of the rule\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TopicRulePayload`  <a name="cfn-iot-topicrule-topicrulepayload"></a>
The rule payload\.  
*Required*: Yes  
*Type*: [TopicRulePayload](aws-properties-iot-topicrule-topicrulepayload.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-iot-topicrule-return-values"></a>

### Ref<a name="aws-resource-iot-topicrule-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the topic rule name\. For example:

 `{ "Ref": "MyTopicRule" }` 

For a stack named My\-Stack \(the \- character is omitted\), a value similar to the following is returned:

 `MyStackMyTopicRule12ABC3D456EFG` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-iot-topicrule-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-iot-topicrule-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the AWS IoT rule, such as `arn:aws:iot:us-east-2:123456789012:rule/MyIoTRule`\.

## Examples<a name="aws-resource-iot-topicrule--examples"></a>

### <a name="aws-resource-iot-topicrule--examples--"></a>

The following example declares an AWS IoT rule\.

#### JSON<a name="aws-resource-iot-topicrule--examples----json"></a>

```
            {
   "AWSTemplateFormatVersion":"2010-09-09",
   "Resources":{
      "MyTopicRule":{
         "Type":"AWS::IoT::TopicRule",
         "Properties":{
            "RuleName":{
               "Ref":"NameParameter"
            },
            "TopicRulePayload":{
               "RuleDisabled":"true",
               "Sql":"SELECT temp FROM 'SomeTopic' WHERE temp > 60",
               "Actions":[
                  {
                     "S3":{
                        "BucketName":{
                           "Ref":"MyBucket"
                        },
                        "RoleArn":{
                           "Fn::GetAtt":[
                              "MyRole",
                              "Arn"
                           ]
                        },
                        "Key":"MyKey.txt"
                     }
                  }
               ]
            },
            "MyBucket":{
               "Type":"AWS::S3::Bucket",
               "Properties":{
                  
               }
            },
            "MyRole":{
               "Type":"AWS::IAM::Role",
               "Properties":{
                  "AssumeRolePolicyDocument":{
                     "Version":"2012-10-17",
                     "Statement":[
                        {
                           "Effect":"Allow",
                           "Principal":{
                              "Service":[
                                 "iot.amazonaws.com"
                              ]
                           },
                           "Action":[
                              "sts:AssumeRole"
                           ]
                        }
                     ]
                  }
               }
            }
         },
         "Parameters":{
            "NameParameter":{
               "Type":"String"
            }
         }
      }
   }
}
```

#### YAML<a name="aws-resource-iot-topicrule--examples----yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Resources:
  MyTopicRule:
    Type: AWS::IoT::TopicRule
    Properties:
      RuleName:
        Ref: NameParameter
      TopicRulePayload:
        RuleDisabled: 'true'
        Sql: SELECT temp FROM 'SomeTopic' WHERE temp > 60
        Actions:
        - S3:
            BucketName:
              Ref: MyBucket
            RoleArn:
              Fn::GetAtt:
              - MyRole
              - Arn
            Key: MyKey.txt
      MyBucket:
        Type: AWS::S3::Bucket
        Properties: {}
      MyRole:
        Type: AWS::IAM::Role
        Properties:
          AssumeRolePolicyDocument:
            Version: '2012-10-17'
            Statement:
            - Effect: Allow
              Principal:
                Service:
                - iot.amazonaws.com
              Action:
              - sts:AssumeRole
    Parameters:
      NameParameter:
        Type: String
```