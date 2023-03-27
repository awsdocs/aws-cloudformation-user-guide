# AWS::Rekognition::StreamProcessor<a name="aws-resource-rekognition-streamprocessor"></a>

The `AWS::Rekognition::StreamProcessor` type creates a stream processor used to detect and recognize faces or to detect connected home labels in a streaming video\. Amazon Rekognition Video is a consumer of live video from Amazon Kinesis Video Streams\. There are two different settings for stream processors in Amazon Rekognition, one for detecting faces and one for connected home features\. 

If you are creating a stream processor for detecting faces, you provide a Kinesis video stream \(input\) and a Kinesis data stream \(output\)\. You also specify the face recognition criteria in FaceSearchSettings\. For example, the collection containing faces that you want to recognize\. 

If you are creating a stream processor for detection of connected home labels, you provide a Kinesis video stream for input, and for output an Amazon S3 bucket and an Amazon SNS topic\. You can also provide a KMS key ID to encrypt the data sent to your Amazon S3 bucket\. You specify what you want to detect in ConnectedHomeSettings, such as people, packages, and pets\. 

You can also specify where in the frame you want Amazon Rekognition to monitor with BoundingBoxRegionsOfInterest and PolygonRegionsOfInterest\. The Name is used to manage the stream processor and it is the identifier for the stream processor\. The `AWS::Rekognition::StreamProcessor` resource creates a stream processor in the same Region where you create the Amazon CloudFormation stack\. 

