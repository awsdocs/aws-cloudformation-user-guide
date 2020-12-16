# AWS::CloudWatch::MetricStream<a name="aws-resource-cloudwatch-metricstream"></a>

Reserved for future use\.

## Syntax<a name="aws-resource-cloudwatch-metricstream-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cloudwatch-metricstream-syntax.json"></a>

```
{
  "Type" : "AWS::CloudWatch::MetricStream",
  "Properties" : {
      "[ExcludeFilters](#cfn-cloudwatch-metricstream-excludefilters)" : [ MetricStreamFilter, ... ],
      "[FirehoseArn](#cfn-cloudwatch-metricstream-firehosearn)" : String,
      "[IncludeFilters](#cfn-cloudwatch-metricstream-includefilters)" : [ MetricStreamFilter, ... ],
      "[Name](#cfn-cloudwatch-metricstream-name)" : String,
      "[RoleArn](#cfn-cloudwatch-metricstream-rolearn)" : String,
      "[Tags](#cfn-cloudwatch-metricstream-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-cloudwatch-metricstream-syntax.yaml"></a>

```
Type: AWS::CloudWatch::MetricStream
Properties: 
  [ExcludeFilters](#cfn-cloudwatch-metricstream-excludefilters): 
    - MetricStreamFilter
  [FirehoseArn](#cfn-cloudwatch-metricstream-firehosearn): String
  [IncludeFilters](#cfn-cloudwatch-metricstream-includefilters): 
    - MetricStreamFilter
  [Name](#cfn-cloudwatch-metricstream-name): String
  [RoleArn](#cfn-cloudwatch-metricstream-rolearn): String
  [Tags](#cfn-cloudwatch-metricstream-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-cloudwatch-metricstream-properties"></a>

`ExcludeFilters`  <a name="cfn-cloudwatch-metricstream-excludefilters"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [MetricStreamFilter](aws-properties-cloudwatch-metricstream-metricstreamfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FirehoseArn`  <a name="cfn-cloudwatch-metricstream-firehosearn"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludeFilters`  <a name="cfn-cloudwatch-metricstream-includefilters"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [MetricStreamFilter](aws-properties-cloudwatch-metricstream-metricstreamfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-cloudwatch-metricstream-name"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RoleArn`  <a name="cfn-cloudwatch-metricstream-rolearn"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-cloudwatch-metricstream-tags"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-cloudwatch-metricstream-return-values"></a>

### Ref<a name="aws-resource-cloudwatch-metricstream-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-cloudwatch-metricstream-return-values-fn--getatt"></a>

#### <a name="aws-resource-cloudwatch-metricstream-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

`CreationDate`  <a name="CreationDate-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

`LastUpdateDate`  <a name="LastUpdateDate-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

`State`  <a name="State-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.