# AWS::GreengrassV2::ComponentVersion ComponentDependencyRequirement<a name="aws-properties-greengrassv2-componentversion-componentdependencyrequirement"></a>

Contains information about a component dependency for a Lambda function component\.

## Syntax<a name="aws-properties-greengrassv2-componentversion-componentdependencyrequirement-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrassv2-componentversion-componentdependencyrequirement-syntax.json"></a>

```
{
  "[DependencyType](#cfn-greengrassv2-componentversion-componentdependencyrequirement-dependencytype)" : String,
  "[VersionRequirement](#cfn-greengrassv2-componentversion-componentdependencyrequirement-versionrequirement)" : String
}
```

### YAML<a name="aws-properties-greengrassv2-componentversion-componentdependencyrequirement-syntax.yaml"></a>

```
  [DependencyType](#cfn-greengrassv2-componentversion-componentdependencyrequirement-dependencytype): String
  [VersionRequirement](#cfn-greengrassv2-componentversion-componentdependencyrequirement-versionrequirement): String
```

## Properties<a name="aws-properties-greengrassv2-componentversion-componentdependencyrequirement-properties"></a>

`DependencyType`  <a name="cfn-greengrassv2-componentversion-componentdependencyrequirement-dependencytype"></a>
The type of this dependency\. Choose from the following options:  
+ `SOFT` – The component doesn't restart if the dependency changes state\.
+ `HARD` – The component restarts if the dependency changes state\.
Default: `HARD`  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VersionRequirement`  <a name="cfn-greengrassv2-componentversion-componentdependencyrequirement-versionrequirement"></a>
The component version requirement for the component dependency\.  
AWS IoT Greengrass uses semantic version constraints\. For more information, see [Semantic Versioning](https://semver.org/)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)