# AWS::QuickSight::Topic<a name="aws-resource-quicksight-topic"></a>

Creates a new Q topic\.

## Syntax<a name="aws-resource-quicksight-topic-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-quicksight-topic-syntax.json"></a>

```
{
  "Type" : "AWS::QuickSight::Topic",
  "Properties" : {
      "[AwsAccountId](#cfn-quicksight-topic-awsaccountid)" : String,
      "[DataSets](#cfn-quicksight-topic-datasets)" : [ DatasetMetadata, ... ],
      "[Description](#cfn-quicksight-topic-description)" : String,
      "[Name](#cfn-quicksight-topic-name)" : String,
      "[TopicId](#cfn-quicksight-topic-topicid)" : String
    }
}
```

### YAML<a name="aws-resource-quicksight-topic-syntax.yaml"></a>

```
Type: AWS::QuickSight::Topic
Properties: 
  [AwsAccountId](#cfn-quicksight-topic-awsaccountid): String
  [DataSets](#cfn-quicksight-topic-datasets): 
    - DatasetMetadata
  [Description](#cfn-quicksight-topic-description): String
  [Name](#cfn-quicksight-topic-name): String
  [TopicId](#cfn-quicksight-topic-topicid): String
```

## Properties<a name="aws-resource-quicksight-topic-properties"></a>

`AwsAccountId`  <a name="cfn-quicksight-topic-awsaccountid"></a>
The ID of the AWS account that you want to create a topic in\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `12`  
*Maximum*: `12`  
*Pattern*: `^[0-9]{12}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DataSets`  <a name="cfn-quicksight-topic-datasets"></a>
The data sets that the topic is associated with\.  
*Required*: Yes  
*Type*: List of [DatasetMetadata](aws-properties-quicksight-topic-datasetmetadata.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-quicksight-topic-description"></a>
The description of the topic\.  
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-quicksight-topic-name"></a>
The name of the topic\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TopicId`  <a name="cfn-quicksight-topic-topicid"></a>
The ID for the topic\. This ID is unique per AWS Region for each AWS account\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `^[A-Za-z0-9-_.\\+]*$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-quicksight-topic-return-values"></a>

### Ref<a name="aws-resource-quicksight-topic-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-quicksight-topic-return-values-fn--getatt"></a>

#### <a name="aws-resource-quicksight-topic-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the topic\.