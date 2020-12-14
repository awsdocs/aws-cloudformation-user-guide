# AWS::ImageBuilder::ImagePipeline<a name="aws-resource-imagebuilder-imagepipeline"></a>

An image pipeline is the automation configuration for building secure OS images on AWS\. The Image Builder image pipeline is associated with an image recipe that defines the build, validation, and test phases for an image build lifecycle\. An image pipeline can be associated with an infrastructure configuration that defines where your image is built\. You can define attributes, such as instance type, subnets, security groups, logging, and other infrastructure\-related configurations\. You can also associate your image pipeline with a distribution configuration to define how you would like to deploy your image\.

## Syntax<a name="aws-resource-imagebuilder-imagepipeline-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-imagebuilder-imagepipeline-syntax.json"></a>

```
{
  "Type" : "AWS::ImageBuilder::ImagePipeline",
  "Properties" : {
      "[Description](#cfn-imagebuilder-imagepipeline-description)" : String,
      "[DistributionConfigurationArn](#cfn-imagebuilder-imagepipeline-distributionconfigurationarn)" : String,
      "[EnhancedImageMetadataEnabled](#cfn-imagebuilder-imagepipeline-enhancedimagemetadataenabled)" : Boolean,
      "[ImageRecipeArn](#cfn-imagebuilder-imagepipeline-imagerecipearn)" : String,
      "[ImageTestsConfiguration](#cfn-imagebuilder-imagepipeline-imagetestsconfiguration)" : ImageTestsConfiguration,
      "[InfrastructureConfigurationArn](#cfn-imagebuilder-imagepipeline-infrastructureconfigurationarn)" : String,
      "[Name](#cfn-imagebuilder-imagepipeline-name)" : String,
      "[Schedule](#cfn-imagebuilder-imagepipeline-schedule)" : Schedule,
      "[Status](#cfn-imagebuilder-imagepipeline-status)" : String,
      "[Tags](#cfn-imagebuilder-imagepipeline-tags)" : {Key : Value, ...}
    }
}
```

### YAML<a name="aws-resource-imagebuilder-imagepipeline-syntax.yaml"></a>

```
Type: AWS::ImageBuilder::ImagePipeline
Properties: 
  [Description](#cfn-imagebuilder-imagepipeline-description): String
  [DistributionConfigurationArn](#cfn-imagebuilder-imagepipeline-distributionconfigurationarn): String
  [EnhancedImageMetadataEnabled](#cfn-imagebuilder-imagepipeline-enhancedimagemetadataenabled): Boolean
  [ImageRecipeArn](#cfn-imagebuilder-imagepipeline-imagerecipearn): String
  [ImageTestsConfiguration](#cfn-imagebuilder-imagepipeline-imagetestsconfiguration): 
    ImageTestsConfiguration
  [InfrastructureConfigurationArn](#cfn-imagebuilder-imagepipeline-infrastructureconfigurationarn): String
  [Name](#cfn-imagebuilder-imagepipeline-name): String
  [Schedule](#cfn-imagebuilder-imagepipeline-schedule): 
    Schedule
  [Status](#cfn-imagebuilder-imagepipeline-status): String
  [Tags](#cfn-imagebuilder-imagepipeline-tags): 
    Key : Value
```

## Properties<a name="aws-resource-imagebuilder-imagepipeline-properties"></a>

