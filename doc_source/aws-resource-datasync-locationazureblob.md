# AWS::DataSync::LocationAzureBlob<a name="aws-resource-datasync-locationazureblob"></a>

Creates an endpoint for a Microsoft Azure Blob Storage container that AWS DataSync can use as a transfer source or destination\.

Before you begin, make sure you know [how DataSync accesses Azure Blob Storage](https://docs.aws.amazon.com/datasync/latest/userguide/creating-azure-blob-location.html#azure-blob-access) and works with [access tiers](https://docs.aws.amazon.com/datasync/latest/userguide/creating-azure-blob-location.html#azure-blob-access-tiers) and [blob types](https://docs.aws.amazon.com/datasync/latest/userguide/creating-azure-blob-location.html#blob-types)\. You also need a [DataSync agent](https://docs.aws.amazon.com/datasync/latest/userguide/creating-azure-blob-location.html#azure-blob-creating-agent) that can connect to your container\.

## Syntax<a name="aws-resource-datasync-locationazureblob-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-datasync-locationazureblob-syntax.json"></a>

```
{
  "Type" : "AWS::DataSync::LocationAzureBlob",
  "Properties" : {
      "[AgentArns](#cfn-datasync-locationazureblob-agentarns)" : [ String, ... ],
      "[AzureAccessTier](#cfn-datasync-locationazureblob-azureaccesstier)" : String,
      "[AzureBlobAuthenticationType](#cfn-datasync-locationazureblob-azureblobauthenticationtype)" : String,
      "[AzureBlobContainerUrl](#cfn-datasync-locationazureblob-azureblobcontainerurl)" : String,
      "[AzureBlobSasConfiguration](#cfn-datasync-locationazureblob-azureblobsasconfiguration)" : AzureBlobSasConfiguration,
      "[AzureBlobType](#cfn-datasync-locationazureblob-azureblobtype)" : String,
      "[Subdirectory](#cfn-datasync-locationazureblob-subdirectory)" : String,
      "[Tags](#cfn-datasync-locationazureblob-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-datasync-locationazureblob-syntax.yaml"></a>

```
Type: AWS::DataSync::LocationAzureBlob
Properties: 
  [AgentArns](#cfn-datasync-locationazureblob-agentarns): 
    - String
  [AzureAccessTier](#cfn-datasync-locationazureblob-azureaccesstier): String
  [AzureBlobAuthenticationType](#cfn-datasync-locationazureblob-azureblobauthenticationtype): String
  [AzureBlobContainerUrl](#cfn-datasync-locationazureblob-azureblobcontainerurl): String
  [AzureBlobSasConfiguration](#cfn-datasync-locationazureblob-azureblobsasconfiguration): 
    AzureBlobSasConfiguration
  [AzureBlobType](#cfn-datasync-locationazureblob-azureblobtype): String
  [Subdirectory](#cfn-datasync-locationazureblob-subdirectory): String
  [Tags](#cfn-datasync-locationazureblob-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-datasync-locationazureblob-properties"></a>

`AgentArns`  <a name="cfn-datasync-locationazureblob-agentarns"></a>
Specifies the Amazon Resource Name \(ARN\) of the DataSync agent that can connect with your Azure Blob Storage container\.  
You can specify more than one agent\. For more information, see [Using multiple agents for your transfer](https://docs.aws.amazon.com/datasync/latest/userguide/multiple-agents.html)\.  
*Required*: Yes  
*Type*: List of String  
*Maximum*: `4`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AzureAccessTier`  <a name="cfn-datasync-locationazureblob-azureaccesstier"></a>
Specifies the access tier that you want your objects or files transferred into\. This only applies when using the location as a transfer destination\. For more information, see [Access tiers](https://docs.aws.amazon.com/datasync/latest/userguide/creating-azure-blob-location.html#azure-blob-access-tiers)\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ARCHIVE | COOL | HOT`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AzureBlobAuthenticationType`  <a name="cfn-datasync-locationazureblob-azureblobauthenticationtype"></a>
Specifies the authentication method DataSync uses to access your Azure Blob Storage\. DataSync can access blob storage using a shared access signature \(SAS\)\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `SAS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AzureBlobContainerUrl`  <a name="cfn-datasync-locationazureblob-azureblobcontainerurl"></a>
Specifies the URL of the Azure Blob Storage container involved in your transfer\.  
*Required*: No  
*Type*: String  
*Maximum*: `325`  
*Pattern*: `^https:\/\/[A-Za-z0-9]((\.|-+)?[A-Za-z0-9]){0,252}\/[a-z0-9](-?[a-z0-9]){2,62}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`AzureBlobSasConfiguration`  <a name="cfn-datasync-locationazureblob-azureblobsasconfiguration"></a>
Specifies the SAS configuration that allows DataSync to access your Azure Blob Storage\.  
*Required*: No  
*Type*: [AzureBlobSasConfiguration](aws-properties-datasync-locationazureblob-azureblobsasconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AzureBlobType`  <a name="cfn-datasync-locationazureblob-azureblobtype"></a>
Specifies the type of blob that you want your objects or files to be when transferring them into Azure Blob Storage\. Currently, DataSync only supports moving data into Azure Blob Storage as block blobs\. For more information on blob types, see the [Azure Blob Storage documentation](https://learn.microsoft.com/en-us/rest/api/storageservices/understanding-block-blobs--append-blobs--and-page-blobs)\.  
*Required*: No  
*Type*: String  
*Allowed values*: `BLOCK`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Subdirectory`  <a name="cfn-datasync-locationazureblob-subdirectory"></a>
Specifies path segments if you want to limit your transfer to a virtual directory in your container \(for example, `/my/images`\)\.  
*Required*: No  
*Type*: String  
*Maximum*: `1024`  
*Pattern*: `^[\p{L}\p{M}\p{Z}\p{S}\p{N}\p{P}\p{C}]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-datasync-locationazureblob-tags"></a>
Specifies labels that help you categorize, filter, and search for your AWS resources\. We recommend creating at least a name tag for your transfer location\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-datasync-locationazureblob-return-values"></a>

### Ref<a name="aws-resource-datasync-locationazureblob-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the location resource ARN\. For example:

 `arn:aws:datasync:us-east-2:111222333444:location/loc-07db7abfc326c50s3` 

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-datasync-locationazureblob-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-datasync-locationazureblob-return-values-fn--getatt-fn--getatt"></a>

`LocationArn`  <a name="LocationArn-fn::getatt"></a>
The ARN of the Azure Blob Storage transfer location that you created\.

`LocationUri`  <a name="LocationUri-fn::getatt"></a>
The URI of the Azure Blob Storage transfer location that you created\.