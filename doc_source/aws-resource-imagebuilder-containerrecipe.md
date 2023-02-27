# AWS::ImageBuilder::ContainerRecipe<a name="aws-resource-imagebuilder-containerrecipe"></a>

Creates a new container recipe\. Container recipes define how images are configured, tested, and assessed\.

## Syntax<a name="aws-resource-imagebuilder-containerrecipe-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-imagebuilder-containerrecipe-syntax.json"></a>

```
{
  "Type" : "AWS::ImageBuilder::ContainerRecipe",
  "Properties" : {
      "[Components](#cfn-imagebuilder-containerrecipe-components)" : [ ComponentConfiguration, ... ],
      "[ContainerType](#cfn-imagebuilder-containerrecipe-containertype)" : String,
      "[Description](#cfn-imagebuilder-containerrecipe-description)" : String,
      "[DockerfileTemplateData](#cfn-imagebuilder-containerrecipe-dockerfiletemplatedata)" : String,
      "[DockerfileTemplateUri](#cfn-imagebuilder-containerrecipe-dockerfiletemplateuri)" : String,
      "[ImageOsVersionOverride](#cfn-imagebuilder-containerrecipe-imageosversionoverride)" : String,
      "[InstanceConfiguration](#cfn-imagebuilder-containerrecipe-instanceconfiguration)" : InstanceConfiguration,
      "[KmsKeyId](#cfn-imagebuilder-containerrecipe-kmskeyid)" : String,
      "[Name](#cfn-imagebuilder-containerrecipe-name)" : String,
      "[ParentImage](#cfn-imagebuilder-containerrecipe-parentimage)" : String,
      "[PlatformOverride](#cfn-imagebuilder-containerrecipe-platformoverride)" : String,
      "[Tags](#cfn-imagebuilder-containerrecipe-tags)" : {Key : Value, ...},
      "[TargetRepository](#cfn-imagebuilder-containerrecipe-targetrepository)" : TargetContainerRepository,
      "[Version](#cfn-imagebuilder-containerrecipe-version)" : String,
      "[WorkingDirectory](#cfn-imagebuilder-containerrecipe-workingdirectory)" : String
    }
}
```

### YAML<a name="aws-resource-imagebuilder-containerrecipe-syntax.yaml"></a>

```
Type: AWS::ImageBuilder::ContainerRecipe
Properties: 
  [Components](#cfn-imagebuilder-containerrecipe-components): 
    - ComponentConfiguration
  [ContainerType](#cfn-imagebuilder-containerrecipe-containertype): String
  [Description](#cfn-imagebuilder-containerrecipe-description): String
  [DockerfileTemplateData](#cfn-imagebuilder-containerrecipe-dockerfiletemplatedata): String
  [DockerfileTemplateUri](#cfn-imagebuilder-containerrecipe-dockerfiletemplateuri): String
  [ImageOsVersionOverride](#cfn-imagebuilder-containerrecipe-imageosversionoverride): String
  [InstanceConfiguration](#cfn-imagebuilder-containerrecipe-instanceconfiguration): 
    InstanceConfiguration
  [KmsKeyId](#cfn-imagebuilder-containerrecipe-kmskeyid): String
  [Name](#cfn-imagebuilder-containerrecipe-name): String
  [ParentImage](#cfn-imagebuilder-containerrecipe-parentimage): String
  [PlatformOverride](#cfn-imagebuilder-containerrecipe-platformoverride): String
  [Tags](#cfn-imagebuilder-containerrecipe-tags): 
    Key : Value
  [TargetRepository](#cfn-imagebuilder-containerrecipe-targetrepository): 
    TargetContainerRepository
  [Version](#cfn-imagebuilder-containerrecipe-version): String
  [WorkingDirectory](#cfn-imagebuilder-containerrecipe-workingdirectory): String
```

## Properties<a name="aws-resource-imagebuilder-containerrecipe-properties"></a>

