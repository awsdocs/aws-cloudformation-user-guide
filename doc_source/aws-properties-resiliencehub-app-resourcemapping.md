# AWS::ResilienceHub::App ResourceMapping<a name="aws-properties-resiliencehub-app-resourcemapping"></a>

Defines a resource mapping\.

## Syntax<a name="aws-properties-resiliencehub-app-resourcemapping-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-resiliencehub-app-resourcemapping-syntax.json"></a>

```
{
  "[LogicalStackName](#cfn-resiliencehub-app-resourcemapping-logicalstackname)" : String,
  "[MappingType](#cfn-resiliencehub-app-resourcemapping-mappingtype)" : String,
  "[PhysicalResourceId](#cfn-resiliencehub-app-resourcemapping-physicalresourceid)" : PhysicalResourceId,
  "[ResourceName](#cfn-resiliencehub-app-resourcemapping-resourcename)" : String,
  "[TerraformSourceName](#cfn-resiliencehub-app-resourcemapping-terraformsourcename)" : String
}
```

### YAML<a name="aws-properties-resiliencehub-app-resourcemapping-syntax.yaml"></a>

```
  [LogicalStackName](#cfn-resiliencehub-app-resourcemapping-logicalstackname): String
  [MappingType](#cfn-resiliencehub-app-resourcemapping-mappingtype): String
  [PhysicalResourceId](#cfn-resiliencehub-app-resourcemapping-physicalresourceid): 
    PhysicalResourceId
  [ResourceName](#cfn-resiliencehub-app-resourcemapping-resourcename): String
  [TerraformSourceName](#cfn-resiliencehub-app-resourcemapping-terraformsourcename): String
```

## Properties<a name="aws-properties-resiliencehub-app-resourcemapping-properties"></a>

`LogicalStackName`  <a name="cfn-resiliencehub-app-resourcemapping-logicalstackname"></a>
The name of the CloudFormation stack this resource is mapped to\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MappingType`  <a name="cfn-resiliencehub-app-resourcemapping-mappingtype"></a>
Specifies the type of resource mapping\.  
Valid Values: CfnStack \| Resource \| AppRegistryApp \| ResourceGroup \| Terraform    
AppRegistryApp  
The resource is mapped to another application\. The name of the application is contained in the `appRegistryAppName` property\.  
CfnStack  
The resource is mapped to a CloudFormation stack\. The name of the CloudFormation stack is contained in the `logicalStackName` property\.  
Resource  
The resource is mapped to another resource\. The name of the resource is contained in the `resourceName` property\.  
ResourceGroup  
The resource is mapped to a resource group\. The name of the resource group is contained in the `resourceGroupName` property\.
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PhysicalResourceId`  <a name="cfn-resiliencehub-app-resourcemapping-physicalresourceid"></a>
The identifier of this resource\.  
*Required*: Yes  
*Type*: [PhysicalResourceId](aws-properties-resiliencehub-app-physicalresourceid.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceName`  <a name="cfn-resiliencehub-app-resourcemapping-resourcename"></a>
The name of the resource this resource is mapped to\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TerraformSourceName`  <a name="cfn-resiliencehub-app-resourcemapping-terraformsourcename"></a>
 The short name of the Terraform source\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)