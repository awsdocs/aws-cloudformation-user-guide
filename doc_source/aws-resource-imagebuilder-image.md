# AWS::ImageBuilder::Image<a name="aws-resource-imagebuilder-image"></a>

An image build version\. An image is a customized, secure, and up\-to\-date “golden” server image that is pre\-installed and pre\-configured with software and settings to meet specific IT standards\.

## Syntax<a name="aws-resource-imagebuilder-image-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-imagebuilder-image-syntax.json"></a>

```
{
  "Type" : "AWS::ImageBuilder::Image",
  "Properties" : {
      "[DistributionConfigurationArn](#cfn-imagebuilder-image-distributionconfigurationarn)" : String,
      "[EnhancedImageMetadataEnabled](#cfn-imagebuilder-image-enhancedimagemetadataenabled)" : Boolean,
      "[ImageRecipeArn](#cfn-imagebuilder-image-imagerecipearn)" : String,
      "[ImageTestsConfiguration](#cfn-imagebuilder-image-imagetestsconfiguration)" : ImageTestsConfiguration,
      "[InfrastructureConfigurationArn](#cfn-imagebuilder-image-infrastructureconfigurationarn)" : String,
      "[Tags](#cfn-imagebuilder-image-tags)" : {Key : Value, ...}
    }
}
```

### YAML<a name="aws-resource-imagebuilder-image-syntax.yaml"></a>

```
Type: AWS::ImageBuilder::Image
Properties: 
  [DistributionConfigurationArn](#cfn-imagebuilder-image-distributionconfigurationarn): String
  [EnhancedImageMetadataEnabled](#cfn-imagebuilder-image-enhancedimagemetadataenabled): Boolean
  [ImageRecipeArn](#cfn-imagebuilder-image-imagerecipearn): String
  [ImageTestsConfiguration](#cfn-imagebuilder-image-imagetestsconfiguration): 
    ImageTestsConfiguration
  [InfrastructureConfigurationArn](#cfn-imagebuilder-image-infrastructureconfigurationarn): String
  [Tags](#cfn-imagebuilder-image-tags): 
    Key : Value
```

## Properties<a name="aws-resource-imagebuilder-image-properties"></a>

`DistributionConfigurationArn`  <a name="cfn-imagebuilder-image-distributionconfigurationarn"></a>
The Amazon Resource Name \(ARN\) of the distribution configuration\.  
*Required*: No  
*Type*: String  
*Pattern*: `^arn:aws[^:]*:imagebuilder:[^:]+:(?:\d{12}|aws):(?:image-recipe|container-recipe|infrastructure-configuration|distribution-configuration|component|image|image-pipeline)/[a-z0-9-_]+(?:/(?:(?:x|\d+)\.(?:x|\d+)\.(?:x|\d+))(?:/\d+)?)?$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EnhancedImageMetadataEnabled`  <a name="cfn-imagebuilder-image-enhancedimagemetadataenabled"></a>
 Collects additional information about the image being created, including the operating system \(OS\) version and package list\. This information is used to enhance the overall experience of using EC2 Image Builder\. Enabled by default\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ImageRecipeArn`  <a name="cfn-imagebuilder-image-imagerecipearn"></a>
The Amazon Resource Name \(ARN\) of the image recipe\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `^arn:aws[^:]*:imagebuilder:[^:]+:(?:\d{12}|aws):(?:image-recipe|container-recipe|infrastructure-configuration|distribution-configuration|component|image|image-pipeline)/[a-z0-9-_]+(?:/(?:(?:x|\d+)\.(?:x|\d+)\.(?:x|\d+))(?:/\d+)?)?$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ImageTestsConfiguration`  <a name="cfn-imagebuilder-image-imagetestsconfiguration"></a>
The configuration of the image tests used when creating this image\.  
*Required*: No  
*Type*: [ImageTestsConfiguration](aws-properties-imagebuilder-image-imagetestsconfiguration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InfrastructureConfigurationArn`  <a name="cfn-imagebuilder-image-infrastructureconfigurationarn"></a>
The Amazon Resource Name \(ARN\) of the infrastructure configuration used to create this image\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `^arn:aws[^:]*:imagebuilder:[^:]+:(?:\d{12}|aws):(?:image-recipe|container-recipe|infrastructure-configuration|distribution-configuration|component|image|image-pipeline)/[a-z0-9-_]+(?:/(?:(?:x|\d+)\.(?:x|\d+)\.(?:x|\d+))(?:/\d+)?)?$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-imagebuilder-image-tags"></a>
The tags of the image\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-imagebuilder-image-return-values"></a>

### Ref<a name="aws-resource-imagebuilder-image-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource ARN, such as `arn:aws:imagebuilder:us-west-2:123456789012:image/my-example-image`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-imagebuilder-image-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-imagebuilder-image-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Returns the Amazon Resource Name \(ARN\) of the image\. For example, `arn:aws:imagebuilder:us-west-2:123456789012:image/mybasicrecipe/2019.12.03/1`\.

`ImageId`  <a name="ImageId-fn::getatt"></a>
Returns the AMI ID of the EC2 AMI in the Region in which you are using Image Builder\.

`Name`  <a name="Name-fn::getatt"></a>
Returns the name of the image\.

## Examples<a name="aws-resource-imagebuilder-image--examples"></a>



### Create an image<a name="aws-resource-imagebuilder-image--examples--Create_an_image"></a>

The following example shows the schema for all of the parameters of the Image resource document in both YAML and JSON format \.

#### YAML<a name="aws-resource-imagebuilder-image--examples--Create_an_image--yaml"></a>

```
Resources:
  ImageAllParameters:
    Type: 'AWS::ImageBuilder::Image'
    Properties:
      ImageRecipeArn: !Ref ImageRecipeArn
      InfrastructureConfigurationArn: !Ref InfrastructureConfigurationArn
      DistributionConfigurationArn: !Ref DistributionConfigurationArn
      ImageTestsConfiguration:
        ImageTestsEnabled: false
        TimeoutMinutes: 60
      Tags:
        CustomerImageTagKey1: 'CustomerImageTagValue1'
        CustomerImageTagKey2: 'CustomerImageTagValue2'
```

#### JSON<a name="aws-resource-imagebuilder-image--examples--Create_an_image--json"></a>

```
{
    "Resources": {
        "ImageAllParameters": {
            "Type": "AWS::ImageBuilder::Image",
            "Properties": {
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
                    "TimeoutMinutes": 60
                },
                "Tags": {
                    "CustomerImageTagKey1": "CustomerImageTagValue1",
                    "CustomerImageTagKey2": "CustomerImageTagValue2"
                }
            }
        }
    }
}
```