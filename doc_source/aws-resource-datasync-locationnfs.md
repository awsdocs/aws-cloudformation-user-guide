# AWS::DataSync::LocationNFS<a name="aws-resource-datasync-locationnfs"></a>

The `AWS::DataSync::LocationNFS` resource specifies a file system on a Network File System \(NFS\) server that can be read from or written to\.

## Syntax<a name="aws-resource-datasync-locationnfs-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-datasync-locationnfs-syntax.json"></a>

```
{
  "Type" : "AWS::DataSync::LocationNFS",
  "Properties" : {
      "[MountOptions](#cfn-datasync-locationnfs-mountoptions)" : MountOptions,
      "[OnPremConfig](#cfn-datasync-locationnfs-onpremconfig)" : OnPremConfig,
      "[ServerHostname](#cfn-datasync-locationnfs-serverhostname)" : String,
      "[Subdirectory](#cfn-datasync-locationnfs-subdirectory)" : String,
      "[Tags](#cfn-datasync-locationnfs-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-datasync-locationnfs-syntax.yaml"></a>

```
Type: AWS::DataSync::LocationNFS
Properties: 
  [MountOptions](#cfn-datasync-locationnfs-mountoptions): 
    MountOptions
  [OnPremConfig](#cfn-datasync-locationnfs-onpremconfig): 
    OnPremConfig
  [ServerHostname](#cfn-datasync-locationnfs-serverhostname): String
  [Subdirectory](#cfn-datasync-locationnfs-subdirectory): String
  [Tags](#cfn-datasync-locationnfs-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-datasync-locationnfs-properties"></a>

`MountOptions`  <a name="cfn-datasync-locationnfs-mountoptions"></a>
Specifies the options that DataSync can use to mount your NFS file server\.  
*Required*: No  
*Type*: [MountOptions](aws-properties-datasync-locationnfs-mountoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OnPremConfig`  <a name="cfn-datasync-locationnfs-onpremconfig"></a>
Specifies the Amazon Resource Name \(ARN\) of the DataSync agent that want to connect to your NFS file server\.  
You can specify more than one agent\. For more information, see [Using multiple agents for transfers](https://docs.aws.amazon.com/datasync/latest/userguide/multiple-agents.html)\.  
*Required*: Yes  
*Type*: [OnPremConfig](aws-properties-datasync-locationnfs-onpremconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServerHostname`  <a name="cfn-datasync-locationnfs-serverhostname"></a>
Specifies the Domain Name System \(DNS\) name or IP version 4 address of the NFS file server that your DataSync agent connects to\.  
*Required*: No  
*Type*: String  
*Maximum*: `255`  
*Pattern*: `^(([a-zA-Z0-9\-]*[a-zA-Z0-9])\.)*([A-Za-z0-9\-]*[A-Za-z0-9])$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Subdirectory`  <a name="cfn-datasync-locationnfs-subdirectory"></a>
Specifies the export path in your NFS file server that you want DataSync to mount\.  
This path \(or a subdirectory of the path\) is where DataSync transfers data to or from\. For information on configuring an export for DataSync, see [Accessing NFS file servers](https://docs.aws.amazon.com/datasync/latest/userguide/create-nfs-location.html#accessing-nfs)\.  
*Required*: No  
*Type*: String  
*Maximum*: `4096`  
*Pattern*: `^[a-zA-Z0-9_\-\+\./\(\)\p{Zs}]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-datasync-locationnfs-tags"></a>
Specifies labels that help you categorize, filter, and search for your AWS resources\. We recommend creating at least a name tag for your location\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-datasync-locationnfs-return-values"></a>

### Ref<a name="aws-resource-datasync-locationnfs-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the location resource ARN\. For example:

`arn:aws:datasync:us-east-2:111222333444:location/loc-07db7abfc326c50s3`

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-datasync-locationnfs-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-datasync-locationnfs-return-values-fn--getatt-fn--getatt"></a>

`LocationArn`  <a name="LocationArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the specified source NFS file system location\.

`LocationUri`  <a name="LocationUri-fn::getatt"></a>
The URI of the specified source NFS location\.

## Examples<a name="aws-resource-datasync-locationnfs--examples"></a>



### Create a NFS location for DataSync<a name="aws-resource-datasync-locationnfs--examples--Create_a_NFS_location_for_DataSync"></a>

The following example specifies an NFS location for DataSync, using a source and destination location\. In this example, the server hostname is `MyServer@example.com`, using NFS version 4\.0, in the subdirectory `/MySubdirectory`\. 

#### JSON<a name="aws-resource-datasync-locationnfs--examples--Create_a_NFS_location_for_DataSync--json"></a>

```
{
"AWSTemplateFormatVersion": "2010-09-09",
"Description": "Specifies an NFS location for DataSync",
"Resources": 
  "LocationNFS": {
    "Type": "AWS::DataSync::LocationNFS",
    "Properties": {
      "MountOptions": {
        "Version": "NFS4_0"
      },
      "OnPremConfig": {
        "AgentArns": [
          "arn:aws:datasync:us-east-2:111222333444:agent/agent-0b0addbeef44b3nfs"
        ]
      },
      "ServerHostname": "MyServer@example.com",
      "Subdirectory": "/MySubdirectory"
    }
  }
}
```

#### YAML<a name="aws-resource-datasync-locationnfs--examples--Create_a_NFS_location_for_DataSync--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: Specifies an NFS location for DataSync
Resources:
LocationNFS:
  Type: AWS::DataSync::LocationNFS
  Properties: 
    MountOptions: 
      Version: NFS4_0
    OnPremConfig: 
      AgentArns: 
        - arn:aws:datasync:us-east-2:111222333444:agent/agent-0b0addbeef44b3nfs
    ServerHostname: MyServer@example.com
    Subdirectory: /MySubdirectory
```