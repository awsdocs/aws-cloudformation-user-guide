# AWS::Connect::ContactFlow<a name="aws-resource-connect-contactflow"></a>

The `AWS::Connect::ContactFlow` resource specifies a contact flow for the specified Amazon Connect instance\.

## Syntax<a name="aws-resource-connect-contactflow-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-connect-contactflow-syntax.json"></a>

```
{
  "Type" : "AWS::Connect::ContactFlow",
  "Properties" : {
      "[Content](#cfn-connect-contactflow-content)" : String,
      "[Description](#cfn-connect-contactflow-description)" : String,
      "[InstanceArn](#cfn-connect-contactflow-instancearn)" : String,
      "[Name](#cfn-connect-contactflow-name)" : String,
      "[State](#cfn-connect-contactflow-state)" : String,
      "[Tags](#cfn-connect-contactflow-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Type](#cfn-connect-contactflow-type)" : String
    }
}
```

### YAML<a name="aws-resource-connect-contactflow-syntax.yaml"></a>

```
Type: AWS::Connect::ContactFlow
Properties: 
  [Content](#cfn-connect-contactflow-content): String
  [Description](#cfn-connect-contactflow-description): String
  [InstanceArn](#cfn-connect-contactflow-instancearn): String
  [Name](#cfn-connect-contactflow-name): String
  [State](#cfn-connect-contactflow-state): String
  [Tags](#cfn-connect-contactflow-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Type](#cfn-connect-contactflow-type): String
```

## Properties<a name="aws-resource-connect-contactflow-properties"></a>

`Content`  <a name="cfn-connect-contactflow-content"></a>
The content of the contact flow\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-connect-contactflow-description"></a>
The description of the contact flow\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceArn`  <a name="cfn-connect-contactflow-instancearn"></a>
The Amazon Resource Name \(ARN\) of the Amazon Connect instance\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-connect-contactflow-name"></a>
The name of the contact flow\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`State`  <a name="cfn-connect-contactflow-state"></a>
The state of the contact flow\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ACTIVE | ARCHIVED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-connect-contactflow-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-connect-contactflow-type"></a>
The type of the contact flow\. For descriptions of the available types, see [Choose a Contact Flow Type](https://docs.aws.amazon.com/connect/latest/adminguide/create-contact-flow.html#contact-flow-types) in the *Amazon Connect Administrator Guide*\.  
*Required*: No  
*Type*: String  
*Allowed values*: `AGENT_HOLD | AGENT_TRANSFER | AGENT_WHISPER | CONTACT_FLOW | CUSTOMER_HOLD | CUSTOMER_QUEUE | CUSTOMER_WHISPER | OUTBOUND_WHISPER | QUEUE_TRANSFER`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-connect-contactflow-return-values"></a>

### Ref<a name="aws-resource-connect-contactflow-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the contact flow name\. For example:

`{ "Ref": "myContactFlowName" }`

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-connect-contactflow-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-connect-contactflow-return-values-fn--getatt-fn--getatt"></a>

`ContactFlowArn`  <a name="ContactFlowArn-fn::getatt"></a>
When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the contact flow Amazon Resource Name \(ARN\)\. For example:  
`{ "Ref": "myContactFlowArn" }`  
For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-connect-contactflow--examples"></a>



### Specify a contact flow resource<a name="aws-resource-connect-contactflow--examples--Specify_a_contact_flow_resource"></a>

The following example specifies a contact flow resource for an Amazon Connect instance\.

#### YAML<a name="aws-resource-connect-contactflow--examples--Specify_a_contact_flow_resource--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: Specifies a contact flow for Amazon Connect instance
Resources:
  ContactFlow:
    Type: 'AWS::Connect::ContactFlow'
    Properties:
      Name: ExampleContactFlow
      Description: contact flow created using cfn
      InstanceArn: arn:aws:connect:region-name:aws-account-id:instance/instance-arn
      Type: CONTACT_FLOW
      Content: ExampleContactFlow content(JSON) using Amazon Connect Flow Language.
      Tags:
        - Key: testkey
          Value: testValue
```