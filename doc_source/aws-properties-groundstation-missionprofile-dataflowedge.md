# AWS::GroundStation::MissionProfile DataflowEdge<a name="aws-properties-groundstation-missionprofile-dataflowedge"></a>

 A dataflow edge defines from where and to where data will flow during a contact\. 

## Syntax<a name="aws-properties-groundstation-missionprofile-dataflowedge-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-groundstation-missionprofile-dataflowedge-syntax.json"></a>

```
{
  "[Destination](#cfn-groundstation-missionprofile-dataflowedge-destination)" : String,
  "[Source](#cfn-groundstation-missionprofile-dataflowedge-source)" : String
}
```

### YAML<a name="aws-properties-groundstation-missionprofile-dataflowedge-syntax.yaml"></a>

```
  [Destination](#cfn-groundstation-missionprofile-dataflowedge-destination): String
  [Source](#cfn-groundstation-missionprofile-dataflowedge-source): String
```

## Properties<a name="aws-properties-groundstation-missionprofile-dataflowedge-properties"></a>

`Destination`  <a name="cfn-groundstation-missionprofile-dataflowedge-destination"></a>
 The ARN of the destination for this dataflow edge\. For example, specify the ARN of a dataflow endpoint config for a downlink edge or an antenna uplink config for an uplink edge\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Source`  <a name="cfn-groundstation-missionprofile-dataflowedge-source"></a>
 The ARN of the source for this dataflow edge\. For example, specify the ARN of an antenna downlink config for a downlink edge or a dataflow endpoint config for an uplink edge\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-groundstation-missionprofile-dataflowedge--examples"></a>

### Downlink Dataflow Edge<a name="aws-properties-groundstation-missionprofile-dataflowedge--examples--Downlink_Dataflow_Edge"></a>

 The dataflow edge below shows how to specify dataflow for a downlink contact\. Data is delivered from the antenna to a dataflow endpoint\. More specifically, data is flowed: 
+ From the antenna using the parameters defined in this antenna downlink config:
  +  `arn:aws:groundstation:us-east-2:1234567890:config/antenna-downlink/11111111-1111-1111-1111-111111111111` 
+ To the dataflow endpoint defined in this dataflow endpoint config:
  +  `arn:aws:groundstation:us-east-2:1234567890:config/dataflow-endpoint/22222222-2222-2222-2222-222222222222` 

#### JSON<a name="aws-properties-groundstation-missionprofile-dataflowedge--examples--Downlink_Dataflow_Edge--json"></a>

```
"DataflowEdges": [
  {
    "Source": "arn:aws:groundstation:us-east-2:1234567890:config/antenna-downlink/11111111-1111-1111-1111-111111111111",
    "Destination": "arn:aws:groundstation:us-east-2:1234567890:config/dataflow-endpoint/22222222-2222-2222-2222-222222222222"
  }
]
```

#### YAML<a name="aws-properties-groundstation-missionprofile-dataflowedge--examples--Downlink_Dataflow_Edge--yaml"></a>

```
DataflowEdges:
  - Source: arn:aws:groundstation:us-east-2:1234567890:config/antenna-downlink/11111111-1111-1111-1111-111111111111
    Destination: arn:aws:groundstation:us-east-2:1234567890:config/dataflow-endpoint/22222222-2222-2222-2222-222222222222
```

### Uplink Dataflow Edge<a name="aws-properties-groundstation-missionprofile-dataflowedge--examples--Uplink_Dataflow_Edge"></a>

 The dataflow edge below shows how to specify dataflow for an uplink contact\. Data is delivered from a dataflow endpoint to the antenna for transmission to a satellite\. More specifically, data is flowed: 
+ From the dataflow endpoint defined in this dataflow endpoint config:
  +  `arn:aws:groundstation:us-east-2:1234567890:config/dataflow-endpoint/33333333-3333-3333-3333-333333333333` 
+ To the antenna using the parameters defined in this antenna uplink config:
  +  `arn:aws:groundstation:us-east-2:1234567890:config/antenna-uplink/44444444-4444-4444-4444-444444444444` 

#### JSON<a name="aws-properties-groundstation-missionprofile-dataflowedge--examples--Uplink_Dataflow_Edge--json"></a>

```
"DataflowEdges": [
  [
    "arn:aws:groundstation:us-east-2:1234567890:config/dataflow-endpoint/33333333-3333-3333-3333-333333333333",
    "arn:aws:groundstation:us-east-2:1234567890:config/antenna-uplink/44444444-4444-4444-4444-444444444444"
  ]
]
```

#### YAML<a name="aws-properties-groundstation-missionprofile-dataflowedge--examples--Uplink_Dataflow_Edge--yaml"></a>

```
DataflowEdges:
  - - arn:aws:groundstation:us-east-2:1234567890:config/dataflow-endpoint/33333333-3333-3333-3333-333333333333
    - arn:aws:groundstation:us-east-2:1234567890:config/antenna-uplink/44444444-4444-4444-4444-444444444444
```