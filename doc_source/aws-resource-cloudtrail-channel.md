# AWS::CloudTrail::Channel<a name="aws-resource-cloudtrail-channel"></a>

Contains information about a returned CloudTrail channel\.

## Syntax<a name="aws-resource-cloudtrail-channel-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cloudtrail-channel-syntax.json"></a>

```
{
  "Type" : "AWS::CloudTrail::Channel",
  "Properties" : {
      "[Destinations](#cfn-cloudtrail-channel-destinations)" : [ Destination, ... ],
      "[Name](#cfn-cloudtrail-channel-name)" : String,
      "[Source](#cfn-cloudtrail-channel-source)" : String,
      "[Tags](#cfn-cloudtrail-channel-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-cloudtrail-channel-syntax.yaml"></a>

```
Type: AWS::CloudTrail::Channel
Properties: 
  [Destinations](#cfn-cloudtrail-channel-destinations): 
    - Destination
  [Name](#cfn-cloudtrail-channel-name): String
  [Source](#cfn-cloudtrail-channel-source): String
  [Tags](#cfn-cloudtrail-channel-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-cloudtrail-channel-properties"></a>

`Destinations`  <a name="cfn-cloudtrail-channel-destinations"></a>
One or more event data stores to which events arriving through a channel will be logged\.  
*Required*: No  
*Type*: List of [Destination](aws-properties-cloudtrail-channel-destination.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-cloudtrail-channel-name"></a>
The name of the channel\.  
*Required*: No  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `128`  
*Pattern*: `^[a-zA-Z0-9._\-]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Source`  <a name="cfn-cloudtrail-channel-source"></a>
The name of the partner or external event source\. You cannot change this name after you create the channel\. A maximum of one channel is allowed per source\.  
 A source can be either `Custom` for all valid non\-AWS events, or the name of a partner event source\. For information about the source names for available partners, see [Additional information about integration partners](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/query-event-data-store-integration.html#cloudtrail-lake-partner-information) in the CloudTrail User Guide\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-cloudtrail-channel-tags"></a>
A list of tags\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-cloudtrail-channel-return-values"></a>

### Ref<a name="aws-resource-cloudtrail-channel-return-values-ref"></a>

When the logical ID of this resource is provided to the Ref intrinsic function, `Ref` returns the resource name\. 

### Fn::GetAtt<a name="aws-resource-cloudtrail-channel-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-cloudtrail-channel-return-values-fn--getatt-fn--getatt"></a>

`ChannelArn`  <a name="ChannelArn-fn::getatt"></a>
 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ARN of the CloudTrail channel, such as `arn:aws:cloudtrail:us-east-2:123456789012:channel/01234567890`\.

## Examples<a name="aws-resource-cloudtrail-channel--examples"></a>

### Example<a name="aws-resource-cloudtrail-channel--examples--Example"></a>

The following example creates a channel for a CloudTrail Lake integration with an event source outside of AWS\. For information about CloudTrail Lake integrations, see [Create an integration with an event source outside of AWS](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/query-event-data-store-integration.html) in the *AWS CloudTrail User Guide*\.

#### JSON<a name="aws-resource-cloudtrail-channel--examples--Example--json"></a>

```
{
    "Parameters": {
    	"Name" : String,
      	"EventDataStoreArn" : String,
      	"Source" : String
    },
    "Resources": {
        "myChannel": {
            "Type": "AWS::CloudTrail::Channel",
            "Properties": {
                "Name": {
                    "Ref": "Name"
                },
                "Source": {
                    "Ref": "Source"
                },
                "Destinations": [
                    {
                        "Type": "EVENT_DATA_STORE",
                        "Location": "{
                        	"Ref": "arn:aws:cloudtrail:us-east-1:12345678910:eventdatastore/EXAMPLE-f852-4e8f-8bd1-bcf6cEXAMPLE"
                    	}
                    }
                ],
                "Tags": [
                    {
                        "Key": "TagKeyIntTest",
                        "Value": "TagValueIntTest"
                    },
                    {
                        "Key": "TagKeyIntTest2",
                        "Value": "TagValueIntTest2"
                    }
                ]
            }
        }
    },
    "Outputs": {
        "myChannelArn": {
            "Description": "The channel ARN",
            "Value": {
                "Fn::GetAtt": [
                    "myChannel",
                    "arn:aws:cloudtrail:us-east-1:01234567890:channel/EXAMPLE8-0558-4f7e-a06a-43969EXAMPLE"
                ]
            }
        }
    }
}
```

#### YAML<a name="aws-resource-cloudtrail-channel--examples--Example--yaml"></a>

```
Parameters:
  Name:
    Type: String
  EventDataStoreArn:
    Type: String
  Source:
    Type: String
Resources:
  myChannel:
    Type: AWS::CloudTrail::Channel
    Properties:
      Name: !Ref Name
      Source: !Ref Source
      Destinations:
        - Type: "EVENT_DATA_STORE"
          Location: !Ref arn:aws:cloudtrail:us-east-1:12345678910:eventdatastore/EXAMPLE-f852-4e8f-8bd1-bcf6cEXAMPLE
      Tags:
        - Key: "TagKeyIntTest"
          Value: "TagValueIntTest"
        - Key: "TagKeyIntTest2"
          Value: "TagValueIntTest2"
Outputs:
  myChannelArn:
    Description: The channel ARN
    Value:
      'Fn::GetAtt':
        - myChannel
        - arn:aws:cloudtrail:us-east-1:01234567890:channel/EXAMPLE8-0558-4f7e-a06a-43969EXAMPLE
```