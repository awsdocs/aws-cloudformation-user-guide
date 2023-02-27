# AWS::Pipes::Pipe PipeTargetEventBridgeEventBusParameters<a name="aws-properties-pipes-pipe-pipetargeteventbridgeeventbusparameters"></a>

The parameters for using an EventBridge event bus as a target\.

## Syntax<a name="aws-properties-pipes-pipe-pipetargeteventbridgeeventbusparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pipes-pipe-pipetargeteventbridgeeventbusparameters-syntax.json"></a>

```
{
  "[DetailType](#cfn-pipes-pipe-pipetargeteventbridgeeventbusparameters-detailtype)" : String,
  "[EndpointId](#cfn-pipes-pipe-pipetargeteventbridgeeventbusparameters-endpointid)" : String,
  "[Resources](#cfn-pipes-pipe-pipetargeteventbridgeeventbusparameters-resources)" : [ String, ... ],
  "[Source](#cfn-pipes-pipe-pipetargeteventbridgeeventbusparameters-source)" : String,
  "[Time](#cfn-pipes-pipe-pipetargeteventbridgeeventbusparameters-time)" : String
}
```

### YAML<a name="aws-properties-pipes-pipe-pipetargeteventbridgeeventbusparameters-syntax.yaml"></a>

```
  [DetailType](#cfn-pipes-pipe-pipetargeteventbridgeeventbusparameters-detailtype): String
  [EndpointId](#cfn-pipes-pipe-pipetargeteventbridgeeventbusparameters-endpointid): String
  [Resources](#cfn-pipes-pipe-pipetargeteventbridgeeventbusparameters-resources): 
    - String
  [Source](#cfn-pipes-pipe-pipetargeteventbridgeeventbusparameters-source): String
  [Time](#cfn-pipes-pipe-pipetargeteventbridgeeventbusparameters-time): String
```

## Properties<a name="aws-properties-pipes-pipe-pipetargeteventbridgeeventbusparameters-properties"></a>

`DetailType`  <a name="cfn-pipes-pipe-pipetargeteventbridgeeventbusparameters-detailtype"></a>
A free\-form string, with a maximum of 128 characters, used to decide what fields to expect in the event detail\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EndpointId`  <a name="cfn-pipes-pipe-pipetargeteventbridgeeventbusparameters-endpointid"></a>
The URL subdomain of the endpoint\. For example, if the URL for Endpoint is https://abcde\.veo\.endpoints\.event\.amazonaws\.com, then the EndpointId is `abcde.veo`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Resources`  <a name="cfn-pipes-pipe-pipetargeteventbridgeeventbusparameters-resources"></a>
AWS resources, identified by Amazon Resource Name \(ARN\), which the event primarily concerns\. Any number, including zero, may be present\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Source`  <a name="cfn-pipes-pipe-pipetargeteventbridgeeventbusparameters-source"></a>
The source of the event\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Time`  <a name="cfn-pipes-pipe-pipetargeteventbridgeeventbusparameters-time"></a>
The time stamp of the event, per [RFC3339](https://www.rfc-editor.org/rfc/rfc3339.txt)\. If no time stamp is provided, the time stamp of the [PutEvents](https://docs.aws.amazon.com/eventbridge/latest/APIReference/API_PutEvents.html) call is used\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)