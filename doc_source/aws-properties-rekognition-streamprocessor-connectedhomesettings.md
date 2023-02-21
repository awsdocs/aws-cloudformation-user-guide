# AWS::Rekognition::StreamProcessor ConnectedHomeSettings<a name="aws-properties-rekognition-streamprocessor-connectedhomesettings"></a>

Connected home settings to use on a streaming video\. Defining the settings is required in the request parameter for `CreateStreamProcessor`\. Including this setting in the CreateStreamProcessor request lets you use the stream processor for connected home features\. You can then select what you want the stream processor to detect, such as people or pets\. 

When the stream processor has started, one notification is sent for each object class specified\. For example, if packages and pets are selected, one SNS notification is published the first time a package is detected and one SNS notification is published the first time a pet is detected\. An end\-of\-session summary is also published\. For more information, see the ConnectedHome section of [StreamProcessorSettings](https://docs.aws.amazon.com/rekognition/latest/APIReference/API_StreamProcessorSettings)\. 

## Syntax<a name="aws-properties-rekognition-streamprocessor-connectedhomesettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-rekognition-streamprocessor-connectedhomesettings-syntax.json"></a>

```
{
  "[Labels](#cfn-rekognition-streamprocessor-connectedhomesettings-labels)" : [ String, ... ],
  "[MinConfidence](#cfn-rekognition-streamprocessor-connectedhomesettings-minconfidence)" : Double
}
```

### YAML<a name="aws-properties-rekognition-streamprocessor-connectedhomesettings-syntax.yaml"></a>

```
  [Labels](#cfn-rekognition-streamprocessor-connectedhomesettings-labels): 
    - String
  [MinConfidence](#cfn-rekognition-streamprocessor-connectedhomesettings-minconfidence): Double
```

## Properties<a name="aws-properties-rekognition-streamprocessor-connectedhomesettings-properties"></a>

`Labels`  <a name="cfn-rekognition-streamprocessor-connectedhomesettings-labels"></a>
Specifies what you want to detect in the video, such as people, packages, or pets\. The current valid labels you can include in this list are: "PERSON", "PET", "PACKAGE", and "ALL"\.   
*Required*: Yes  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MinConfidence`  <a name="cfn-rekognition-streamprocessor-connectedhomesettings-minconfidence"></a>
The minimum confidence required to label an object in the video\.   
*Required*: No  
*Type*: Double  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)