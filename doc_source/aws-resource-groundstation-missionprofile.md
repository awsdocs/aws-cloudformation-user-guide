# AWS::GroundStation::MissionProfile<a name="aws-resource-groundstation-missionprofile"></a>

 Mission profiles specify parameters and provide references to config objects to define how Ground Station lists and executes contacts\. 

## Syntax<a name="aws-resource-groundstation-missionprofile-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-groundstation-missionprofile-syntax.json"></a>

```
{
  "Type" : "AWS::GroundStation::MissionProfile",
  "Properties" : {
      "[ContactPostPassDurationSeconds](#cfn-groundstation-missionprofile-contactpostpassdurationseconds)" : Integer,
      "[ContactPrePassDurationSeconds](#cfn-groundstation-missionprofile-contactprepassdurationseconds)" : Integer,
      "[DataflowEdges](#cfn-groundstation-missionprofile-dataflowedges)" : [ DataflowEdge, ... ],
      "[MinimumViableContactDurationSeconds](#cfn-groundstation-missionprofile-minimumviablecontactdurationseconds)" : Integer,
      "[Name](#cfn-groundstation-missionprofile-name)" : String,
      "[Tags](#cfn-groundstation-missionprofile-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[TrackingConfigArn](#cfn-groundstation-missionprofile-trackingconfigarn)" : String
    }
}
```

### YAML<a name="aws-resource-groundstation-missionprofile-syntax.yaml"></a>

```
Type: AWS::GroundStation::MissionProfile
Properties: 
  [ContactPostPassDurationSeconds](#cfn-groundstation-missionprofile-contactpostpassdurationseconds): Integer
  [ContactPrePassDurationSeconds](#cfn-groundstation-missionprofile-contactprepassdurationseconds): Integer
  [DataflowEdges](#cfn-groundstation-missionprofile-dataflowedges): 
    - DataflowEdge
  [MinimumViableContactDurationSeconds](#cfn-groundstation-missionprofile-minimumviablecontactdurationseconds): Integer
  [Name](#cfn-groundstation-missionprofile-name): String
  [Tags](#cfn-groundstation-missionprofile-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [TrackingConfigArn](#cfn-groundstation-missionprofile-trackingconfigarn): String
```

## Properties<a name="aws-resource-groundstation-missionprofile-properties"></a>