For more information, see [CreateStreamProcessor](https://docs.aws.amazon.com/rekognition/latest/APIReference/API_CreateStreamProcessor)\. 

## Syntax<a name="aws-resource-rekognition-streamprocessor-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-rekognition-streamprocessor-syntax.json"></a>

```
{
  "Type" : "AWS::Rekognition::StreamProcessor",
  "Properties" : {
      "[BoundingBoxRegionsOfInterest](#cfn-rekognition-streamprocessor-boundingboxregionsofinterest)" : [ BoundingBox, ... ],
      "[ConnectedHomeSettings](#cfn-rekognition-streamprocessor-connectedhomesettings)" : ConnectedHomeSettings,
      "[DataSharingPreference](#cfn-rekognition-streamprocessor-datasharingpreference)" : DataSharingPreference,
      "[FaceSearchSettings](#cfn-rekognition-streamprocessor-facesearchsettings)" : FaceSearchSettings,
      "[KinesisDataStream](#cfn-rekognition-streamprocessor-kinesisdatastream)" : KinesisDataStream,
      "[KinesisVideoStream](#cfn-rekognition-streamprocessor-kinesisvideostream)" : KinesisVideoStream,
      "[KmsKeyId](#cfn-rekognition-streamprocessor-kmskeyid)" : String,
      "[Name](#cfn-rekognition-streamprocessor-name)" : String,
      "[NotificationChannel](#cfn-rekognition-streamprocessor-notificationchannel)" : NotificationChannel,
      "[PolygonRegionsOfInterest](#cfn-rekognition-streamprocessor-polygonregionsofinterest)" : Json,
      "[RoleArn](#cfn-rekognition-streamprocessor-rolearn)" : String,
      "[S3Destination](#cfn-rekognition-streamprocessor-s3destination)" : S3Destination,
      "[Tags](#cfn-rekognition-streamprocessor-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-rekognition-streamprocessor-syntax.yaml"></a>

```
Type: AWS::Rekognition::StreamProcessor
Properties: 
  [BoundingBoxRegionsOfInterest](#cfn-rekognition-streamprocessor-boundingboxregionsofinterest): 
    - BoundingBox
  [ConnectedHomeSettings](#cfn-rekognition-streamprocessor-connectedhomesettings): 
    ConnectedHomeSettings
  [DataSharingPreference](#cfn-rekognition-streamprocessor-datasharingpreference): 
    DataSharingPreference
  [FaceSearchSettings](#cfn-rekognition-streamprocessor-facesearchsettings): 
    FaceSearchSettings
  [KinesisDataStream](#cfn-rekognition-streamprocessor-kinesisdatastream): 
    KinesisDataStream
  [KinesisVideoStream](#cfn-rekognition-streamprocessor-kinesisvideostream): 
    KinesisVideoStream
  [KmsKeyId](#cfn-rekognition-streamprocessor-kmskeyid): String
  [Name](#cfn-rekognition-streamprocessor-name): String
  [NotificationChannel](#cfn-rekognition-streamprocessor-notificationchannel): 
    NotificationChannel
  [PolygonRegionsOfInterest](#cfn-rekognition-streamprocessor-polygonregionsofinterest): Json
  [RoleArn](#cfn-rekognition-streamprocessor-rolearn): String
  [S3Destination](#cfn-rekognition-streamprocessor-s3destination): 
    S3Destination
  [Tags](#cfn-rekognition-streamprocessor-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-rekognition-streamprocessor-properties"></a>

`BoundingBoxRegionsOfInterest`  <a name="cfn-rekognition-streamprocessor-boundingboxregionsofinterest"></a>
List of BoundingBox objects, each of which denotes a region of interest on screen\. For more information, see the BoundingBox field of [RegionOfInterest](https://docs.aws.amazon.com/rekognition/latest/APIReference/API_RegionOfInterest)\.   
*Required*: No  
*Type*: List of [BoundingBox](aws-properties-rekognition-streamprocessor-boundingbox.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ConnectedHomeSettings`  <a name="cfn-rekognition-streamprocessor-connectedhomesettings"></a>
Connected home settings to use on a streaming video\. You can use a stream processor for connected home features and select what you want the stream processor to detect, such as people or pets\. When the stream processor has started, one notification is sent for each object class specified\. For more information, see the ConnectedHome section of [StreamProcessorSettings](https://docs.aws.amazon.com/rekognition/latest/APIReference/API_StreamProcessorSettings)\.   
*Required*: No  
*Type*: [ConnectedHomeSettings](aws-properties-rekognition-streamprocessor-connectedhomesettings.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DataSharingPreference`  <a name="cfn-rekognition-streamprocessor-datasharingpreference"></a>
Allows you to opt in or opt out to share data with Rekognition to improve model performance\. You can choose this option at the account level or on a per\-stream basis\. Note that if you opt out at the account level this setting is ignored on individual streams\. For more information, see [StreamProcessorDataSharingPreference](https://docs.aws.amazon.com/rekognition/latest/APIReference/API_StreamProcessorDataSharingPreference)\.   
*Required*: No  
*Type*: [DataSharingPreference](aws-properties-rekognition-streamprocessor-datasharingpreference.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FaceSearchSettings`  <a name="cfn-rekognition-streamprocessor-facesearchsettings"></a>
The input parameters used to recognize faces in a streaming video analyzed by an Amazon Rekognition stream processor\. For more information regarding the contents of the parameters, see [FaceSearchSettings](https://docs.aws.amazon.com/rekognition/latest/APIReference/API_FaceSearchSettings)\.   
*Required*: No  
*Type*: [FaceSearchSettings](aws-properties-rekognition-streamprocessor-facesearchsettings.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KinesisDataStream`  <a name="cfn-rekognition-streamprocessor-kinesisdatastream"></a>
Amazon Rekognition's Video Stream Processor takes a Kinesis video stream as input\. This is the Amazon Kinesis Data Streams instance to which the Amazon Rekognition stream processor streams the analysis results\. This must be created within the constraints specified at [KinesisDataStream](https://docs.aws.amazon.com/rekognition/latest/APIReference/API_KinesisDataStream)\.  
*Required*: No  
*Type*: [KinesisDataStream](aws-properties-rekognition-streamprocessor-kinesisdatastream.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KinesisVideoStream`  <a name="cfn-rekognition-streamprocessor-kinesisvideostream"></a>
The Kinesis video stream that provides the source of the streaming video for an Amazon Rekognition Video stream processor\. For more information, see [KinesisVideoStream](https://docs.aws.amazon.com/rekognition/latest/APIReference/API_KinesisVideoStream)\.  
*Required*: Yes  
*Type*: [KinesisVideoStream](aws-properties-rekognition-streamprocessor-kinesisvideostream.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KmsKeyId`  <a name="cfn-rekognition-streamprocessor-kmskeyid"></a>
 The identifier for your Amazon Key Management Service key \(Amazon KMS key\)\. Optional parameter for connected home stream processors used to encrypt results and data published to your Amazon S3 bucket\. For more information, see the KMSKeyId section of [CreateStreamProcessor](https://docs.aws.amazon.com/rekognition/latest/APIReference/API_CreateStreamProcessor)\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-rekognition-streamprocessor-name"></a>
 The Name attribute specifies the name of the stream processor and it must be within the constraints described in the Name section of [StreamProcessor](https://docs.aws.amazon.com/rekognition/latest/APIReference/API_StreamProcessor)\. If you don't specify a name, Amazon CloudFormation generates a unique ID and uses that ID for the stream processor name\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[a-zA-Z0-9_.\-]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`NotificationChannel`  <a name="cfn-rekognition-streamprocessor-notificationchannel"></a>
 The Amazon Simple Notification Service topic to which Amazon Rekognition publishes the object detection results and completion status of a video analysis operation\. Amazon Rekognition publishes a notification the first time an object of interest or a person is detected in the video stream\. Amazon Rekognition also publishes an end\-of\-session notification with a summary when the stream processing session is complete\. For more information, see [StreamProcessorNotificationChannel](https://docs.aws.amazon.com/rekognition/latest/APIReference/API_StreamProcessorNotificationChannel)\.  
*Required*: No  
*Type*: [NotificationChannel](aws-properties-rekognition-streamprocessor-notificationchannel.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PolygonRegionsOfInterest`  <a name="cfn-rekognition-streamprocessor-polygonregionsofinterest"></a>
A set of ordered lists of [Point](https://docs.aws.amazon.com/rekognition/latest/APIReference/API_Point) objects\. Each entry of the set contains a polygon denoting a region of interest on the screen\. Each polygon is an ordered list of [Point](https://docs.aws.amazon.com/rekognition/latest/APIReference/API_Point) objects\. For more information, see the Polygon field of [RegionOfInterest](https://docs.aws.amazon.com/rekognition/latest/APIReference/API_RegionOfInterest)\.  
*Required*: No  
*Type*: Json  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RoleArn`  <a name="cfn-rekognition-streamprocessor-rolearn"></a>
The ARN of the IAM role that allows access to the stream processor\. The IAM role provides Rekognition read permissions to the Kinesis stream\. It also provides write permissions to an Amazon S3 bucket and Amazon Simple Notification Service topic for a connected home stream processor\. This is required for both face search and connected home stream processors\. For information about constraints, see the RoleArn section of [CreateStreamProcessor](https://docs.aws.amazon.com/rekognition/latest/APIReference/API_CreateStreamProcessor)\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`S3Destination`  <a name="cfn-rekognition-streamprocessor-s3destination"></a>
The Amazon S3 bucket location to which Amazon Rekognition publishes the detailed inference results of a video analysis operation\. For more information, see the S3Destination section of [StreamProcessorOutput](https://docs.aws.amazon.com/rekognition/latest/APIReference/API_StreamProcessorOutput)\.   
*Required*: No  
*Type*: [S3Destination](aws-properties-rekognition-streamprocessor-s3destination.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-rekognition-streamprocessor-tags"></a>
A set of tags \(key\-value pairs\) that you want to attach to the stream processor\. For more information, see the Tags section of [CreateStreamProcessor](https://docs.aws.amazon.com/rekognition/latest/APIReference/API_CreateStreamProcessor)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-rekognition-streamprocessor-return-values"></a>

### Ref<a name="aws-resource-rekognition-streamprocessor-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the stream processor\. For example: 

 `{ "Ref": "MyStreamProcessor" }` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-rekognition-streamprocessor-return-values-fn--getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. For more information about using `Fn::GetAtt`, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\. 

#### <a name="aws-resource-rekognition-streamprocessor-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
 Amazon Resource Name for the newly created stream processor\. 

`Status`  <a name="Status-fn::getatt"></a>
 Current status of the Amazon Rekognition stream processor\. 

`StatusMessage`  <a name="StatusMessage-fn::getatt"></a>
 Detailed status message about the stream processor\. 

## Examples<a name="aws-resource-rekognition-streamprocessor--examples"></a>

### StreamProcessor configured to recognize faces given an input Rekognition Collection<a name="aws-resource-rekognition-streamprocessor--examples--StreamProcessor_configured_to_recognize_faces_given_an_input_Rekognition_Collection"></a>

This template creates a stream processor configured to recognize faces defined in the collection with Collection ID `ExampleCollection`\. It outputs the results to the configured Kinesis data stream\.

#### JSON<a name="aws-resource-rekognition-streamprocessor--examples--StreamProcessor_configured_to_recognize_faces_given_an_input_Rekognition_Collection--json"></a>

```
{
    "ExampleStreamProcessor": {
        "Type": "AWS::Rekognition::StreamProcessor",
        "Properties": {
            "RoleArn": "arn:aws:iam::123456789012:role/Admin",
            "KinesisVideoStream": {
                "Arn": "arn:aws:kinesisvideo:us-east-1:123456789012:stream/my-stream/0123456789012"
            },
            "FaceSearchSettings": {
                "CollectionId": {
                    "Ref": "ExampleCollection"
                },
                "FaceMatchThreshold": 90
            },
            "KinesisDataStream": {
                "Arn": "arn:aws:kinesis:us-east-1:123456789012:stream/my-stream"
            },
            "Tags": [
                {
                    "Key": "Key1",
                    "Value": "Value1"
                },
                {
                    "Key": "Key2",
                    "Value": "Value2"
                }
            ]
        }
    }
}
```

#### YAML<a name="aws-resource-rekognition-streamprocessor--examples--StreamProcessor_configured_to_recognize_faces_given_an_input_Rekognition_Collection--yaml"></a>

```
ExampleStreamProcessor:
    Type: AWS::Rekognition::StreamProcessor
    Properties:
      RoleArn: 'arn:aws:iam::123456789012:role/RoleForRekognition'
      KinesisVideoStream:
        Arn: 'arn:aws:kinesisvideo:us-east-1:123456789012:stream/my-stream/0123456789012'
      FaceSearchSettings:
        CollectionId: 'MyCollection'
        FaceMatchThreshold: 90
      KinesisDataStream:
        Arn: 'arn:aws:kinesis:us-east-1:123456789012:stream/my-stream'
      Tags:
        - Key: 'Key1'
          Value: 'Value1'
        - Key: 'Key2'
          Value: 'Value2'
```

### StreamProcessor to detect ConnectedHome labels without any specific regions of interest configured<a name="aws-resource-rekognition-streamprocessor--examples--StreamProcessor_to_detect_ConnectedHome_labels_without_any_specific_regions_of_interest_configured"></a>

This template creates a stream processor that is configured to detect all supported labels\. Note that the template doesn’t configure any specific regions of interest using `BoundingBoxRegionsOfInterest` and/or `PolygonRegionsOfInterest`, hence Rekognition detects and outputs labels of interest from the entire frame\.

#### JSON<a name="aws-resource-rekognition-streamprocessor--examples--StreamProcessor_to_detect_ConnectedHome_labels_without_any_specific_regions_of_interest_configured--json"></a>

```
{
    "ExampleStreamProcessor": {
        "Type": "AWS::Rekognition::StreamProcessor",
        "Properties": {
            "RoleArn": "arn:aws:iam::123456789012:role/RoleForRekognition",
            "KinesisVideoStream": {
                "Arn": "arn:aws:kinesisvideo:us-east-1:123456789012:stream/my-stream/0123456789012"
            },
            "ConnectedHomeSettings": {
                "Labels": [
                    "ALL"
                ]
            },
            "S3Destination": {
                "BucketName": "MyS3Bucket"
            },
            "NotificationChannel": {
                "Arn": "arn:aws:sns:us-east-1:123456789012:mystack-mytopic-ABCDEFGHIJKL"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-rekognition-streamprocessor--examples--StreamProcessor_to_detect_ConnectedHome_labels_without_any_specific_regions_of_interest_configured--yaml"></a>

```
ExampleStreamProcessor:
    Type: AWS::Rekognition::StreamProcessor
    Properties:
      RoleArn: 'arn:aws:iam::123456789012:role/RoleForRekognition'
      KinesisVideoStream:
        Arn: 'arn:aws:kinesisvideo:us-east-1:123456789012:stream/my-stream/0123456789012'
      ConnectedHomeSettings:
        Labels:
          - 'ALL'
      S3Destination:
        BucketName: 'MyS3Bucket'
      NotificationChannel:
        Arn: 'arn:aws:sns:us-east-1:123456789012:mystack-mytopic-ABCDEFGHIJKL'
```

### StreamProcessor to detect ConnectedHome labels with specific bounding\-box based regions of interest and polygon based regions of interest and polygons configured<a name="aws-resource-rekognition-streamprocessor--examples--StreamProcessor_to_detect_ConnectedHome_labels_with_specific_bounding-box_based_regions_of_interest_and_polygon_based_regions_of_interest_and_polygons_configured"></a>

This template creates a stream processor that is configured to detect PERSON and PACKAGE\. The template configures specific regions of interest using `BoundingBoxRegionsOfInterest` and `PolygonRegionsOfInterest`, hence Rekognition outputs labels of interest detected within those defined bounding boxes and polygons\. The template also specifies the optional KMS key ID which Rekognition uses to encrypt results while publishing data to the Amazon S3 bucket\.

#### JSON<a name="aws-resource-rekognition-streamprocessor--examples--StreamProcessor_to_detect_ConnectedHome_labels_with_specific_bounding-box_based_regions_of_interest_and_polygon_based_regions_of_interest_and_polygons_configured--json"></a>

```
{
    "ExampleStreamProcessor": {
        "Type": "AWS::Rekognition::StreamProcessor",
        "Properties": {
            "RoleArn": "arn:aws:iam::123456789012:role/RoleForRekognition",
            "KmsKeyId": "1234abcd-12ab-34cd-56ef-1234567890ab",
            "KinesisVideoStream": {
                "Arn": "arn:aws:kinesisvideo:us-east-1:123456789012:stream/my-stream/0123456789012"
            },
            "ConnectedHomeSettings": {
                "Labels": [
                    "PERSON",
                    "PACKAGE"
                ],
                "MinConfidence": 60
            },
            "S3Destination": {
                "BucketName": "MyS3Bucket",
                "ObjectKeyPrefix": "/my/prefix/"
            },
            "NotificationChannel": {
                "Arn": "arn:aws:sns:us-east-1:123456789012:mystack-mytopic-ABCDEFGHIJKL"
            },
            "BoundingBoxRegionsOfInterest": [
                {
                    "Height": 0.4,
                    "Width": 0.2,
                    "Left": 0.1,
                    "Top": 0.5
                },
                {
                    "Height": 0.2,
                    "Width": 0.4,
                    "Left": 0.1,
                    "Top": 0.3
                }
            ],
            "PolygonRegionsOfInterest": [
                [
                    {
                        "X": 0.2,
                        "Y": 0.4
                    },
                    {
                        "X": 0.1,
                        "Y": 0.5
                    },
                    {
                        "X": 0.6,
                        "Y": 0.6
                    }
                ],
                [
                    {
                        "X": 0.6,
                        "Y": 0.3
                    },
                    {
                        "X": 0.2,
                        "Y": 0.7
                    },
                    {
                        "X": 0.1,
                        "Y": 0.1
                    }
                ]
            ],
            "Tags": [
                {
                    "Key": "Key1",
                    "Value": "Value1"
                },
                {
                    "Key": "Key2",
                    "Value": "Value2"
                }
            ]
        }
    }
}
```

#### YAML<a name="aws-resource-rekognition-streamprocessor--examples--StreamProcessor_to_detect_ConnectedHome_labels_with_specific_bounding-box_based_regions_of_interest_and_polygon_based_regions_of_interest_and_polygons_configured--yaml"></a>

```
ExampleStreamProcessor:
    Type: AWS::Rekognition::StreamProcessor
    Properties:
      RoleArn: 'arn:aws:iam::123456789012:role/RoleForRekognition'
      KmsKeyId: '1234abcd-12ab-34cd-56ef-1234567890ab'
      KinesisVideoStream:
        Arn: 'arn:aws:kinesisvideo:us-east-1:123456789012:stream/my-stream/0123456789012'
      ConnectedHomeSettings:
        Labels:
          - "PERSON"
          - "PACKAGE"
        MinConfidence: 60
      S3Destination:
        BucketName: 'MyS3Bucket'
        ObjectKeyPrefix: '/my/prefix/'
      NotificationChannel:
        Arn: 'arn:aws:sns:us-east-1:123456789012:mystack-mytopic-ABCDEFGHIJKL'
      BoundingBoxRegionsOfInterest:
        - Height: 0.4
          Width: 0.2
          Left: 0.1
          Top: 0.5
        - Height: 0.2
          Width: 0.4
          Left: 0.1
          Top: 0.3
      PolygonRegionsOfInterest:
        -
          - X: 0.2
            Y: 0.4
          - X: 0.1
            Y: 0.5
          - X: 0.6
            Y: 0.6
        -
          - X: 0.6
            Y: 0.3
          - X: 0.2
            Y: 0.7
          - X: 0.1
            Y: 0.1
      Tags:
        - Key: 'Key1'
          Value: 'Value1'
        - Key: 'Key2'
          Value: 'Value2'
```

### StreamProcessor to detect ConnectedHome labels with specific bounding\-box based regions of interest and polygon based regions of interest configured<a name="aws-resource-rekognition-streamprocessor--examples--StreamProcessor_to_detect_ConnectedHome_labels_with_specific_bounding-box_based_regions_of_interest_and_polygon_based_regions_of_interest_configured"></a>

This template creates a stream processor that is configured to detect PERSON and PACKAGE\. The template configures specific regions of interest using `BoundingBoxRegionsOfInterest` , hence Rekognition outputs labels of interest detected within those defined bounding boxes\. The template also specifies the optional KMS key ID which Rekognition uses to encrypt results while publishing data to the Amazon S3 bucket\.

#### JSON<a name="aws-resource-rekognition-streamprocessor--examples--StreamProcessor_to_detect_ConnectedHome_labels_with_specific_bounding-box_based_regions_of_interest_and_polygon_based_regions_of_interest_configured--json"></a>

```
{
    "ExampleStreamProcessor": {
        "Type": "AWS::Rekognition::StreamProcessor",
        "Properties": {
            "RoleArn": "arn:aws:iam::123456789012:role/RoleForRekognition",
            "KmsKeyId": "1234abcd-12ab-34cd-56ef-1234567890ab",
            "KinesisVideoStream": {
                "Arn": "arn:aws:kinesisvideo:us-east-1:123456789012:stream/my-stream/0123456789012"
            },
            "ConnectedHomeSettings": {
                "Labels": [
                    "PERSON",
                    "PACKAGE"
                ],
                "MinConfidence": 60
            },
            "S3Destination": {
                "BucketName": "MyS3Bucket",
                "ObjectKeyPrefix": "/my/prefix/"
            },
            "NotificationChannel": {
                "Arn": "arn:aws:sns:us-east-1:123456789012:mystack-mytopic-ABCDEFGHIJKL"
            },
            "BoundingBoxRegionsOfInterest": [
                {
                    "Height": 0.4,
                    "Width": 0.2,
                    "Left": 0.1,
                    "Top": 0.5
                },
                {
                    "Height": 0.2,
                    "Width": 0.4,
                    "Left": 0.1,
                    "Top": 0.3
                }
            ],
            "Tags": [
                {
                    "Key": "Key1",
                    "Value": "Value1"
                },
                {
                    "Key": "Key2",
                    "Value": "Value2"
                }
            ]
        }
    }
}
```

#### YAML<a name="aws-resource-rekognition-streamprocessor--examples--StreamProcessor_to_detect_ConnectedHome_labels_with_specific_bounding-box_based_regions_of_interest_and_polygon_based_regions_of_interest_configured--yaml"></a>

```
ExampleStreamProcessor:
    Type: AWS::Rekognition::StreamProcessor
    Properties:
      RoleArn: 'arn:aws:iam::123456789012:role/RoleForRekognition'
      KmsKeyId: '1234abcd-12ab-34cd-56ef-1234567890ab'
      KinesisVideoStream:
        Arn: 'arn:aws:kinesisvideo:us-east-1:123456789012:stream/my-stream/0123456789012'
      ConnectedHomeSettings:
        Labels:
          - "PERSON"
          - "PACKAGE"
        MinConfidence: 60
      S3Destination:
        BucketName: 'MyS3Bucket'
        ObjectKeyPrefix: '/my/prefix/'
      NotificationChannel:
        Arn: 'arn:aws:sns:us-east-1:123456789012:mystack-mytopic-ABCDEFGHIJKL'
      BoundingBoxRegionsOfInterest:
        - Height: 0.4
          Width: 0.2
          Left: 0.1
          Top: 0.5
        - Height: 0.2
          Width: 0.4
          Left: 0.1
          Top: 0.3
      Tags:
        - Key: 'Key1'
          Value: 'Value1'
        - Key: 'Key2'
          Value: 'Value2'
```

### StreamProcessor to detect ConnectedHome labels with specific polygons configured<a name="aws-resource-rekognition-streamprocessor--examples--StreamProcessor_to_detect_ConnectedHome_labels_with_specific_polygons_configured"></a>

This template creates a stream processor that is configured to detect PERSON and PACKAGE\. The template configures specific regions of interest using `PolygonRegionsOfInterest` , hence Rekognition outputs labels of interest detected within those defined polygons\. The template also specifies the optional KMS key ID which Rekognition uses to encrypt results while publishing data to the Amazon S3 bucket\.

#### JSON<a name="aws-resource-rekognition-streamprocessor--examples--StreamProcessor_to_detect_ConnectedHome_labels_with_specific_polygons_configured--json"></a>

```
{
    "ExampleStreamProcessor": {
        "Type": "AWS::Rekognition::StreamProcessor",
        "Properties": {
            "RoleArn": "arn:aws:iam::123456789012:role/RoleForRekognition",
            "KmsKeyId": "1234abcd-12ab-34cd-56ef-1234567890ab",
            "KinesisVideoStream": {
                "Arn": "arn:aws:kinesisvideo:us-east-1:123456789012:stream/my-stream/0123456789012"
            },
            "ConnectedHomeSettings": {
                "Labels": [
                    "PERSON",
                    "PACKAGE"
                ],
                "MinConfidence": 60
            },
            "S3Destination": {
                "BucketName": "MyS3Bucket",
                "ObjectKeyPrefix": "/my/prefix/"
            },
            "NotificationChannel": {
                "Arn": "arn:aws:sns:us-east-1:123456789012:mystack-mytopic-ABCDEFGHIJKL"
            },
            "PolygonRegionsOfInterest": [
                [
                    {
                        "X": 0.2,
                        "Y": 0.4
                    },
                    {
                        "X": 0.1,
                        "Y": 0.5
                    },
                    {
                        "X": 0.6,
                        "Y": 0.6
                    }
                ],
                [
                    {
                        "X": 0.6,
                        "Y": 0.3
                    },
                    {
                        "X": 0.2,
                        "Y": 0.7
                    },
                    {
                        "X": 0.1,
                        "Y": 0.1
                    }
                ]
            ],
            "Tags": [
                {
                    "Key": "Key1",
                    "Value": "Value1"
                },
                {
                    "Key": "Key2",
                    "Value": "Value2"
                }
            ]
        }
    }
}
```

#### YAML<a name="aws-resource-rekognition-streamprocessor--examples--StreamProcessor_to_detect_ConnectedHome_labels_with_specific_polygons_configured--yaml"></a>

```
ExampleStreamProcessor:
    Type: AWS::Rekognition::StreamProcessor
    Properties:
      RoleArn: 'arn:aws:iam::123456789012:role/RoleForRekognition'
      KmsKeyId: '1234abcd-12ab-34cd-56ef-1234567890ab'
      KinesisVideoStream:
        Arn: 'arn:aws:kinesisvideo:us-east-1:123456789012:stream/my-stream/0123456789012'
      ConnectedHomeSettings:
        Labels:
          - "PERSON"
          - "PACKAGE"
        MinConfidence: 60
      S3Destination:
        BucketName: 'MyS3Bucket'
        ObjectKeyPrefix: '/my/prefix/'
      NotificationChannel:
        Arn: 'arn:aws:sns:us-east-1:123456789012:mystack-mytopic-ABCDEFGHIJKL'
      PolygonRegionsOfInterest:
        -
          - X: 0.2
            Y: 0.4
          - X: 0.1
            Y: 0.5
          - X: 0.6
            Y: 0.6
        -
          - X: 0.6
            Y: 0.3
          - X: 0.2
            Y: 0.7
          - X: 0.1
            Y: 0.1
      Tags:
        - Key: 'Key1'
          Value: 'Value1'
        - Key: 'Key2'
          Value: 'Value2'
```