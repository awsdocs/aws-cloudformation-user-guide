# Amazon AppStream 2\.0 Stack StorageConnector<a name="aws-properties-appstream-stack-storageconnector"></a>

<a name="aws-properties-appstream-stack-storageconnector-description"></a>The `StorageConnector` property type specifies a connector to enable persistent storage for users of an Amazon AppStream 2\.0 stack\.

<a name="aws-properties-appstream-stack-storageconnector-inheritance"></a> `StorageConnector` is a property of the [AWS::AppStream::Stack](aws-resource-appstream-stack.md) resource\.

## Syntax<a name="aws-properties-appstream-stack-storageconnector-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appstream-stack-storageconnector-syntax.json"></a>

```
{
  "[ConnectorType](#cfn-appstream-stack-storageconnector-connectortype)" : String,
  "[Domains](#cfn-appstream-stack-storageconnector-domains)" : [ String, ... ],
  "[ResourceIdentifier](#cfn-appstream-stack-storageconnector-resourceidentifier)" : String
}
```

### YAML<a name="aws-properties-appstream-stack-storageconnector-syntax.yaml"></a>

```
[ConnectorType](#cfn-appstream-stack-storageconnector-connectortype): String
[Domains](#cfn-appstream-stack-storageconnector-domains): 
  - String
[ResourceIdentifier](#cfn-appstream-stack-storageconnector-resourceidentifier): String
```

## Properties<a name="aws-properties-appstream-stack-storageconnector-properties"></a>

`ConnectorType`  <a name="cfn-appstream-stack-storageconnector-connectortype"></a>
The type of storage connector\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Domains`  <a name="cfn-appstream-stack-storageconnector-domains"></a>
The names of the domains for the account\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ResourceIdentifier`  <a name="cfn-appstream-stack-storageconnector-resourceidentifier"></a>
The ARN of the storage connector\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 