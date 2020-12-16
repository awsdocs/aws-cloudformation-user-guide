# AWS::IoTEvents::DetectorModel<a name="aws-resource-iotevents-detectormodel"></a>

The AWS::IoTEvents::DetectorModel resource creates a detector model\. You create a *detector model* \(a model of your equipment or process\) using *states*\. For each state, you define conditional \(Boolean\) logic that evaluates the incoming inputs to detect significant events\. When an event is detected, it can change the state or trigger custom\-built or predefined actions using other AWS services\. You can define additional events that trigger actions when entering or exiting a state and, optionally, when a condition is met\. For more information, see [ How to Use AWS IoT Events](https://docs.aws.amazon.com/iotevents/latest/developerguide/how-to-use-iotevents.html) in the *AWS IoT Events Developer Guide*\.

**Note**  
When you successfully update a detector model \(using the AWS IoT Events console, AWS IoT Events API or CLI commands, or AWS CloudFormation\) all detector instances created by the model are reset to their initial states\. \(The detector's `state`, and the values of any variables and timers are reset\.\)  
When you successfully update a detector model \(using the AWS IoT Events console, AWS IoT Events API or CLI commands, or AWS CloudFormation\) the version number of the detector model is incremented\. \(A detector model with version number 1 before the update has version number 2 after the update succeeds\.\)  
If you attempt to update a detector model using AWS CloudFormation and the update does not succeed, the system may, in some cases, restore the original detector model\. When this occurs, the detector model's version is incremented twice \(for example, from version 1 to version 3\) and the detector instances are reset\.  
Also, be aware that if you attempt to update several detector models at once using AWS CloudFormation, some updates may succeed and others fail\. In this case, the effects on each detector model's detector instances and version number depend on whether the update succeeded or failed, with the results as stated\.

## Syntax<a name="aws-resource-iotevents-detectormodel-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iotevents-detectormodel-syntax.json"></a>

```
{
  "Type" : "AWS::IoTEvents::DetectorModel",
  "Properties" : {
      "[DetectorModelDefinition](#cfn-iotevents-detectormodel-detectormodeldefinition)" : DetectorModelDefinition,
      "[DetectorModelDescription](#cfn-iotevents-detectormodel-detectormodeldescription)" : String,
      "[DetectorModelName](#cfn-iotevents-detectormodel-detectormodelname)" : String,
      "[EvaluationMethod](#cfn-iotevents-detectormodel-evaluationmethod)" : String,
      "[Key](#cfn-iotevents-detectormodel-key)" : String,
      "[RoleArn](#cfn-iotevents-detectormodel-rolearn)" : String,
      "[Tags](#cfn-iotevents-detectormodel-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-iotevents-detectormodel-syntax.yaml"></a>

```
Type: AWS::IoTEvents::DetectorModel
Properties: 
  [DetectorModelDefinition](#cfn-iotevents-detectormodel-detectormodeldefinition): 
    DetectorModelDefinition
  [DetectorModelDescription](#cfn-iotevents-detectormodel-detectormodeldescription): String
  [DetectorModelName](#cfn-iotevents-detectormodel-detectormodelname): String
  [EvaluationMethod](#cfn-iotevents-detectormodel-evaluationmethod): String
  [Key](#cfn-iotevents-detectormodel-key): String
  [RoleArn](#cfn-iotevents-detectormodel-rolearn): String
  [Tags](#cfn-iotevents-detectormodel-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-iotevents-detectormodel-properties"></a>

`DetectorModelDefinition`  <a name="cfn-iotevents-detectormodel-detectormodeldefinition"></a>
Information that defines how a detector operates\.  
*Required*: No  
*Type*: [DetectorModelDefinition](aws-properties-iotevents-detectormodel-detectormodeldefinition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DetectorModelDescription`  <a name="cfn-iotevents-detectormodel-detectormodeldescription"></a>
A brief description of the detector model\.  
*Required*: No  
*Type*: String  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DetectorModelName`  <a name="cfn-iotevents-detectormodel-detectormodelname"></a>
The name of the detector model\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `^[a-zA-Z0-9_-]+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EvaluationMethod`  <a name="cfn-iotevents-detectormodel-evaluationmethod"></a>
Information about the order in which events are evaluated and how actions are executed\.   
*Required*: No  
*Type*: String  
*Allowed values*: `BATCH | SERIAL`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Key`  <a name="cfn-iotevents-detectormodel-key"></a>
The value used to identify a detector instance\. When a device or system sends input, a new detector instance with a unique key value is created\. AWS IoT Events can continue to route input to its corresponding detector instance based on this identifying information\.   
This parameter uses a JSON\-path expression to select the attribute\-value pair in the message payload that is used for identification\. To route the message to the correct detector instance, the device must send a message payload that contains the same attribute\-value\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `^((`[\w\- ]+`)|([\w\-]+))(\.((`[\w- ]+`)|([\w\-]+)))*$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RoleArn`  <a name="cfn-iotevents-detectormodel-rolearn"></a>
The ARN of the role that grants permission to AWS IoT Events to perform its operations\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-iotevents-detectormodel-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-iotevents-detectormodel-return-values"></a>

### Ref<a name="aws-resource-iotevents-detectormodel-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the detector model\. For example:

`{"Ref": "myDetectorModel"}`

For the AWS IoT Events detector model `myDetectorModel`, `Ref` returns the name of the detector model\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-iotevents-detectormodel--examples"></a>



### Simple Detector Model<a name="aws-resource-iotevents-detectormodel--examples--Simple_Detector_Model"></a>

The following example creates a simple detector model with only one state\.

#### JSON<a name="aws-resource-iotevents-detectormodel--examples--Simple_Detector_Model--json"></a>

```
{
  "Description": "Simple Detector Model Template",
  "Resources": {
    "MyDetectorModel": {
      "Type": "AWS::IoTEvents::DetectorModel",
      "Properties": {
        "DetectorModelName": "myDetectorModel",
        "DetectorModelDescription": "My Detector Model created by CloudFormation",
        "Key": "myKey",
        "RoleArn": { "Fn::GetAtt" : [ "myRole", "Arn" ] },
        "DetectorModelDefinition": {
          "InitialStateName": "myInitialState",
          "States": [
            {
              "StateName": "myInitialState",
              "OnInput": {
                "Events": [
                  {
                    "EventName": "onInputPublishEvent",
                    "Condition": { "Fn::Join" : [ ".", ["$input", {"Ref": "myInput"}, "foo > 1"] ] },
                    "Actions": [
                      {
                        "IotTopicPublish": {
                          "MqttTopic": "myMqttTopic"
                        }
                      }
                    ]
                  }
                ]
              }
            }
          ]
        }
      }
    }
  }
}
```

#### YAML<a name="aws-resource-iotevents-detectormodel--examples--Simple_Detector_Model--yaml"></a>

```
---
Description: "Simple Detector Model Template"
Resources:
  MyDetectorModel:
    Type: "AWS::IoTEvents::DetectorModel"
    Properties:
      DetectorModelName: "myDetectorModel"
      DetectorModelDescription: "My Detector Model created by CloudFormation"
      Key: "myKey"
      RoleArn: !GetAtt myRole.Arn
      DetectorModelDefinition:
        InitialStateName: "myInitialState"
        States:
         - StateName: "myInitialState"
           OnInput:
             Events:
               - EventName: "onInputPublishEvent"
                 Condition: !Join [".", ["$input", {'Ref': myInput}, "foo > 1"]]
                 Actions:
                   - IotTopicPublish:
                       MqttTopic: "myMqttTopic"
```

### Full Detector Model<a name="aws-resource-iotevents-detectormodel--examples--Full_Detector_Model"></a>

The following example creates a more complete example of a detector model with two states\.

#### JSON<a name="aws-resource-iotevents-detectormodel--examples--Full_Detector_Model--json"></a>

```
{
  "Description": "Detector Model Template for CloudFormation",
  "Resources": {
    "MyDetectorModel": {
      "Type": "AWS::IoTEvents::DetectorModel",
      "Properties": {
        "DetectorModelName": "myDetectorModel",
        "DetectorModelDescription": "My Detector Model created by CloudFormation",
        "Key": "myKey",
        "RoleArn": "arn:aws:iam::123456789012:role/myIotEventsRole",
        "DetectorModelDefinition": {
          "InitialStateName": "myInitialState",
          "States": [
            {
              "StateName": "myInitialState",
              "OnEnter": {
                "Events": [
                  {
                    "EventName": "onEnterEvent",
                    "Actions": [
                      {
                        "SetVariable": {
                          "VariableName": "Variable",
                          "Value": "0"
                        }
                      }
                    ]
                  },
                  {
                    "EventName": "onEnter Event 2",
                    "Condition": "true",
                    "Actions": [
                      {
                        "SetTimer": {
                          "TimerName": "myTimer",
                          "Seconds": 60
                        }
                      }
                    ]
                  }
                ]
              },
              "OnInput": {
                "Events": [
                  {
                    "EventName": "onInputEvent",
                    "Condition": { "Fn::Join" : [ ".", ["$input", {"Ref": "myInput"}, "foo > 1"] ] },
                    "Actions": [
                      {
                        "IotTopicPublish": {
                          "MqttTopic": "myMqttTopic"
                        }
                      },
                      {
                        "ResetTimer": {
                          "TimerName": "myTimer"
                        }
                      }
                    ]
                  }
                ],
                "TransitionEvents": [
                  {
                    "EventName": "Transit to other state",
                    "Condition": "true",
                    "Actions": [
                      {
                        "Sns": {
                          "TargetArn": "arn:aws:sns:123456789012:mySnsTopic"
                        }
                      },
                      {
                        "Lambda": {
                          "FunctionArn": "arn:aws:lambda:123456789012:function:myLambdaFunction"
                        }
                      },
                      {
                        "Firehose": {
                          "DeliveryStreamName": "myStreamName",
                          "Separator": ","
                        }
                      },
                      {
                        "Sqs": {
                          "QueueUrl": "myQueueUrl",
                          "UseBase64": true
                        }
                      },
                      {
                        "IotEvents": {
                          "InputName": "myInputName"
                        }
                      }
                    ],
                    "NextState": "myOtherState"
                  }
                ]
              },
              "OnExit": {
                "Events": [
                  {
                    "EventName": "Clear timers",
                    "Condition": "1 == 1",
                    "Actions": [
                      {
                        "ClearTimer": {
                          "TimerName": "myTimer"
                        }
                      }
                    ]
                  }
                ]
              }
            },
            {
              "StateName": "myOtherState",
              "OnEnter": {
                "Events": [
                  {
                    "EventName": "onEnterEvent",
                    "Actions": [
                      {
                        "SetVariable": {
                          "VariableName": "Variable",
                          "Value": "0"
                        }
                      }
                    ]
                  },
                  {
                    "EventName": "onEnter Event 2",
                    "Condition": "true",
                    "Actions": [
                      {
                        "SetTimer": {
                          "TimerName": "myTimer",
                          "Seconds": 60
                        }
                      }
                    ]
                  }
                ]
              },
              "OnExit": {
                "Events": [
                  {
                    "EventName": "Clear timers",
                    "Condition": "1 == 1",
                    "Actions": [
                      {
                        "ClearTimer": {
                          "TimerName": "myTimer"
                        }
                      }
                    ]
                  }
                ]
              }
            }
          ]
        }
      }
    }
  }
}
```

#### YAML<a name="aws-resource-iotevents-detectormodel--examples--Full_Detector_Model--yaml"></a>

```
---
Description: "Detector Model Template for CloudFormation"
Resources:
  MyDetectorModel:
    Type: "AWS::IoTEvents::DetectorModel"
    Properties:
      DetectorModelName: "myDetectorModel"
      DetectorModelDescription: "My Detector Model created by CloudFormation"
      Key: "myKey"
      RoleArn: "arn:aws:iam::123456789012:role/myIotEventsRole"
      DetectorModelDefinition:
        InitialStateName: "myInitialState"
        States:
          - StateName: "myInitialState"
            OnEnter:
              Events:
                - EventName: "onEnterEvent"
                  Actions:
                    - SetVariable:
                        VariableName: "Variable"
                        Value: "0"
                - EventName: "onEnter Event 2"
                  Condition: "true"
                  Actions:
                    - SetTimer:
                        TimerName: "myTimer"
                        Seconds: 60
            OnInput:
              Events:
                - EventName: "onInputEvent"
                  Condition: !Join [".", ["$input", {'Ref': myInput}, "foo > 1"]]
                  Actions:
                    - IotTopicPublish:
                        MqttTopic: "myMqttTopic"
                    - ResetTimer:
                        TimerName: "myTimer"
              TransitionEvents:
                - EventName: "Transit to other state"
                  Condition: "true"
                  Actions:
                    - Sns:
                        TargetArn: "arn:aws:sns:123456789012:mySnsTopic"
                    - Lambda:
                        FunctionArn: "arn:aws:lambda:123456789012:function:myLambdaFunction"
                    - Firehose:
                        DeliveryStreamName: "myStreamName"
                        Separator: ","
                    - Sqs:
                        QueueUrl: "myQueueUrl"
                        UseBase64: true
                    - IotEvents:
                        InputName: "myInputName"
                  NextState: "myOtherState"
            OnExit:
              Events:
                - EventName: "Clear timers"
                  Condition: "1 == 1"
                  Actions:
                    - ClearTimer:
                        TimerName: "myTimer"
          - StateName: "myOtherState"
            OnEnter:
              Events:
                - EventName: "onEnterEvent"
                  Actions:
                    - SetVariable:
                        VariableName: "Variable"
                        Value: "0"
                - EventName: "onEnter Event 2"
                  Condition: "true"
                  Actions:
                    - SetTimer:
                        TimerName: "myTimer"
                        Seconds: 60
            OnExit:
              Events:
                - EventName: "Clear timers"
                  Condition: "1 == 1"
                  Actions:
                    - ClearTimer:
                        TimerName: "myTimer"
```

## See also<a name="aws-resource-iotevents-detectormodel--seealso"></a>
+  [ How to Use AWS IoT Events](https://docs.aws.amazon.com/iotevents/latest/developerguide/how-to-use-iotevents.html) in the *AWS IoT Events Developer Guide*
+  [ CreateDetectorModel](https://docs.aws.amazon.com/iotevents/latest/apireference/API_CreateDetectorModel.html) in the *AWS IoT Events API Reference*