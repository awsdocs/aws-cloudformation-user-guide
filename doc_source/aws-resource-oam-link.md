# AWS::Oam::Link<a name="aws-resource-oam-link"></a>

Creates a link between a source account and a sink that you have created in a monitoring account\.

Before you create a link, you must create a sink in the monitoring account\. The sink must have a sink policy that permits the source account to link to it\. You can grant permission to source accounts by granting permission to an entire organization, an organizational unit, or to individual accounts\.

For more information, see [CreateSink](https://docs.aws.amazon.com/OAM/latest/APIReference/API_CreateSink.html) and [PutSinkPolicy](https://docs.aws.amazon.com/OAM/latest/APIReference/API_PutSinkPolicy.html)\.

Each monitoring account can be linked to as many as 100,000 source accounts\.

Each source account can be linked to as many as five monitoring accounts\.

## Syntax<a name="aws-resource-oam-link-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-oam-link-syntax.json"></a>

```
{
  "Type" : "AWS::Oam::Link",
  "Properties" : {
      "[LabelTemplate](#cfn-oam-link-labeltemplate)" : String,
      "[ResourceTypes](#cfn-oam-link-resourcetypes)" : [ String, ... ],
      "[SinkIdentifier](#cfn-oam-link-sinkidentifier)" : String,
      "[Tags](#cfn-oam-link-tags)" : {Key: Value, ...}
    }
}
```

### YAML<a name="aws-resource-oam-link-syntax.yaml"></a>

```
Type: AWS::Oam::Link
Properties: 
  [LabelTemplate](#cfn-oam-link-labeltemplate): String
  [ResourceTypes](#cfn-oam-link-resourcetypes): 
    - String
  [SinkIdentifier](#cfn-oam-link-sinkidentifier): String
  [Tags](#cfn-oam-link-tags): 
    Key: Value
```

## Properties<a name="aws-resource-oam-link-properties"></a>

`LabelTemplate`  <a name="cfn-oam-link-labeltemplate"></a>
Specify a friendly human\-readable name to use to identify this source account when you are viewing data from it in the monitoring account\.  
You can include the following variables in your template:  
+ `$AccountName` is the name of the account
+ `$AccountEmail` is a globally\-unique email address, which includes the email domain, such as `mariagarcia@example.com`
+ `$AccountEmailNoDomain` is an email address without the domain name, such as `mariagarcia`
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ResourceTypes`  <a name="cfn-oam-link-resourcetypes"></a>
An array of strings that define which types of data that the source account shares with the monitoring account\. Valid values are `AWS::CloudWatch::Metric | AWS::Logs::LogGroup | AWS::XRay::Trace`\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SinkIdentifier`  <a name="cfn-oam-link-sinkidentifier"></a>
The ARN of the sink in the monitoring account that you want to link to\. You can use [ListSinks](https://docs.aws.amazon.com/OAM/latest/APIReference/API_ListSinks.html) to find the ARNs of sinks\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-oam-link-tags"></a>
An array of key\-value pairs to apply to the link\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-oam-link-return-values"></a>

### Ref<a name="aws-resource-oam-link-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the ARN of the link\. For example, `arn:aws:oam:us-west-1:111111111111:link:abcd1234-a123-456a-a12b-a123b456c789`\.

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-oam-link-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-oam-link-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the link\. For example, `arn:aws:oam:us-west-1:111111111111:link:abcd1234-a123-456a-a12b-a123b456c789`

`Label`  <a name="Label-fn::getatt"></a>
The friendly human\-readable name used to identify this source account when it is viewed from the monitoring account\. For example, `my-account1`\.

## Examples<a name="aws-resource-oam-link--examples"></a>



### Sample CloudWatch cross\-account observability link<a name="aws-resource-oam-link--examples--Sample_CloudWatch_cross-account_observability_link"></a>

This example creates a link from the current source account to the sink created in the `111111111111` account\. Over this link, logs and traces are shared but metrics are not\.

#### JSON<a name="aws-resource-oam-link--examples--Sample_CloudWatch_cross-account_observability_link--json"></a>

```
{
    "LabelTemplate": "$AccountEmail",
    "ResourceTypes": [
        "AWS::Logs::LogGroup",
        "AWS::XRay::Trace"
    ],
    "SinkIdentifier": "arn:aws:oam:eu-north-1:1111111111111111:sink/EXAMPLE-206d-4daf-9b42-1e17d5f145ef"
}
```

#### YAML<a name="aws-resource-oam-link--examples--Sample_CloudWatch_cross-account_observability_link--yaml"></a>

```
LabelTemplate: "$AccountEmail"
ResourceTypes:
   - "AWS::CloudWatch::Metric"
   - "AWS::Logs::LogGroup"
SinkIdentifier: "arn:aws:oam:eu-north-1:1111111111111111:sink/EXAMPLE-206d-4daf-9b42-1e17d5f145ef"
```