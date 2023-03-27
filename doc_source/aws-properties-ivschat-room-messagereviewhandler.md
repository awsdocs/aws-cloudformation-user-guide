# AWS::IVSChat::Room MessageReviewHandler<a name="aws-properties-ivschat-room-messagereviewhandler"></a>

The MessageReviewHandler property type specifies configuration information for optional message review\.

## Syntax<a name="aws-properties-ivschat-room-messagereviewhandler-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ivschat-room-messagereviewhandler-syntax.json"></a>

```
{
  "[FallbackResult](#cfn-ivschat-room-messagereviewhandler-fallbackresult)" : String,
  "[Uri](#cfn-ivschat-room-messagereviewhandler-uri)" : String
}
```

### YAML<a name="aws-properties-ivschat-room-messagereviewhandler-syntax.yaml"></a>

```
  [FallbackResult](#cfn-ivschat-room-messagereviewhandler-fallbackresult): String
  [Uri](#cfn-ivschat-room-messagereviewhandler-uri): String
```

## Properties<a name="aws-properties-ivschat-room-messagereviewhandler-properties"></a>

`FallbackResult`  <a name="cfn-ivschat-room-messagereviewhandler-fallbackresult"></a>
Specifies the fallback behavior \(whether the message is allowed or denied\) if the handler does not return a valid response, encounters an error, or times out\. \(For the timeout period, see [ Service Quotas](https://docs.aws.amazon.com/ivs/latest/userguide/service-quotas.html)\.\) If allowed, the message is delivered with returned content to all users connected to the room\. If denied, the message is not delivered to any user\.  
*Default*: `ALLOW`  
*Required*: No  
*Type*: String  
*Allowed values*: `ALLOW | DENY`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Uri`  <a name="cfn-ivschat-room-messagereviewhandler-uri"></a>
Identifier of the message review handler\. Currently this must be an ARN of a lambda function\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `170`  
*Pattern*: `^$|^arn:aws:lambda:[a-z0-9-]+:[0-9]{12}:function:.+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-ivschat-room-messagereviewhandler--examples"></a>



### Room Message Review Handler Template Examples<a name="aws-properties-ivschat-room-messagereviewhandler--examples--Room_Message_Review_Handler_Template_Examples"></a>

The following examples specify an Amazon IVS Chat Room with message review\.

#### JSON<a name="aws-properties-ivschat-room-messagereviewhandler--examples--Room_Message_Review_Handler_Template_Examples--json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Resources": {
    "MessageReviewHandlerRole": {
      "Type": "AWS::IAM::Role",
      "Properties": {
        "AssumeRolePolicyDocument": {
          "Version": "2012-10-17",
          "Statement": {
            "Effect": "Allow",
            "Principal": {
              "Service": "lambda.amazonaws.com"
            },
            "Action": "sts:AssumeRole"
          }
        }
      }
    },
    "MessageReviewHandler": {
      "Type": "AWS::Lambda::Function",
      "Properties": {
        "Handler": "index.handler",
        "Role": {
          "Fn::GetAtt": [
            "MessageReviewHandlerRole",
            "Arn"
          ]
        },
        "Runtime": "nodejs12.x",
        "Code": {
          "S3Bucket":"my-bucket",
          "S3Key": "function.zip"
        }
      }
    },
    "MessageReviewHandlerPermission": {
      "Type": "AWS::Lambda::Permission",
      "Properties": {
        "Principal": "ivschat.amazonaws.com",
        "Action": "lambda:InvokeFunction",
        "FunctionName": {
          "Ref": "MessageReviewHandler"
        },
        "SourceAccount": {
          "Ref": "AWS::AccountId"
        },
        "SourceArn": {
          "Fn::Sub": "arn:${AWS::Partition}:ivschat:${AWS::Region}:${AWS::AccountId}:room/*"
        }
      }
    },
    "Room": {
      "Type": "AWS::IVSChat::Room",
      "Properties": {
        "Name": "MyRoom",
        "MessageReviewHandler": {
          "FallbackResult": "ALLOW",
          "Uri": {
            "Fn::GetAtt": [
              "MessageReviewHandler",
              "Arn"
            ]
          }
        }
      },
      "DependsOn": "MessageReviewHandlerPermission"
    }
  }
}
```

#### YAML<a name="aws-properties-ivschat-room-messagereviewhandler--examples--Room_Message_Review_Handler_Template_Examples--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  MessageReviewHandlerRole:
    Type: AWS::IAM::Role
    Properties:
      AssumeRolePolicyDocument:
        Version: 2012-10-17
        Statement:
          Effect: Allow
          Principal:
            Service: lambda.amazonaws.com
          Action: sts:AssumeRole
  MessageReviewHandler:
    Type: AWS::Lambda::Function
    Properties:
      Handler: index.handler
      Role: !GetAtt MessageReviewHandlerRole.Arn
      Runtime: nodejs12.x
      Code:
        S3Bucket: my-bucket
        S3Key: function.zip
  MessageReviewHandlerPermission:
    Type: AWS::Lambda::Permission
    Properties:
      Principal: ivschat.amazonaws.com
      Action: lambda:InvokeFunction
      FunctionName: !Ref MessageReviewHandler
      SourceAccount: !Ref AWS::AccountId
      SourceArn: !Sub arn:${AWS::Partition}:ivschat:${AWS::Region}:${AWS::AccountId}:room/*
  Room:
    Type: AWS::IVSChat::Room
    Properties:
      Name: MyRoom
      MessageReviewHandler:
        FallbackResult: ALLOW
        Uri: !GetAtt MessageReviewHandler.Arn
    DependsOn: MessageReviewHandlerPermission
```