`ContactPostPassDurationSeconds`  <a name="cfn-groundstation-missionprofile-contactpostpassdurationseconds"></a>
 Amount of time in seconds after a contact ends that you’d like to receive a CloudWatch Event indicating the pass has finished\. For more information on CloudWatch Events, see the [What Is CloudWatch Events?](https://docs.aws.amazon.com/AmazonCloudWatch/latest/events/WhatIsCloudWatchEvents.html)   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ContactPrePassDurationSeconds`  <a name="cfn-groundstation-missionprofile-contactprepassdurationseconds"></a>
 Amount of time in seconds prior to contact start that you'd like to receive a CloudWatch Event indicating an upcoming pass\. For more information on CloudWatch Events, see the [What Is CloudWatch Events?](https://docs.aws.amazon.com/AmazonCloudWatch/latest/events/WhatIsCloudWatchEvents.html)   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataflowEdges`  <a name="cfn-groundstation-missionprofile-dataflowedges"></a>
 A list containing lists of config ARNs\. Each list of config ARNs is an edge, with a "from" config and a "to" config\.   
*Required*: Yes  
*Type*: List of [DataflowEdge](aws-properties-groundstation-missionprofile-dataflowedge.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinimumViableContactDurationSeconds`  <a name="cfn-groundstation-missionprofile-minimumviablecontactdurationseconds"></a>
 Minimum length of a contact in seconds that Ground Station will return when listing contacts\. Ground Station will not return contacts shorter than this duration\.   
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-groundstation-missionprofile-name"></a>
 The name of the mission profile\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-groundstation-missionprofile-tags"></a>
 Tags assigned to the mission profile\.   
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TrackingConfigArn`  <a name="cfn-groundstation-missionprofile-trackingconfigarn"></a>
 The ARN of a tracking config objects that defines how to track the satellite through the sky during a contact\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-groundstation-missionprofile-return-values"></a>

### Ref<a name="aws-resource-groundstation-missionprofile-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ARN of the mission profile\. For example: 

 `{ "Ref": "MissionProfile" }` 

 `Ref` returns the ARN of the mission profile\. 

### Fn::GetAtt<a name="aws-resource-groundstation-missionprofile-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-groundstation-missionprofile-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the mission profile, such as `arn:aws:groundstation:us-east-2:1234567890:mission-profile/9940bf3b-d2ba-427e-9906-842b5e5d2296`\. 

`Id`  <a name="Id-fn::getatt"></a>
The ID of the mission profile, such as `9940bf3b-d2ba-427e-9906-842b5e5d2296`\. 

`Region`  <a name="Region-fn::getatt"></a>
 The region of the mission profile\. 

## Examples<a name="aws-resource-groundstation-missionprofile--examples"></a>

### Mission Profile With Downlink And Uplink<a name="aws-resource-groundstation-missionprofile--examples--Mission_Profile_With_Downlink_And_Uplink"></a>

 The following example shows how to create a mission profile that utilizes both downlink and uplink during a contact\. 

 The resulting mission profile will have a name of `My Mission Profile`\. CloudWatch Events will be sent `120` seconds before the contact starts and `180` seconds after the contact completes\. No contacts less than `300` seconds in duration will be returned when listing available contacts with this mission profile selected\. 

 The satellite will be tracked as it moves through the sky using the method specified by the referenced tracking config\. 

 The first dataflow edge in the list shows how to specify dataflow for a downlink contact\. Data is delivered from the antenna to a dataflow endpoint\. More specifically, data is flowed: 
+ From the antenna using the parameters defined in this antenna downlink config:
  +  `arn:aws:groundstation:us-east-2:1234567890:config/antenna-downlink/11111111-1111-1111-1111-111111111111` 
+ To the dataflow endpoint defined in this dataflow endpoint config:
  +  `arn:aws:groundstation:us-east-2:1234567890:config/dataflow-endpoint/22222222-2222-2222-2222-222222222222` 

 The second dataflow edge in the list shows how to specify dataflow for an uplink contact\. Data is delivered from a dataflow endpoint to the antenna for transmission to a satellite\. More specifically, data is flowed: 
+ From the dataflow endpoint defined in this dataflow endpoint config:
  +  `arn:aws:groundstation:us-east-2:1234567890:config/dataflow-endpoint/33333333-3333-3333-3333-333333333333` 
+ To the antenna using the parameters defined in this antenna uplink config:
  +  `arn:aws:groundstation:us-east-2:1234567890:config/antenna-uplink/44444444-4444-4444-4444-444444444444` 

#### JSON<a name="aws-resource-groundstation-missionprofile--examples--Mission_Profile_With_Downlink_And_Uplink--json"></a>

```
{
  "Resources": {
    "MyMissionProfile": {
      "Type": "AWS::GroundStation::MissionProfile",
      "Properties": {
        "Name": "My Mission Profile",
        "ContactPrePassDurationSeconds": 120,
        "ContactPostPassDurationSeconds": 180,
        "MinimumViableContactDurationSeconds": 300,
        "TrackingConfigArn": "arn:aws:groundstation:us-east-2:1234567890:config/tracking/00000000-0000-0000-0000-000000000000",
        "DataflowEdges": [
          {
            "Source": "arn:aws:groundstation:us-east-2:1234567890:config/antenna-downlink/11111111-1111-1111-1111-111111111111",
            "Destination": "arn:aws:groundstation:us-east-2:1234567890:config/dataflow-endpoint/22222222-2222-2222-2222-222222222222"
          },
          {
            "Source": "arn:aws:groundstation:us-east-2:1234567890:config/dataflow-endpoint/33333333-3333-3333-3333-333333333333",
            "Destination": "arn:aws:groundstation:us-east-2:1234567890:config/antenna-uplink/44444444-4444-4444-4444-444444444444"
          }
        ]
      }
    }
  }
}
```

#### YAML<a name="aws-resource-groundstation-missionprofile--examples--Mission_Profile_With_Downlink_And_Uplink--yaml"></a>

```
Resources:
  MyMissionProfile:
    Type: AWS::GroundStation::MissionProfile
    Properties:
      Name: "Mission Profile"
      ContactPrePassDurationSeconds: 120
      ContactPostPassDurationSeconds: 180
      MinimumViableContactDurationSeconds: 300
      TrackingConfigArn: arn:aws:groundstation:us-east-2:1234567890:config/tracking/00000000-0000-0000-0000-000000000000
      DataflowEdges:
        - Source: arn:aws:groundstation:us-east-2:1234567890:config/antenna-downlink/11111111-1111-1111-1111-111111111111
          Destination: arn:aws:groundstation:us-east-2:1234567890:config/dataflow-endpoint/22222222-2222-2222-2222-222222222222
        - Source: arn:aws:groundstation:us-east-2:1234567890:config/dataflow-endpoint/33333333-3333-3333-3333-333333333333
          Destination: arn:aws:groundstation:us-east-2:1234567890:config/antenna-uplink/44444444-4444-4444-4444-444444444444
```