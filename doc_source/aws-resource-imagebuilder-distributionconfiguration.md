# AWS::ImageBuilder::DistributionConfiguration<a name="aws-resource-imagebuilder-distributionconfiguration"></a>

A distribution configuration allows you to specify the name and description of your output AMI, authorize other AWS accounts to launch the AMI, and replicate the AMI to other AWS Regions\. It also allows you to export the AMI to Amazon S3\.

## Syntax<a name="aws-resource-imagebuilder-distributionconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-imagebuilder-distributionconfiguration-syntax.json"></a>

```
{
  "Type" : "AWS::ImageBuilder::DistributionConfiguration",
  "Properties" : {
      "[Description](#cfn-imagebuilder-distributionconfiguration-description)" : String,
      "[Distributions](#cfn-imagebuilder-distributionconfiguration-distributions)" : [ Distribution, ... ],
      "[Name](#cfn-imagebuilder-distributionconfiguration-name)" : String,
      "[Tags](#cfn-imagebuilder-distributionconfiguration-tags)" : {Key : Value, ...}
    }
}
```

### YAML<a name="aws-resource-imagebuilder-distributionconfiguration-syntax.yaml"></a>

```
Type: AWS::ImageBuilder::DistributionConfiguration
Properties: 
  [Description](#cfn-imagebuilder-distributionconfiguration-description): String
  [Distributions](#cfn-imagebuilder-distributionconfiguration-distributions): 
    - Distribution
  [Name](#cfn-imagebuilder-distributionconfiguration-name): String
  [Tags](#cfn-imagebuilder-distributionconfiguration-tags): 
    Key : Value
```

## Properties<a name="aws-resource-imagebuilder-distributionconfiguration-properties"></a>

`Description`  <a name="cfn-imagebuilder-distributionconfiguration-description"></a>
The description of this distribution configuration\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Distributions`  <a name="cfn-imagebuilder-distributionconfiguration-distributions"></a>
The distributions of this distribution configuration formatted as an array of Distribution objects\.  
*Required*: Yes  
*Type*: List of [Distribution](aws-properties-imagebuilder-distributionconfiguration-distribution.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-imagebuilder-distributionconfiguration-name"></a>
The name of this distribution configuration\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `^[-_A-Za-z-0-9][-_A-Za-z0-9 ]{1,126}[-_A-Za-z-0-9]$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-imagebuilder-distributionconfiguration-tags"></a>
The tags of this distribution configuration\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-imagebuilder-distributionconfiguration-return-values"></a>

### Ref<a name="aws-resource-imagebuilder-distributionconfiguration-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Amazon Resource Name \(ARN\) of the resource, such as `arn:aws:imagebuilder:us-west-2:123456789012:distribution-configuration/myexampledistribution`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-imagebuilder-distributionconfiguration-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-imagebuilder-distributionconfiguration-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Returns the Amazon Resource Name \(ARN\) of this distribution configuration\. The following pattern is applied: `^arn:aws[^:]*:imagebuilder:[^:]+:(?:\d{12}|aws):(?:image-recipe|infrastructure-configuration|distribution-configuration|component|image|image-pipeline)/[a-z0-9-_]+(?:/(?:(?:x|\d+)\.(?:x|\d+)\.(?:x|\d+))(?:/\d+)?)?$`\.

`Name`  <a name="Name-fn::getatt"></a>
Returns the name of the distribution configuration\.

## Examples<a name="aws-resource-imagebuilder-distributionconfiguration--examples"></a>



### Create a distribution configuration resource for an AMI<a name="aws-resource-imagebuilder-distributionconfiguration--examples--Create_a_distribution_configuration_resource_for_an_AMI"></a>

The following example shows the schema for a DistributionConfiguration resource document for an AMI that is shared using launch permissions, presented in both YAML and JSON\.

#### YAML<a name="aws-resource-imagebuilder-distributionconfiguration--examples--Create_a_distribution_configuration_resource_for_an_AMI--yaml"></a>

```
Resources:
  DistributionConfigurationAllParameters:
    Type: 'AWS::ImageBuilder::DistributionConfiguration'
    Properties:
      Name: 'distribution-configuration-name'
      Description: 'description'
      Distributions:
        - Region: 'us-west-2'
          AmiDistributionConfiguration:
            Name: 'ami-dist-config-name-1 {{ imagebuilder:buildDate }}'
            Description: 'Set launch permissions and specify a license configuration for destination Region.'
            AmiTags:
              AmiTagKey: 'ami-tag-key'
            LaunchPermissionConfiguration:
              UserGroups:
                - 'ExampleGroup1'
                - 'ExampleGroup2'
              UserIds:
                - '123123123123' # Example user Id A
                - '321321321321' # Example user Id B
          LicenseConfigurationArns:
            - 'example-license-configuration-arn'
        - Region: 'us-east-1'
          AmiDistributionConfiguration:
            Name: 'ami-dist-config-name-2 {{ imagebuilder:buildDate }}'
            Description: 'Distribute a copy of the AMI to specified target accounts.'
            TargetAccountIds:
              - '111122223333'
              - '444455556666'
        - Region: 'us-east-2'
          AmiDistributionConfiguration:
            Name: 'ami-dist-config-name-3 {{ imagebuilder:buildDate }}'
            Description: 'Distribute to orgs and OUs.'
            AmiTags:
              auto-delete: 'no'
            LaunchPermissionConfiguration:
              OrganizationArns:
                - 'arn:aws:organizations::123456789012:organization/o-myorganization123'
              OrganizationalUnitArns:
                - 'arn:aws:organizations::123456789012:ou/o-123example/ou-1234-myorganizationalunit'
          
    Tags:
      CustomerDistributionConfigTagKey1: 'CustomerDistributionConfigTagValue1'
      CustomerDistributionConfigTagKey2: 'CustomerDistributionConfigTagValue2'
```

