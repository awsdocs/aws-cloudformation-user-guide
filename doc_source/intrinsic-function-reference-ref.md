# `Ref`<a name="intrinsic-function-reference-ref"></a>

The intrinsic function `Ref` returns the value of the specified *parameter* or *resource*\. When the [`AWS::LanguageExtensions` transform](transform-aws-languageextensions.md) transform is used, you can use intrinsic functions as a parameter to [`Ref`](#intrinsic-function-reference-ref) and [`Fn::GetAtt`](intrinsic-function-reference-getatt.md)\.
+ When you specify a parameter's logical name, it returns the value of the parameter\.
+ When you specify a resource's logical name, it returns a value that you can typically use to refer to that resource, such as a [physical ID](resources-section-structure.md)\.
+ When you specify an intrinsic function, it returns the output of that function\.

When you are declaring a resource in a template and you need to specify another template resource by name, you can use the `Ref` to refer to that other resource\. In general, `Ref` returns the name of the resource\. For example, a reference to an [AWS::AutoScaling::AutoScalingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html) returns the name of that Auto Scaling group resource\.

For some resources, an identifier is returned that has another significant meaning in the context of the resource\. An [AWS::EC2::EIP](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-eip.html) resource, for instance, returns the IP address, and an [AWS::EC2::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html) returns the instance ID\.

**Tip**  
You can also use `Ref` to add values to [Outputs](outputs-section-structure.md) messages\.

For more information about `Ref` return values for a particular resource or property, refer to the documentation for that resource or property in the [Resource and property reference](aws-template-resource-type-ref.md)\.

## Declaration<a name="ref-declaration"></a>

### JSON<a name="intrinsic-function-reference-ref-syntax.json"></a>

```
{ "Ref" : "logicalName" }
```

```
{ "Ref" : "IntrinsicFunction" }
```

### YAML<a name="intrinsic-function-reference-ref-syntax.yaml"></a>

Syntax for the full function name:

```
Ref: logicalName
```

```
Ref: IntrinsicFunction
```

Syntax for the short form:

```
!Ref logicalName
```

```
!Ref IntrinsicFunction
```

## Parameters<a name="ref-parameters"></a>

logicalName  
The logical name of the resource or parameter you want to reference\.

IntrinsicFunction  
The intrinsic function that resolves to a valid string\. It should contain references to parameters or identifiers, and should not contain resource logical identifiers\.

## Return value<a name="ref-return-value"></a>

When the parameter is a *logicalName*, the return value is the physical ID of the resource or the value of the parameter\.

When the parameter is an *IntrinsicFunction*, the return value is the return value from the intrinsic function

## Examples<a name="ref-examples"></a>

### Example<a name="ref-example"></a>

The following resource declaration for an Elastic IP address needs the instance ID of an EC2 instance and uses the `Ref` function to specify the instance ID of the `MyEC2Instance` resource:

#### JSON<a name="intrinsic-function-reference-ref-example.json"></a>

```
"MyEIP" : {
   "Type" : "AWS::EC2::EIP",
   "Properties" : {
      "InstanceId" : { "Ref" : "MyEC2Instance" }
   }
}
```

#### YAML<a name="intrinsic-function-reference-ref-example.yaml"></a>

```
MyEIP:
  Type: "AWS::EC2::EIP"
  Properties:
    InstanceId: !Ref MyEC2Instance
```

### Example generating identifier for multiple stages<a name="ref-example-intrinsic-functions-multiple-stages"></a>

This example demonstrates how to use the `Fn::Sub` intrinsic function to substitute values for the Identifier for different stages\. The `Ref` and the `Fn::GetAtt` functions can then be used to reference the appropriate values, based on the input for the stage\. `Fn::Sub` is first used with `Fn::GetAtt` to obtain the ARN of the appropriate Amazon SQS queue to set the dimensions of the Amazon CloudWatch alarm\. Next, [`Fn::Join`](intrinsic-function-reference-join.md) is used with `Ref` to create the logical ID string of the `Stage` parameter\. 

#### JSON<a name="ref-example-intrinsic-functions-multiple-stages.json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Transform": "AWS::LanguageExtensions",
    "Parameters": {
        "Stage": {
            "Type": "String",
            "Default": "Dev",
            "AllowedValues": [
                "Dev",
                "Prod"
            ]
        }
    },
    "Conditions": {
        "isProd": {
            "Fn::Equals": [
                {"Ref": "Stage"},
                "Prod"
            ]
        },
        "isDev": {
            "Fn::Equals": [
                {"Ref": "Stage"},
                "Dev"
            ]
        }
    },
    "Resources": {
        "DevQueue": {
            "Type": "AWS::SQS::Queue",
            "Condition": "isDev",
            "Properties": {
                "QueueName": {"Fn::Sub": "My${Stage}Queue"}
            }
        },
        "ProdQueue": {
            "Type": "AWS::SQS::Queue",
            "Condition": "isProd",
            "Properties": {
                "QueueName": {"Fn::Sub": "My${Stage}Queue"}
            }
        },
        "DevTopic": {
            "Condition": "isDev",
            "Type": "AWS::SNS::Topic"
        },
        "ProdTopic": {
            "Condition": "isProd",
            "Type": "AWS::SNS::Topic"
        },
        "MyAlarm": {
            "Type": "AWS::CloudWatch::Alarm",
            "Properties": {
                "AlarmDescription": "Alarm if queue depth grows beyond 10 messages",
                "Namespace": "AWS/SQS",
                "MetricName": "ApproximateNumberOfMessagesVisible",
                "Dimensions":[
                    {
                        "Name": {"Fn::Sub": "${Stage}Queue"},
                        "Value": {"Fn::GetAtt": [{"Fn::Sub": "${Stage}Queue"}, "QueueName"]}
                    }
                ],
                "Statistic": "Sum",
                "Period": 300,
                "EvaluationPeriods": 1,
                "Threshold": 10,
                "ComparisonOperator": "GreaterThanThreshold",
                "AlarmActions": [
                    {
                        "Ref": {"Fn::Join": ["", [{"Ref": "Stage"}, "Topic"]]}
                    }
                ]
            }
        }
    }
}
```

#### YAML<a name="ref-example-intrinsic-functions-multiple-stages.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Transform: 'AWS::LanguageExtensions'
Parameters:
  Stage:
    Type: String
    Default: Dev
    AllowedValues:
      - Dev
      - Prod
Conditions:
  isProd: !Equals 
    - !Ref Stage
    - Prod
  isDev: !Equals 
    - !Ref Stage
    - Dev
Resources:
  DevQueue:
    Type: 'AWS::SQS::Queue'
    Condition: isDev
    Properties:
      QueueName: !Sub 'My${Stage}Queue'
  ProdQueue:
    Type: 'AWS::SQS::Queue'
    Condition: isProd
    Properties:
      QueueName: !Sub 'My${Stage}Queue'
  DevTopic:
    Condition: isDev
    Type: 'AWS::SNS::Topic'
  ProdTopic:
    Condition: isProd
    Type: 'AWS::SNS::Topic'
  MyAlarm:
    Type: 'AWS::CloudWatch::Alarm'
    Properties:
      AlarmDescription: Alarm if queue depth grows beyond 10 messages
      Namespace: AWS/SQS
      MetricName: ApproximateNumberOfMessagesVisible
      Dimensions:
        - Name: !Sub '${Stage}Queue'
          Value: !GetAtt 
            - !Sub '${Stage}Queue'
            - QueueName
      Statistic: Sum
      Period: 300
      EvaluationPeriods: 1
      Threshold: 10
      ComparisonOperator: GreaterThanThreshold
      AlarmActions:
        - !Ref 
          'Fn::Join':
            - ''
            - - !Ref Stage
              - Topic
```

## Supported functions<a name="ref-supported-functions"></a>

When the [`AWS::LanguageExtensions` transform](transform-aws-languageextensions.md) transform is used, within the `Ref` function, you can use the following functions\.
+ ``Fn::Base64``
+ ``Fn::FindInMap``
+ ``Fn::If``
+ ``Fn::Join``
+ ``Fn::Sub``
+ ``Fn::ToJsonString``
+ `Ref`