`Description`  <a name="cfn-imagebuilder-imagepipeline-description"></a>
The description of this image pipeline\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DistributionConfigurationArn`  <a name="cfn-imagebuilder-imagepipeline-distributionconfigurationarn"></a>
The Amazon Resource Name \(ARN\) of the distribution configuration associated with this image pipeline\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnhancedImageMetadataEnabled`  <a name="cfn-imagebuilder-imagepipeline-enhancedimagemetadataenabled"></a>
 Collects additional information about the image being created, including the operating system \(OS\) version and package list\. This information is used to enhance the overall experience of using EC2 Image Builder\. Enabled by default\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ImageRecipeArn`  <a name="cfn-imagebuilder-imagepipeline-imagerecipearn"></a>
The Amazon Resource Name \(ARN\) of the image recipe associated with this image pipeline\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ImageTestsConfiguration`  <a name="cfn-imagebuilder-imagepipeline-imagetestsconfiguration"></a>
The configuration of the image tests used when creating this image\.  
*Required*: No  
*Type*: [ImageTestsConfiguration](aws-properties-imagebuilder-imagepipeline-imagetestsconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InfrastructureConfigurationArn`  <a name="cfn-imagebuilder-imagepipeline-infrastructureconfigurationarn"></a>
The Amazon Resource Name \(ARN\) of the infrastructure configuration associated with this image pipeline\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-imagebuilder-imagepipeline-name"></a>
The name of the image pipeline\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `^[-_A-Za-z-0-9][-_A-Za-z0-9 ]{1,126}[-_A-Za-z-0-9]$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Schedule`  <a name="cfn-imagebuilder-imagepipeline-schedule"></a>
The schedule of the image pipeline\. A schedule configures how often and when a pipeline will automatically create a new image\.  
*Required*: No  
*Type*: [Schedule](aws-properties-imagebuilder-imagepipeline-schedule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Status`  <a name="cfn-imagebuilder-imagepipeline-status"></a>
The status of the image pipeline\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DISABLED | ENABLED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-imagebuilder-imagepipeline-tags"></a>
The tags of this image pipeline\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-imagebuilder-imagepipeline-return-values"></a>

### Ref<a name="aws-resource-imagebuilder-imagepipeline-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource ARN, such as `arn:aws:imagebuilder:us-west-2:123456789012:image-pipeline/mywindows2016pipeline`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-imagebuilder-imagepipeline-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-imagebuilder-imagepipeline-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Returns the Amazon Resource Name \(ARN\) of the image pipeline\. For example, `arn:aws:imagebuilder:us-west-2:123456789012:image-pipeline/mywindows2016pipeline`\.

## Examples<a name="aws-resource-imagebuilder-imagepipeline--examples"></a>



### Create an image pipeline<a name="aws-resource-imagebuilder-imagepipeline--examples--Create_an_image_pipeline"></a>

The following example shows the schema for all of the parameters of the ImagePipeline resource document in both YAML and JSON format \.

#### YAML<a name="aws-resource-imagebuilder-imagepipeline--examples--Create_an_image_pipeline--yaml"></a>

```
Resources:
  ImagePipelineAllParameters:
    Type: 'AWS::ImageBuilder::ImagePipeline'
    Properties:
      Name: 'image-pipeline-name'
      Description: 'description'
      ImageRecipeArn: !Ref ImageRecipeArn
      InfrastructureConfigurationArn: !Ref InfrastructureConfigurationArn
      DistributionConfigurationArn: !Ref DistributionConfigurationArn
      ImageTestsConfiguration:
        ImageTestsEnabled: false
        TimeoutMinutes: 90
      Schedule:
        ScheduleExpression: 'cron(0 0 * * 0)'
        PipelineExecutionStartCondition: 'EXPRESSION_MATCH_ONLY'
      Status: 'DISABLED'
      Tags:
        CustomerImagePipelineTagKey1: 'CustomerImagePipelineTagValue1'
        CustomerImagePipelineTagKey2: 'CustomerImagePipelineTagValue2'
```

#### JSON<a name="aws-resource-imagebuilder-imagepipeline--examples--Create_an_image_pipeline--json"></a>

```
{
    "Resources": {
        "ImagePipelineAllParameters": {
            "Type": "AWS::ImageBuilder::ImagePipeline",
            "Properties": {
                "Name": "image-pipeline-name",
                "Description": "description",
                "ImageRecipeArn": {
                    "Ref": "ImageRecipeArn"
                },
                "InfrastructureConfigurationArn": {
                    "Ref": "InfrastructureConfigurationArn"
                },
                "DistributionConfigurationArn": {
                    "Ref": "DistributionConfigurationArn"
                },
                "ImageTestsConfiguration": {
                    "ImageTestsEnabled": false,
                    "TimeoutMinutes": 90
                },
                "Schedule": {
                    "ScheduleExpression": "cron(0 0 * * 0)",
                    "PipelineExecutionStartCondition": "EXPRESSION_MATCH_ONLY"
                },
                "Status": "DISABLED",
                "Tags": {
                    "CustomerImagePipelineTagKey1": "CustomerImagePipelineTagValue1",
                    "CustomerImagePipelineTagKey2": "CustomerImagePipelineTagValue2"
                }
            }
        }
    }
}
```