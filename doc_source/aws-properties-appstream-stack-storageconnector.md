# AWS::AppStream::Stack StorageConnector<a name="aws-properties-appstream-stack-storageconnector"></a>

A connector that enables persistent storage for users\.

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
*Allowed values*: `GOOGLE_DRIVE | HOMEFOLDERS | ONE_DRIVE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Domains`  <a name="cfn-appstream-stack-storageconnector-domains"></a>
The names of the domains for the account\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceIdentifier`  <a name="cfn-appstream-stack-storageconnector-resourceidentifier"></a>
The ARN of the storage connector\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)