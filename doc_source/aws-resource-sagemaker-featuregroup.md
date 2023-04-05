# AWS::SageMaker::FeatureGroup<a name="aws-resource-sagemaker-featuregroup"></a>

Create a new `FeatureGroup`\. A `FeatureGroup` is a group of `Features` defined in the `FeatureStore` to describe a `Record`\. 

The `FeatureGroup` defines the schema and features contained in the FeatureGroup\. A `FeatureGroup` definition is composed of a list of `Features`, a `RecordIdentifierFeatureName`, an `EventTimeFeatureName` and configurations for its `OnlineStore` and `OfflineStore`\. Check [AWS service quotas](https://docs.aws.amazon.com/general/latest/gr/aws_service_limits.html) to see the `FeatureGroup`s quota for your AWS account\.

**Important**  
You must include at least one of `OnlineStoreConfig` and `OfflineStoreConfig` to create a `FeatureGroup`\.

## Syntax<a name="aws-resource-sagemaker-featuregroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-sagemaker-featuregroup-syntax.json"></a>

```
{
  "Type" : "AWS::SageMaker::FeatureGroup",
  "Properties" : {
      "[Description](#cfn-sagemaker-featuregroup-description)" : String,
      "[EventTimeFeatureName](#cfn-sagemaker-featuregroup-eventtimefeaturename)" : String,
      "[FeatureDefinitions](#cfn-sagemaker-featuregroup-featuredefinitions)" : [ FeatureDefinition, ... ],
      "[FeatureGroupName](#cfn-sagemaker-featuregroup-featuregroupname)" : String,
      "[OfflineStoreConfig](#cfn-sagemaker-featuregroup-offlinestoreconfig)" : OfflineStoreConfig,
      "[OnlineStoreConfig](#cfn-sagemaker-featuregroup-onlinestoreconfig)" : OnlineStoreConfig,
      "[RecordIdentifierFeatureName](#cfn-sagemaker-featuregroup-recordidentifierfeaturename)" : String,
      "[RoleArn](#cfn-sagemaker-featuregroup-rolearn)" : String,
      "[Tags](#cfn-sagemaker-featuregroup-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-sagemaker-featuregroup-syntax.yaml"></a>

```
Type: AWS::SageMaker::FeatureGroup
Properties: 
  [Description](#cfn-sagemaker-featuregroup-description): String
  [EventTimeFeatureName](#cfn-sagemaker-featuregroup-eventtimefeaturename): String
  [FeatureDefinitions](#cfn-sagemaker-featuregroup-featuredefinitions): 
    - FeatureDefinition
  [FeatureGroupName](#cfn-sagemaker-featuregroup-featuregroupname): String
  [OfflineStoreConfig](#cfn-sagemaker-featuregroup-offlinestoreconfig): 
    OfflineStoreConfig
  [OnlineStoreConfig](#cfn-sagemaker-featuregroup-onlinestoreconfig): 
    OnlineStoreConfig
  [RecordIdentifierFeatureName](#cfn-sagemaker-featuregroup-recordidentifierfeaturename): String
  [RoleArn](#cfn-sagemaker-featuregroup-rolearn): String
  [Tags](#cfn-sagemaker-featuregroup-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-sagemaker-featuregroup-properties"></a>

`Description`  <a name="cfn-sagemaker-featuregroup-description"></a>
A free form description of a `FeatureGroup`\.  
*Required*: No  
*Type*: String  
*Maximum*: `128`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EventTimeFeatureName`  <a name="cfn-sagemaker-featuregroup-eventtimefeaturename"></a>
The name of the feature that stores the `EventTime` of a Record in a `FeatureGroup`\.  
A `EventTime` is point in time when a new event occurs that corresponds to the creation or update of a `Record` in `FeatureGroup`\. All `Records` in the `FeatureGroup` must have a corresponding `EventTime`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Pattern*: `^[a-zA-Z0-9]([-_]*[a-zA-Z0-9]){0,63}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FeatureDefinitions`  <a name="cfn-sagemaker-featuregroup-featuredefinitions"></a>
A list of `Feature`s\. Each `Feature` must include a `FeatureName` and a `FeatureType`\.   
Valid `FeatureType`s are `Integral`, `Fractional` and `String`\.   
 `FeatureName`s cannot be any of the following: `is_deleted`, `write_time`, `api_invocation_time`\.  
You can create up to 2,500 `FeatureDefinition`s per `FeatureGroup`\.  
*Required*: Yes  
*Type*: List of [FeatureDefinition](aws-properties-sagemaker-featuregroup-featuredefinition.md)  
*Maximum*: `2500`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FeatureGroupName`  <a name="cfn-sagemaker-featuregroup-featuregroupname"></a>
The name of the `FeatureGroup`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Pattern*: `^[a-zA-Z0-9]([_-]*[a-zA-Z0-9]){0,63}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`OfflineStoreConfig`  <a name="cfn-sagemaker-featuregroup-offlinestoreconfig"></a>
The configuration of an `OfflineStore`\.  
*Required*: No  
*Type*: [OfflineStoreConfig](aws-properties-sagemaker-featuregroup-offlinestoreconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`OnlineStoreConfig`  <a name="cfn-sagemaker-featuregroup-onlinestoreconfig"></a>
The configuration of an `OnlineStore`\.  
*Required*: No  
*Type*: [OnlineStoreConfig](aws-properties-sagemaker-featuregroup-onlinestoreconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RecordIdentifierFeatureName`  <a name="cfn-sagemaker-featuregroup-recordidentifierfeaturename"></a>
The name of the `Feature` whose value uniquely identifies a `Record` defined in the `FeatureGroup` `FeatureDefinitions`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Pattern*: `^[a-zA-Z0-9]([-_]*[a-zA-Z0-9]){0,63}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RoleArn`  <a name="cfn-sagemaker-featuregroup-rolearn"></a>
The Amazon Resource Name \(ARN\) of the IAM execution role used to create the feature group\.  
*Required*: No  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `^arn:aws[a-z\-]*:iam::\d{12}:role/?[a-zA-Z_0-9+=,.@\-_/]+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-sagemaker-featuregroup-tags"></a>
Tags used to define a `FeatureGroup`\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-sagemaker-featuregroup-return-values"></a>

### Ref<a name="aws-resource-sagemaker-featuregroup-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `FeatureGroupName` of the feature group\.