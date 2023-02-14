# AWS::Evidently::Feature<a name="aws-resource-evidently-feature"></a>

Creates or updates an Evidently *feature* that you want to launch or test\. You can define up to five variations of a feature, and use these variations in your launches and experiments\. A feature must be created in a project\. For information about creating a project, see [CreateProject](https://docs.aws.amazon.com/cloudwatchevidently/latest/APIReference/API_CreateProject.html)\.

## Syntax<a name="aws-resource-evidently-feature-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-evidently-feature-syntax.json"></a>

```
{
  "Type" : "AWS::Evidently::Feature",
  "Properties" : {
      "[DefaultVariation](#cfn-evidently-feature-defaultvariation)" : String,
      "[Description](#cfn-evidently-feature-description)" : String,
      "[EntityOverrides](#cfn-evidently-feature-entityoverrides)" : [ EntityOverride, ... ],
      "[EvaluationStrategy](#cfn-evidently-feature-evaluationstrategy)" : String,
      "[Name](#cfn-evidently-feature-name)" : String,
      "[Project](#cfn-evidently-feature-project)" : String,
      "[Tags](#cfn-evidently-feature-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Variations](#cfn-evidently-feature-variations)" : [ VariationObject, ... ]
    }
}
```

### YAML<a name="aws-resource-evidently-feature-syntax.yaml"></a>

```
Type: AWS::Evidently::Feature
Properties: 
  [DefaultVariation](#cfn-evidently-feature-defaultvariation): String
  [Description](#cfn-evidently-feature-description): String
  [EntityOverrides](#cfn-evidently-feature-entityoverrides): 
    - EntityOverride
  [EvaluationStrategy](#cfn-evidently-feature-evaluationstrategy): String
  [Name](#cfn-evidently-feature-name): String
  [Project](#cfn-evidently-feature-project): String
  [Tags](#cfn-evidently-feature-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Variations](#cfn-evidently-feature-variations): 
    - VariationObject
```

## Properties<a name="aws-resource-evidently-feature-properties"></a>

`DefaultVariation`  <a name="cfn-evidently-feature-defaultvariation"></a>
The name of the variation to use as the default variation\. The default variation is served to users who are not allocated to any ongoing launches or experiments of this feature\.  
This variation must also be listed in the `Variations` structure\.  
If you omit `DefaultVariation`, the first variation listed in the `Variations` structure is used as the default variation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-evidently-feature-description"></a>
An optional description of the feature\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EntityOverrides`  <a name="cfn-evidently-feature-entityoverrides"></a>
Specify users that should always be served a specific variation of a feature\. Each user is specified by a key\-value pair \. For each key, specify a user by entering their user ID, account ID, or some other identifier\. For the value, specify the name of the variation that they are to be served\.  
*Required*: No  
*Type*: List of [EntityOverride](aws-properties-evidently-feature-entityoverride.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EvaluationStrategy`  <a name="cfn-evidently-feature-evaluationstrategy"></a>
Specify `ALL_RULES` to activate the traffic allocation specified by any ongoing launches or experiments\. Specify `DEFAULT_VARIATION` to serve the default variation to all users instead\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-evidently-feature-name"></a>
The name for the feature\. It can include up to 127 characters\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Project`  <a name="cfn-evidently-feature-project"></a>
The name or ARN of the project that is to contain the new feature\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-evidently-feature-tags"></a>
Assigns one or more tags \(key\-value pairs\) to the feature\.  
Tags can help you organize and categorize your resources\. You can also use them to scope user permissions by granting a user permission to access or change only resources with certain tag values\.  
Tags don't have any semantic meaning to AWS and are interpreted strictly as strings of characters\.  
You can associate as many as 50 tags with a feature\.  
For more information, see [Tagging AWS resources](https://docs.aws.amazon.com/general/latest/gr/aws_tagging.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Variations`  <a name="cfn-evidently-feature-variations"></a>
An array of structures that contain the configuration of the feature's different variations\.  
Each `VariationObject` in the `Variations` array for a feature must have the same type of value \(`BooleanValue`, `DoubleValue`, `LongValue` or `StringValue`\)\.  
*Required*: Yes  
*Type*: List of [VariationObject](aws-properties-evidently-feature-variationobject.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-evidently-feature-return-values"></a>

### Ref<a name="aws-resource-evidently-feature-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ARN of the feature\. For example, `arn:aws:evidently:us-west-2:0123455678912:project/myProject/feature/myFeature` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-evidently-feature-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-evidently-feature-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the feature\. For example, `arn:aws:evidently:us-west-2:0123455678912:project/myProject/feature/myFeature`\.