`Components`  <a name="cfn-imagebuilder-containerrecipe-components"></a>
Build and test components that are included in the container recipe\. Recipes require a minimum of one build component, and can have a maximum of 20 build and test components in any combination\.  
*Required*: Yes  
*Type*: List of [ComponentConfiguration](aws-properties-imagebuilder-containerrecipe-componentconfiguration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ContainerType`  <a name="cfn-imagebuilder-containerrecipe-containertype"></a>
Specifies the type of container, such as Docker\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `DOCKER`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-imagebuilder-containerrecipe-description"></a>
The description of the container recipe\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DockerfileTemplateData`  <a name="cfn-imagebuilder-containerrecipe-dockerfiletemplatedata"></a>
Dockerfiles are text documents that are used to build Docker containers, and ensure that they contain all of the elements required by the application running inside\. The template data consists of contextual variables where Image Builder places build information or scripts, based on your container image recipe\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DockerfileTemplateUri`  <a name="cfn-imagebuilder-containerrecipe-dockerfiletemplateuri"></a>
The S3 URI for the Dockerfile that will be used to build your container image\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ImageOsVersionOverride`  <a name="cfn-imagebuilder-containerrecipe-imageosversionoverride"></a>
Specifies the operating system version for the base image\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InstanceConfiguration`  <a name="cfn-imagebuilder-containerrecipe-instanceconfiguration"></a>
A group of options that can be used to configure an instance for building and testing container images\.  
*Required*: No  
*Type*: [InstanceConfiguration](aws-properties-imagebuilder-containerrecipe-instanceconfiguration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KmsKeyId`  <a name="cfn-imagebuilder-containerrecipe-kmskeyid"></a>
Identifies which KMS key is used to encrypt the container image for distribution to the target Region\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-imagebuilder-containerrecipe-name"></a>
The name of the container recipe\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `^[-_A-Za-z-0-9][-_A-Za-z0-9 ]{1,126}[-_A-Za-z-0-9]$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ParentImage`  <a name="cfn-imagebuilder-containerrecipe-parentimage"></a>
The base image for the container recipe\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PlatformOverride`  <a name="cfn-imagebuilder-containerrecipe-platformoverride"></a>
Specifies the operating system platform when you use a custom base image\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-imagebuilder-containerrecipe-tags"></a>
Tags that are attached to the container recipe\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TargetRepository`  <a name="cfn-imagebuilder-containerrecipe-targetrepository"></a>
The destination repository for the container image\.  
*Required*: Yes  
*Type*: [TargetContainerRepository](aws-properties-imagebuilder-containerrecipe-targetcontainerrepository.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Version`  <a name="cfn-imagebuilder-containerrecipe-version"></a>
The semantic version of the container recipe\.  
The semantic version has four nodes: <major>\.<minor>\.<patch>/<build>\. You can assign values for the first three, and can filter on all of them\.  
 **Assignment:** For the first three nodes you can assign any positive integer value, including zero, with an upper limit of 2^30\-1, or 1073741823 for each node\. Image Builder automatically assigns the build number to the fourth node\.  
 **Patterns:** You can use any numeric pattern that adheres to the assignment requirements for the nodes that you can assign\. For example, you might choose a software version pattern, such as 1\.0\.0, or a date, such as 2021\.01\.01\.  
 **Filtering:** With semantic versioning, you have the flexibility to use wildcards \(x\) to specify the most recent versions or nodes when selecting the base image or components for your recipe\. When you use a wildcard in any node, all nodes to the right of the first wildcard must also be wildcards\.
*Required*: Yes  
*Type*: String  
*Pattern*: `^[0-9]+\.[0-9]+\.[0-9]+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`WorkingDirectory`  <a name="cfn-imagebuilder-containerrecipe-workingdirectory"></a>
The working directory for use during build and test workflows\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-imagebuilder-containerrecipe-return-values"></a>

### Ref<a name="aws-resource-imagebuilder-containerrecipe-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource ARN, such as `arn:aws:imagebuilder:us-east-1:123456789012:container-recipe/mybasicrecipe/2020.12.17`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-imagebuilder-containerrecipe-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-imagebuilder-containerrecipe-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Returns the Amazon Resource Name \(ARN\) of the container recipe\. For example, `arn:aws:imagebuilder:us-east-1:123456789012:container-recipe/mybasicrecipe/2020.12.17`\.

`Name`  <a name="Name-fn::getatt"></a>
Returns the name of the container recipe\.

## Examples<a name="aws-resource-imagebuilder-containerrecipe--examples"></a>



### Create a container recipe\.<a name="aws-resource-imagebuilder-containerrecipe--examples--Create_a_container_recipe."></a>

The following example shows the schema for the ContainerRecipe resource document in both YAML and JSON format\.

#### YAML<a name="aws-resource-imagebuilder-containerrecipe--examples--Create_a_container_recipe.--yaml"></a>

```
Resources:
   ContainerRecipeAllParameters:
      Type: 'AWS::ImageBuilder::ContainerRecipe'
      Properties:
         Name: 'container-recipe-name'
         Version: '1.0.0'
         ParentImage: !Ref ParentImage
         Description: 'description'
         ContainerType: 'DOCKER'
         Components:
            - ComponentArn: !Ref ComponentArn
            - ComponentArn: !Ref AnotherComponentArn
         TargetRepository:
            Service: 'ECR'
            RepositoryName: !Ref RepositoryName
         DockerfileTemplateData: |
           FROM {{{ imagebuilder:parentImage }}}
           {{{ imagebuilder:environments }}}
           {{{ imagebuilder:components }}}
         WorkingDirectory: "dummy-working-directory"
         KmsKeyId: !Ref KmsKeyId
         Tags:
            Usage: 'Documentation'
   
Outputs:
   OutputContainerRecipeArn:
      Value:
         'Fn::GetAtt':
            - ContainerRecipeAllParameters
            - Arn
```

#### JSON<a name="aws-resource-imagebuilder-containerrecipe--examples--Create_a_container_recipe.--json"></a>

```
{
   "Resources": {
      "ContainerRecipeAllParameters": {
         "Type": "AWS::ImageBuilder::ContainerRecipe",
         "Properties": {
            "Name": "container-recipe-name",
            "Version": "1.0.0",
            "ParentImage": {
               "Ref": "ParentImage"
            },
            "Description": "description",
            "ContainerType": "DOCKER",
            "Components": [
               {
                  "ComponentArn": {
                     "Ref": "ComponentArn"
                  }
               },
               {
                  "ComponentArn": {
                     "Ref": "AnotherComponentArn"
                  }
               }
            ],
            "TargetRepository": {
               "Service": "ECR",
               "RepositoryName": {
                  "Ref": "RepositoryName"
               },
            },
            "DockerfileTemplateData": "FROM {{{ imagebuilder:parentImage }}}\n{{{ imagebuilder:environments }}}\n{{{ imagebuilder:components }}}\n",
            "WorkingDirectory": "dummy-working-directory",
            "KmsKeyId": {
               "Ref": "KmsKeyId"
            },
            "Tags": {
               "Usage": "Documentation"
            }
         }
      }
   },
   "Outputs": {
      "OutputContainerRecipeArn": {
         "Value": {
            "Fn::GetAtt": [
               "ContainerRecipeAllParameters",
               "Arn"
            ]
         }
      }
   }
}
```