#### JSON<a name="aws-resource-imagebuilder-distributionconfiguration--examples--Create_a_distribution_configuration_resource_for_an_AMI--json"></a>

```
{
    "Resources": {
        "DistributionConfigurationAllParameters": {
            "Type": "AWS::ImageBuilder::DistributionConfiguration",
            "Properties": {
                "Name": "distribution-configuration-name",
                "Description": "description",
                "Distributions": [
                    {
                        "Region": "us-west-2",
                        "AmiDistributionConfiguration": {
                            "Name": "ami-dist-config-name-1 {{ imagebuilder:buildDate }}",
                            "Description": "Set launch permissions and specify a license configuration for destination Region.",
                            "AmiTags": {
                                "AmiTagKey": "ami-tag-key"
                            },
                            "LaunchPermissionConfiguration": {
                                "UserGroups": [
                                    "ExampleGroup1",
                                    "ExampleGroup2"
                                ],
                                "UserIds": [
                                    "123123123123",
                                    "321321321321"
                                ]
                            }
                        },
                        "LicenseConfigurationArns": [
                            "example-license-configuration-arn"
                        ]
                    },
                    {
                        "Region": "us-east-1",
                        "AmiDistributionConfiguration": {
                            "Name": "ami-dist-config-name-2 {{ imagebuilder:buildDate }}",
                            "Description": "Distribute to specified target accounts.",
                            "TargetAccountIds": [
                                "111122223333",
                                "444455556666"
                            ]
                            
                        }
                    },
                    {
                        "Region": "us-east-2",
                        "AmiDistributionConfiguration": {
	                        "Name": "ami-dist-config-name-3 {{ imagebuilder:buildDate }}",
	                        "Description": "Distribute to orgs and OUs.",
	                        "AmiTags": {
	                            "auto-delete": "no"
	                        },
	                        "LaunchPermissionConfiguration": {
	                    	    "OrganizationArns": [
	                    	   	 "arn:aws:organizations::123456789012:organization/o-myorganization123"
		                        ],
		                        "OrganizationalUnitArns": [
		                       	 "arn:aws:organizations::123456789012:ou/o-123example/ou-1234-myorganizationalunit"
		                        ]
	                        }
                        
                        }
                    }
                ]
            },
            "Tags": {
                "CustomerDistributionConfigTagKey1": "CustomerDistributionConfigTagValue1",
                "CustomerDistributionConfigTagKey2": "CustomerDistributionConfigTagValue2"
            }
        }
    }
}
```

### Create a distribution configuration resource for a container image<a name="aws-resource-imagebuilder-distributionconfiguration--examples--Create_a_distribution_configuration_resource_for_a_container_image"></a>

The following example shows the schema for a DistributionConfiguration resource document for a container image that is distributed to two Regions, presented in both YAML and JSON\.

#### YAML<a name="aws-resource-imagebuilder-distributionconfiguration--examples--Create_a_distribution_configuration_resource_for_a_container_image--yaml"></a>

```
Resources:
  DistributionConfigurationAllParameters:
    Type: 'AWS::ImageBuilder::DistributionConfiguration'
    Properties:
      Name: 'distribution-configuration-all-parameters'
      Description: 'Set target repository and container tags for container distribution to two Regions.'
      Distributions:
        - Region: 'us-west-2'
          ContainerDistributionConfiguration:
            Description: 'test distribution cfn template'
            TargetRepository:
              Service: ECR
              RepositoryName: 'cfn-test'
            ContainerTags:
              - 'Tag1'
              - 'Tag2'
        - Region: 'us-east-1'
          ContainerDistributionConfiguration:
            Description: 'test distribution cfn template'
            TargetRepository:
              Service: ECR
              RepositoryName: 'cfn-test'
            ContainerTags:
              - 'Tag1'
              - 'Tag2'      
    Tags:
      DistributionConfigurationTestTagKey1: 'DistributionConfigurationTestTagValue1'
      DistributionConfigurationTestTagKey2: 'DistributionConfigurationTestTagValue2'
```

#### JSON<a name="aws-resource-imagebuilder-distributionconfiguration--examples--Create_a_distribution_configuration_resource_for_a_container_image--json"></a>

```
{
    "Resources": {
        "DistributionConfigurationAllParameters": {
            "Type": "AWS::ImageBuilder::DistributionConfiguration",
            "Properties": {
                "Name": "distribution-configuration-name",
                "Description": "Set target repository and container tags for container distribution to two Regions.",
                "Distributions": [
                    {
                        "Region": "us-west-2",
                        "ContainerDistributionConfiguration": {
                            "Description": "description",
                            "TargetRepository": {
                                "Service": "ECR",
                                "RepositoryName": "cfn-test"
                            },
                            "ContainerTags": ["Tag1", "Tag2"]
                        }
                    },
                    {
                        "Region": "us-east-1",
                        "ContainerDistributionConfiguration": {
                            "Description": "description",
                            "TargetRepository": {
                                "Service": "ECR",
                                "RepositoryName": "cfn-test"
                            },
                           "ContainerTags": ["Tag1", "Tag2"]
                        }
                    }
                ]
            },
            "Tags": {
   			"DistributionConfigurationTestTagKey1": "DistributionConfigurationTestTagValue1",
   			"DistributionConfigurationTestTagKey2": "DistributionConfigurationTestTagValue2"
            }
        }
    }
}
```

## See also<a name="aws-resource-imagebuilder-distributionconfiguration--seealso"></a>
+ [Create a distribution configuration](https://docs.aws.amazon.com/imagebuilder/latest/userguide/managing-image-builder-cli.html#image-builder-cli-create-distribution-configuration) in the *Image Builder User Guide*\.

