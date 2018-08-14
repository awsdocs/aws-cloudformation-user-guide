# AWS::IoT::TopicRule<a name="aws-resource-iot-topicrule"></a>

Use the `AWS::IoT::TopicRule` resource to declare an AWS IoT rule\.

For information about working with AWS IoT rules, see [Rules for AWS IoT](http://docs.aws.amazon.com/iot/latest/developerguide/iot-rules.html) in the *AWS IoT Developer Guide*\.

## Syntax<a name="aws-resource-iot-topicrule-syntax"></a>

### JSON<a name="aws-resource-iot-topicrule-syntax.json"></a>

```
{
   "Type": "AWS::IoT::TopicRule",
   "Properties": {
      "[RuleName](#cfn-iot-topicrule-rulename)": String,
      "[TopicRulePayload](#cfn-iot-topicrule-topicrulepayload)": TopicRulePayLoad
   }
}
```

### YAML<a name="aws-resource-iot-topicrule-syntax.yaml"></a>

```
Type: "AWS::IoT::TopicRule"
Properties:
  [RuleName](#cfn-iot-topicrule-rulename): String
  [TopicRulePayload](#cfn-iot-topicrule-topicrulepayload): TopicRulePayLoad
```

## Properties<a name="aws-resource-iot-topicrule-properties"></a>

`RuleName`  <a name="cfn-iot-topicrule-rulename"></a>
The name \(the physical ID\) of the AWS IoT rule\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`TopicRulePayload`  <a name="cfn-iot-topicrule-topicrulepayload"></a>
The actions associated with the AWS IoT rule\.  
*Required*: Yes  
*Type*: [`TopicRulePayload`](aws-properties-iot-topicrule-topicrulepayload.md) object  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Values<a name="aws-resource-iot-topicrule-returnvalues"></a>

### Ref<a name="aws-resource-iot-topicrule-ref"></a>

When you provide the logical ID of this resource to the `Ref` intrinsic function, `Ref` returns the topic rule name\. For example:

```
{ "Ref": "MyTopicRule" }
```

For a stack named `My-Stack` \(the `–` character is omitted\), a value similar to the following is returned:

```
MyStackMyTopicRule12ABC3D456EFG
```

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="aws-resource-iot-topicrule-getatt"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`Arn`  
The Amazon Resource Name \(ARN\) of the AWS IoT rule, such as `arn:aws:iot:us-east-2:123456789012:rule/MyIoTRule`\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## Example<a name="aws-resource-iot-topicrule-examples"></a>

The following example declares an AWS IoT rule\.

### JSON<a name="aws-resource-iot-topicrule-example.json"></a>

```
{
   "AWSTemplateFormatVersion": "2010-09-09",
   "Resources": {
      "MyTopicRule": {
         "Type": "AWS::IoT::TopicRule",
         "Properties": {
            "RuleName": {
               "Ref": "NameParameter"
            },
            "TopicRulePayload": {
               "RuleDisabled": "true",
               "Sql": "SELECT temp FROM 'SomeTopic' WHERE temp > 60",
               "Actions": [{
                  "S3": {
                     "BucketName": {
                        "Ref": "MyBucket"
                     },
                     "RoleArn": {
                        "Fn::GetAtt": ["MyRole", "Arn"]
                     },
                     "Key": "MyKey.txt"
                  }
               }]
            }
         }
      },
      "MyBucket": {
         "Type": "AWS::S3::Bucket",
         "Properties": {}
      },
      "MyRole": {
         "Type": "AWS::IAM::Role",
         "Properties": {
            "AssumeRolePolicyDocument": {
               "Version": "2012-10-17",
               "Statement": [{
                  "Effect": "Allow",
                  "Principal": {
                     "Service": [
                        "iot.amazonaws.com"
                     ]
                  },
                  "Action": [
                     "sts:AssumeRole"
                  ]
               }]
            }
         }
      }
   },
   "Parameters": {
      "NameParameter": {
         "Type": "String"
      }
   }
}
```

### YAML<a name="aws-resource-iot-topicrule-example.yaml"></a>

```
AWSTemplateFormatVersion: "2010-09-09"
Resources: 
  MyTopicRule: 
    Type: "AWS::IoT::TopicRule"
    Properties: 
      RuleName: 
        Ref: "NameParameter"
      TopicRulePayload: 
        RuleDisabled: "true"
        Sql: >-
          Select temp FROM 'SomeTopic' WHERE temp > 60
        Actions: 
          - 
            S3: 
              BucketName: 
                Ref: "MyBucket"
              RoleArn: 
                Fn::GetAtt: 
                  - "MyRole"
                  - "Arn"
              Key: "MyKey.txt"
  MyBucket: 
    Type: "AWS::S3::Bucket"
    Properties:
  MyRole: 
    Type: "AWS::IAM::Role"
    Properties: 
      AssumeRolePolicyDocument: 
        Version: "2012-10-17"
        Statement: 
          - 
            Effect: "Allow"
            Principal: 
              Service: 
                - "iot.amazonaws.com"
            Action: 
              - "sts:AssumeRole"
Parameters: 
  NameParameter: 
    Type: "String"
```