# AWS::Oam::Sink<a name="aws-resource-oam-sink"></a>

Creates or updates a *sink* in the current account, so that it can be used as a monitoring account in CloudWatch cross\-account observability\. A sink is a resource that represents an attachment point in a monitoring account, which source accounts can link to to be able to send observability data\.

After you create a sink, you must create a sink policy that allows source accounts to attach to it\. For more information, see [PutSinkPolicy](https://docs.aws.amazon.com/OAM/latest/APIReference/API_PutSinkPolicy.html)\.

An account can have one sink\.

## Syntax<a name="aws-resource-oam-sink-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-oam-sink-syntax.json"></a>

```
{
  "Type" : "AWS::Oam::Sink",
  "Properties" : {
      "[Name](#cfn-oam-sink-name)" : String,
      "[Policy](#cfn-oam-sink-policy)" : Json,
      "[Tags](#cfn-oam-sink-tags)" : {Key: Value, ...}
    }
}
```

### YAML<a name="aws-resource-oam-sink-syntax.yaml"></a>

```
Type: AWS::Oam::Sink
Properties: 
  [Name](#cfn-oam-sink-name): String
  [Policy](#cfn-oam-sink-policy): Json
  [Tags](#cfn-oam-sink-tags): 
    Key: Value
```

## Properties<a name="aws-resource-oam-sink-properties"></a>

`Name`  <a name="cfn-oam-sink-name"></a>
A name for the sink\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Policy`  <a name="cfn-oam-sink-policy"></a>
The IAM policy that grants permissions to source accounts to link to this sink\. The policy can grant permission in the following ways:  
+ Include organization IDs or organization paths to permit all accounts in an organization
+ Include account IDs to permit the specified accounts
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-oam-sink-tags"></a>
An array of key\-value pairs to apply to the sink\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-oam-sink-return-values"></a>

### Ref<a name="aws-resource-oam-sink-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the ARN of the link\. For example, `arn:aws:oam:us-west-1:111111111111:link:abcd1234-a123-456a-a12b-a123b456c789`\.

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-oam-sink-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-oam-sink-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the sink\. For example, `arn:aws:oam:us-west-1:111111111111:sink:abcd1234-a123-456a-a12b-a123b456c789`

## Examples<a name="aws-resource-oam-sink--examples"></a>



### Sample sink to connect that permits links to all accounts in an organization<a name="aws-resource-oam-sink--examples--Sample_sink_to_connect_that_permits_links_to_all_accounts_in_an_organization"></a>

This example creates a sink that allows all accounts in a specified organization to create links to share metric and log data\.

#### JSON<a name="aws-resource-oam-sink--examples--Sample_sink_to_connect_that_permits_links_to_all_accounts_in_an_organization--json"></a>

```
"Name": "SampleSink",
"Policy": {
   "Version": "2012-10-17",
   "Statement": [{
       "Effect": "Allow",
       "Principal": "*",
       "Resource": "*",
       "Action": [ "oam:CreateLink", "oam:UpdateLink" ],
       "Condition": {
        "StringEquals": {"aws:PrincipalOrgID":"o-xxxxxxxxxxx"},
        "ForAllValues:StringEquals": {
          "oam:ResourceTypes": [
            "AWS::CloudWatch::Metric",
            "AWS::Logs::LogGroup"
          ]
        }
       }
    }]
}
```

#### YAML<a name="aws-resource-oam-sink--examples--Sample_sink_to_connect_that_permits_links_to_all_accounts_in_an_organization--yaml"></a>

```
Name: "SampleSink"
Policy:
  Version: '2012-10-17'
  Statement:
  - Effect: Allow
    Principal: "*"
    Resource: "*"
    Action:
    - "oam:CreateLink"
    - "oam:UpdateLink"
    Condition:
      StringEquals:
        aws:PrincipalOrgID: o-xxxxxxxxxxx
      ForAllValues:StringEquals:
        oam:ResourceTypes:
          - "AWS::CloudWatch::Metric"
          - "AWS::Logs::LogGroup"
```

### Sample sink that permits a link to an individual account<a name="aws-resource-oam-sink--examples--Sample_sink_that_permits_a_link_to_an_individual_account"></a>

This example creates a sink that allows the account with the ID `111111111111` to create a link to share metrics, logs, and traces\.

#### JSON<a name="aws-resource-oam-sink--examples--Sample_sink_that_permits_a_link_to_an_individual_account--json"></a>

```
"Name": "SampleSink",
"Policy": {
   "Version": "2012-10-17",
   "Statement": [{
       "Effect": "Allow",
       "Resource": "*",
       "Action": "oam:*",
       "Principal": {
        "AWS": [ "1111111111111" ]
       },
       "Condition": {
        "ForAllValues:StringEquals": {
          "oam:ResourceTypes": [
            "AWS::CloudWatch::Metric",
            "AWS::Logs::LogGroup",
            "AWS::XRay::Trace"
          ]
        }
       }
    }]
}
```

#### YAML<a name="aws-resource-oam-sink--examples--Sample_sink_that_permits_a_link_to_an_individual_account--yaml"></a>

```
Name: "SampleSink"
Policy:
  Version: '2012-10-17'
  Statement:
  - Effect: Allow
    Resource: "*"
    Action: "oam:*"
    Principal:
      AWS:
      - '1111111111111'
    Condition:
      ForAllValues:StringEquals:
        oam:ResourceTypes:
          - "AWS::CloudWatch::Metric"
          - "AWS::Logs::LogGroup"
          - "AWS::XRay::Trace"
```