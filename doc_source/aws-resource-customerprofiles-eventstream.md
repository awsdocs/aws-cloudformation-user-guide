# AWS::CustomerProfiles::EventStream<a name="aws-resource-customerprofiles-eventstream"></a>

An Event Stream resource of Amazon Connect Customer Profiles\.

## Syntax<a name="aws-resource-customerprofiles-eventstream-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-customerprofiles-eventstream-syntax.json"></a>

```
{
  "Type" : "AWS::CustomerProfiles::EventStream",
  "Properties" : {
      "[DomainName](#cfn-customerprofiles-eventstream-domainname)" : String,
      "[EventStreamName](#cfn-customerprofiles-eventstream-eventstreamname)" : String,
      "[Tags](#cfn-customerprofiles-eventstream-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Uri](#cfn-customerprofiles-eventstream-uri)" : String
    }
}
```

### YAML<a name="aws-resource-customerprofiles-eventstream-syntax.yaml"></a>

```
Type: AWS::CustomerProfiles::EventStream
Properties: 
  [DomainName](#cfn-customerprofiles-eventstream-domainname): String
  [EventStreamName](#cfn-customerprofiles-eventstream-eventstreamname): String
  [Tags](#cfn-customerprofiles-eventstream-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Uri](#cfn-customerprofiles-eventstream-uri): String
```

## Properties<a name="aws-resource-customerprofiles-eventstream-properties"></a>

`DomainName`  <a name="cfn-customerprofiles-eventstream-domainname"></a>
The unique name of the domain\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EventStreamName`  <a name="cfn-customerprofiles-eventstream-eventstreamname"></a>
The name of the event stream\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-customerprofiles-eventstream-tags"></a>
The tags used to organize, track, or control access for this resource\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Uri`  <a name="cfn-customerprofiles-eventstream-uri"></a>
The StreamARN of the destination to deliver profile events to\. For example, arn:aws:kinesis:region:account\-id:stream/stream\-name\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-customerprofiles-eventstream-return-values"></a>

### Ref<a name="aws-resource-customerprofiles-eventstream-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-customerprofiles-eventstream-return-values-fn--getatt"></a>

#### <a name="aws-resource-customerprofiles-eventstream-return-values-fn--getatt-fn--getatt"></a>

`CreatedAt`  <a name="CreatedAt-fn::getatt"></a>
The timestamp of when the export was created\.

`DestinationDetails`  <a name="DestinationDetails-fn::getatt"></a>
Details regarding the Kinesis stream\.

`DestinationDetails.Status`  <a name="DestinationDetails.Status-fn::getatt"></a>
The status of enabling the Kinesis stream as a destination for export\.

`DestinationDetails.Uri`  <a name="DestinationDetails.Uri-fn::getatt"></a>
The StreamARN of the destination to deliver profile events to\. For example, arn:aws:kinesis:region:account\-id:stream/stream\-name\.

`EventStreamArn`  <a name="EventStreamArn-fn::getatt"></a>
A unique identifier for the event stream\.

`State`  <a name="State-fn::getatt"></a>
The operational state of destination stream for export\.