# AWS::OpenSearchService::Domain SoftwareUpdateOptions<a name="aws-properties-opensearchservice-domain-softwareupdateoptions"></a>

Options for configuring service software updates for a domain\.

## Syntax<a name="aws-properties-opensearchservice-domain-softwareupdateoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-opensearchservice-domain-softwareupdateoptions-syntax.json"></a>

```
{
  "[AutoSoftwareUpdateEnabled](#cfn-opensearchservice-domain-softwareupdateoptions-autosoftwareupdateenabled)" : Boolean
}
```

### YAML<a name="aws-properties-opensearchservice-domain-softwareupdateoptions-syntax.yaml"></a>

```
  [AutoSoftwareUpdateEnabled](#cfn-opensearchservice-domain-softwareupdateoptions-autosoftwareupdateenabled): Boolean
```

## Properties<a name="aws-properties-opensearchservice-domain-softwareupdateoptions-properties"></a>

`AutoSoftwareUpdateEnabled`  <a name="cfn-opensearchservice-domain-softwareupdateoptions-autosoftwareupdateenabled"></a>
Specifies whether automatic service software updates are enabled for the domain\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)