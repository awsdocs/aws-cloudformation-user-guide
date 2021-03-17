# AWS::IoT::SecurityProfile<a name="aws-resource-iot-securityprofile"></a>

Use the `AWS::IoT::SecurityProfile` resource to create a Device Defender security profile\. For API reference, see [CreateSecurityProfile](https://docs.aws.amazon.com/iot/latest/apireference/API_CreateSecurityProfile.html) and for general information, see [Detect](https://docs.aws.amazon.com/iot/latest/developerguide/device-defender-detect.html)\.

## Syntax<a name="aws-resource-iot-securityprofile-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iot-securityprofile-syntax.json"></a>

```
{
  "Type" : "AWS::IoT::SecurityProfile",
  "Properties" : {
      "[AdditionalMetricsToRetainV2](#cfn-iot-securityprofile-additionalmetricstoretainv2)" : [ MetricToRetain, ... ],
      "[AlertTargets](#cfn-iot-securityprofile-alerttargets)" : {Key : Value, ...},
      "[Behaviors](#cfn-iot-securityprofile-behaviors)" : [ Behavior, ... ],
      "[SecurityProfileDescription](#cfn-iot-securityprofile-securityprofiledescription)" : String,
      "[SecurityProfileName](#cfn-iot-securityprofile-securityprofilename)" : String,
      "[Tags](#cfn-iot-securityprofile-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[TargetArns](#cfn-iot-securityprofile-targetarns)" : [ String, ... ]
    }
}
```

### YAML<a name="aws-resource-iot-securityprofile-syntax.yaml"></a>

```
Type: AWS::IoT::SecurityProfile
Properties: 
  [AdditionalMetricsToRetainV2](#cfn-iot-securityprofile-additionalmetricstoretainv2): 
    - MetricToRetain
  [AlertTargets](#cfn-iot-securityprofile-alerttargets): 
    Key : Value
  [Behaviors](#cfn-iot-securityprofile-behaviors): 
    - Behavior
  [SecurityProfileDescription](#cfn-iot-securityprofile-securityprofiledescription): String
  [SecurityProfileName](#cfn-iot-securityprofile-securityprofilename): String
  [Tags](#cfn-iot-securityprofile-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [TargetArns](#cfn-iot-securityprofile-targetarns): 
    - String
```

## Properties<a name="aws-resource-iot-securityprofile-properties"></a>

`AdditionalMetricsToRetainV2`  <a name="cfn-iot-securityprofile-additionalmetricstoretainv2"></a>
A list of metrics whose data is retained \(stored\)\. By default, data is retained for any metric used in the profile's `behaviors`, but it's also retained for any metric specified here\. Can be used with custom metrics; can't be used with dimensions\.  
*Required*: No  
*Type*: List of [MetricToRetain](aws-properties-iot-securityprofile-metrictoretain.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AlertTargets`  <a name="cfn-iot-securityprofile-alerttargets"></a>
Specifies the destinations to which alerts are sent\. \(Alerts are always sent to the console\.\) Alerts are generated when a device \(thing\) violates a behavior\.  
*Required*: No  
*Type*: Map of [AlertTarget](aws-properties-iot-securityprofile-alerttarget.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Behaviors`  <a name="cfn-iot-securityprofile-behaviors"></a>
Specifies the behaviors that, when violated by a device \(thing\), cause an alert\.  
*Required*: No  
*Type*: List of [Behavior](aws-properties-iot-securityprofile-behavior.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityProfileDescription`  <a name="cfn-iot-securityprofile-securityprofiledescription"></a>
A description of the security profile\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityProfileName`  <a name="cfn-iot-securityprofile-securityprofilename"></a>
The name you gave to the security profile\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-iot-securityprofile-tags"></a>
Metadata that can be used to manage the security profile\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetArns`  <a name="cfn-iot-securityprofile-targetarns"></a>
The ARN of the target \(thing group\) to which the security profile is attached\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-iot-securityprofile-return-values"></a>

### Ref<a name="aws-resource-iot-securityprofile-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the security profile name\.

### Fn::GetAtt<a name="aws-resource-iot-securityprofile-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-iot-securityprofile-return-values-fn--getatt-fn--getatt"></a>

`SecurityProfileArn`  <a name="SecurityProfileArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the security profile\.

## Examples<a name="aws-resource-iot-securityprofile--examples"></a>



### <a name="aws-resource-iot-securityprofile--examples--"></a>



#### JSON<a name="aws-resource-iot-securityprofile--examples----json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Description": "AWS IoT SecurityProfile Sample Template",
  "Resources": {
    "MySecurityProfile": {
      "Type": "AWS::IoT::SecurityProfile",
      "Properties": {
        "AdditionalMetricsToRetainV2": [
          {
            "Metric": "aws:num-messages-received"
          },
          {
            "Metric": "aws:num-disconnects"
          }
        ],
        "AlertTargets": {
          "SNS": {
            "AlertTargetArn": "!Ref SNSTopicForAlertTarget",
            "RoleArn": "!GetAtt AlertTargetSNSPermissionsRole.Arn"
          }
        },
        "Behaviors": [
          {
            "Name": "MaxMessageSize",
            "Metric": "aws:message-byte-size",
            "Criteria": {
              "ConsecutiveDatapointsToAlarm": 1,
              "ConsecutiveDatapointsToClear": 1,
              "Value": {
                "Count": 5
              }
            }
          },
          {
            "Name": "OutboundMessageCount",
            "Metric": "aws:num-messages-sent",
            "Criteria": {
              "DurationSeconds": 300,
              "ComparisonOperator": "less-than-equals",
              "Value": {
                "count": 50
              }
            }
          },
          {
            "Name": "AuthFailuresStatThreshold",
            "Metric": "aws:num-authorization-failures",
            "Criteria": {
              "ComparisonOperator": "less-than-equals",
              "DurationSeconds": 300,
              "StatisticalThreshold": {
                "Statistic": "p90"
              }
            }
          }
        ],
        "SecurityProfileDescription": "Contains expected behaviors for connected devices",
        "SecurityProfileName": "ProfileForConnectedDevices",
        "Tags": [
          {
            "Key": "Application"
            "Value": "SmartHome"
          }
        ],
        "TargetArns": [
          "arn:aws:iot:us-east-1:123456789012:all/things"
        ]
      }
    }
  }
}
```

#### YAML<a name="aws-resource-iot-securityprofile--examples----yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Description: AWS IoT SecurityProfile Sample Template
Resources:
  MySecurityProfile:
    Type: AWS::IoT::SecurityProfile
    Properties:
      AdditionalMetricsToRetainV2:
      - Metric: aws:num-messages-received
      - Metric: aws:num-disconnects
      AlertTargets:
        SNS:
          AlertTargetArn: !Ref 
            "SnsTopicForAlertTarget"
          RoleArn: !GetAtt 
            "AlertTargetSNSPermissionsRole.Arn"
      Behaviors:
      - Name: MaxMessageSize
        Metric: aws:message-byte-size
        Criteria:
          ConsecutiveDatapointsToAlarm: 1
          ConsecutiveDatapointsToClear: 1
          Value:
            Count: 5
      - Name: OutboundMessageCount
        Metric: aws:num-messages-sent
        Criteria:
          DurationSeconds: 300
          ComparisonOperator: less-than-equals
          Value:
            count: 50
      - Name: AuthFailuresStatThreshold
        Metric: aws:num-authorization-failures
        Criteria:
          ComparisonOperator: less-than-equals
          DurationSeconds: 300
          StatisticalThreshold:
            Statistic: p90
      SecurityProfileDescription: Contains expected behaviors for connected devices
      SecurityProfileName: ProfileForConnectedDevices
      Tags:
      - Key: "tagKey"
      - Value: "tagValue"
      TargetArns:
      - "arn:aws:iot:us-east-1:123456789012:all/things"
```