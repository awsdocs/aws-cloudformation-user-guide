# AWS::WorkSpacesWeb::UserAccessLoggingSettings<a name="aws-resource-workspacesweb-useraccessloggingsettings"></a>

This resource specifies user access logging settings that can be associated with a web portal\.

In order to receive logs from WorkSpaces Web, you must have an Amazon Kinesis Data Stream that starts with "amazon\-workspaces\-web\-\*"\. Your Amazon Kinesis data stream must either have server\-side encryption turned off, or must use AWS managed keys for server\-side encryption\.

For more information about setting server\-side encryption in Amazon Kinesis, see [How Do I Get Started with Server\-Side Encryption?](https://docs.aws.amazon.com/streams/latest/dev/getting-started-with-sse.html)\.

For more information about setting up user access logging, see [Set up user access logging](https://docs.aws.amazon.com/workspaces-web/latest/adminguide/user-logging.html)\.

## Syntax<a name="aws-resource-workspacesweb-useraccessloggingsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-workspacesweb-useraccessloggingsettings-syntax.json"></a>

```
{
  "Type" : "AWS::WorkSpacesWeb::UserAccessLoggingSettings",
  "Properties" : {
      "[KinesisStreamArn](#cfn-workspacesweb-useraccessloggingsettings-kinesisstreamarn)" : String,
      "[Tags](#cfn-workspacesweb-useraccessloggingsettings-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-workspacesweb-useraccessloggingsettings-syntax.yaml"></a>

```
Type: AWS::WorkSpacesWeb::UserAccessLoggingSettings
Properties: 
  [KinesisStreamArn](#cfn-workspacesweb-useraccessloggingsettings-kinesisstreamarn): String
  [Tags](#cfn-workspacesweb-useraccessloggingsettings-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-workspacesweb-useraccessloggingsettings-properties"></a>

`KinesisStreamArn`  <a name="cfn-workspacesweb-useraccessloggingsettings-kinesisstreamarn"></a>
The ARN of the Kinesis stream\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `.*arn:[\w+=/,.@-]+:kinesis:[a-zA-Z0-9\-]*:[a-zA-Z0-9]{1,12}:stream/.+.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-workspacesweb-useraccessloggingsettings-tags"></a>
The tags to add to the user access logging settings resource\. A tag is a key\-value pair\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-workspacesweb-useraccessloggingsettings-return-values"></a>

### Ref<a name="aws-resource-workspacesweb-useraccessloggingsettings-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource's Amazon Resource Name \(ARN\)\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-workspacesweb-useraccessloggingsettings-return-values-fn--getatt"></a>

#### <a name="aws-resource-workspacesweb-useraccessloggingsettings-return-values-fn--getatt-fn--getatt"></a>

`AssociatedPortalArns`  <a name="AssociatedPortalArns-fn::getatt"></a>
A list of web portal ARNs that this user access logging settings is associated with\.

`UserAccessLoggingSettingsArn`  <a name="UserAccessLoggingSettingsArn-fn::getatt"></a>
The ARN of the user access logging settings\.