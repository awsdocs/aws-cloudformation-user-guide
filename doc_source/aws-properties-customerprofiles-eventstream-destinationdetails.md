# AWS::CustomerProfiles::EventStream DestinationDetails<a name="aws-properties-customerprofiles-eventstream-destinationdetails"></a>

Details regarding the Kinesis stream\.

## Syntax<a name="aws-properties-customerprofiles-eventstream-destinationdetails-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-customerprofiles-eventstream-destinationdetails-syntax.json"></a>

```
{
  "[Status](#cfn-customerprofiles-eventstream-destinationdetails-status)" : String,
  "[Uri](#cfn-customerprofiles-eventstream-destinationdetails-uri)" : String
}
```

### YAML<a name="aws-properties-customerprofiles-eventstream-destinationdetails-syntax.yaml"></a>

```
  [Status](#cfn-customerprofiles-eventstream-destinationdetails-status): String
  [Uri](#cfn-customerprofiles-eventstream-destinationdetails-uri): String
```

## Properties<a name="aws-properties-customerprofiles-eventstream-destinationdetails-properties"></a>

`Status`  <a name="cfn-customerprofiles-eventstream-destinationdetails-status"></a>
The status of enabling the Kinesis stream as a destination for export\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Uri`  <a name="cfn-customerprofiles-eventstream-destinationdetails-uri"></a>
The StreamARN of the destination to deliver profile events to\. For example, arn:aws:kinesis:region:account\-id:stream/stream\-name\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)