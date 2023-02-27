# AWS::DataSync::LocationSMB<a name="aws-resource-datasync-locationsmb"></a>

The `AWS::DataSync::LocationSMB` resource specifies a Server Message Block \(SMB\) location\.

## Syntax<a name="aws-resource-datasync-locationsmb-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-datasync-locationsmb-syntax.json"></a>

```
{
  "Type" : "AWS::DataSync::LocationSMB",
  "Properties" : {
      "[AgentArns](#cfn-datasync-locationsmb-agentarns)" : [ String, ... ],
      "[Domain](#cfn-datasync-locationsmb-domain)" : String,
      "[MountOptions](#cfn-datasync-locationsmb-mountoptions)" : MountOptions,
      "[Password](#cfn-datasync-locationsmb-password)" : String,
      "[ServerHostname](#cfn-datasync-locationsmb-serverhostname)" : String,
      "[Subdirectory](#cfn-datasync-locationsmb-subdirectory)" : String,
      "[Tags](#cfn-datasync-locationsmb-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[User](#cfn-datasync-locationsmb-user)" : String
    }
}
```

### YAML<a name="aws-resource-datasync-locationsmb-syntax.yaml"></a>

```
Type: AWS::DataSync::LocationSMB
Properties: 
  [AgentArns](#cfn-datasync-locationsmb-agentarns): 
    - String
  [Domain](#cfn-datasync-locationsmb-domain): String
  [MountOptions](#cfn-datasync-locationsmb-mountoptions): 
    MountOptions
  [Password](#cfn-datasync-locationsmb-password): String
  [ServerHostname](#cfn-datasync-locationsmb-serverhostname): String
  [Subdirectory](#cfn-datasync-locationsmb-subdirectory): String
  [Tags](#cfn-datasync-locationsmb-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [User](#cfn-datasync-locationsmb-user): String
```

## Properties<a name="aws-resource-datasync-locationsmb-properties"></a>

`AgentArns`  <a name="cfn-datasync-locationsmb-agentarns"></a>
The Amazon Resource Names \(ARNs\) of agents to use for a Server Message Block \(SMB\) location\.   
*Required*: Yes  
*Type*: List of String  
*Maximum*: `4`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Domain`  <a name="cfn-datasync-locationsmb-domain"></a>
Specifies the Windows domain name that your SMB file server belongs to\.   
For more information, see [required permissions](https://docs.aws.amazon.com/datasync/latest/userguide/create-smb-location.html#configuring-smb-permissions) for SMB locations\.  
*Required*: No  
*Type*: String  
*Maximum*: `253`  
*Pattern*: `^[A-Za-z0-9]((\.|-+)?[A-Za-z0-9]){0,252}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MountOptions`  <a name="cfn-datasync-locationsmb-mountoptions"></a>
Specifies the version of the SMB protocol that DataSync uses to access your SMB file server\.  
*Required*: No  
*Type*: [MountOptions](aws-properties-datasync-locationsmb-mountoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Password`  <a name="cfn-datasync-locationsmb-password"></a>
The password of the user who can mount the share and has the permissions to access files and folders in the SMB share\.  
*Required*: No  
*Type*: String  
*Maximum*: `104`  
*Pattern*: `^.{0,104}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServerHostname`  <a name="cfn-datasync-locationsmb-serverhostname"></a>
Specifies the Domain Name Service \(DNS\) name or IP address of the SMB file server that your DataSync agent will mount\.  
You can't specify an IP version 6 \(IPv6\) address\.
*Required*: No  
*Type*: String  
*Maximum*: `255`  
*Pattern*: `^(([a-zA-Z0-9\-]*[a-zA-Z0-9])\.)*([A-Za-z0-9\-]*[A-Za-z0-9])$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Subdirectory`  <a name="cfn-datasync-locationsmb-subdirectory"></a>
The subdirectory in the SMB file system that is used to read data from the SMB source location or write data to the SMB destination\. The SMB path should be a path that's exported by the SMB server, or a subdirectory of that path\. The path should be such that it can be mounted by other SMB clients in your network\.  
 `Subdirectory` must be specified with forward slashes\. For example, `/path/to/folder`\.
To transfer all the data in the folder you specified, DataSync must have permissions to mount the SMB share, as well as to access all the data in that share\. To ensure this, either make sure that the user name and password specified belongs to the user who can mount the share, and who has the appropriate permissions for all of the files and directories that you want DataSync to access, or use credentials of a member of the Backup Operators group to mount the share\. Doing either one enables the agent to access the data\. For the agent to access directories, you must additionally enable all execute access\.  
*Required*: No  
*Type*: String  
*Maximum*: `4096`  
*Pattern*: `^[a-zA-Z0-9_\-\+\./\(\)\$\p{Zs}]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-datasync-locationsmb-tags"></a>
Specifies labels that help you categorize, filter, and search for your AWS resources\. We recommend creating at least a name tag for your location\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`User`  <a name="cfn-datasync-locationsmb-user"></a>
The user who can mount the share and has the permissions to access files and folders in the SMB share\.  
For information about choosing a user name that ensures sufficient permissions to files, folders, and metadata, see [user](https://docs.aws.amazon.com/datasync/latest/userguide/create-smb-location.html#SMBuser)\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `104`  
*Pattern*: `^[^\x5B\x5D\\/:;|=,+*?]{1,104}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-datasync-locationsmb-return-values"></a>

### Ref<a name="aws-resource-datasync-locationsmb-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the location resource Amazon Resource Name \(ARN\)\. For example:

`arn:aws:datasync:us-east-2:111222333444:location/loc-07db7abfc326c50s3`

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-datasync-locationsmb-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-datasync-locationsmb-return-values-fn--getatt-fn--getatt"></a>

`LocationArn`  <a name="LocationArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the specified SMB file system\.

`LocationUri`  <a name="LocationUri-fn::getatt"></a>
The URI of the specified SMB location\.

## Examples<a name="aws-resource-datasync-locationsmb--examples"></a>



### Create an SMB storage location for DataSync<a name="aws-resource-datasync-locationsmb--examples--Create_an_SMB_storage_location_for_DataSync"></a>

The following example specifies an SMB storage location for DataSync\. In this example, the SMB location uses the domain `EXAMPLE` with SMB version 3\. The server hostname is `MyServer@example.com`, and the SMB location is in the `/share` subdirectory\. This example specifies the user ID `user-1`\. 

#### JSON<a name="aws-resource-datasync-locationsmb--examples--Create_an_SMB_storage_location_for_DataSync--json"></a>

```
{
"AWSTemplateFormatVersion": "2010-09-09",
"Description": "Specifies an SMB storage location for DataSync",
"Resources": 
  {
    "LocationSMB": {
      "Type": "AWS::DataSync::LocationSMB",
      "Properties": {
        "AgentArns": [
          "arn:aws:datasync:us-east-2:111222333444:agent/agent-0b0addbeef44b3nfs,",
          "arn:aws:datasync:us-east-2:111222333444:agent/agent-2345noo35nnee1123ovo3"
        ],
        "Domain": "EXAMPLE",
        "MountOptions": {
          "Version": "SMB3"
        },
        "Password": {"Ref": "Password"},
        "ServerHostname": "MyServer.example.com",
        "Subdirectory": "/share",
        "User": "user-1"
      }
    }
  }            
}
```

#### YAML<a name="aws-resource-datasync-locationsmb--examples--Create_an_SMB_storage_location_for_DataSync--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: Specifies an object storage location for DataSync
Resources:
  LocationSMB:
    Type: AWS::DataSync::LocationSMB
    Properties: 
      AgentArns: 
        - arn:aws:datasync:us-east-2:111222333444:agent/agent-0b0addbeef44b3nfs,
        - arn:aws:datasync:us-east-2:111222333444:agent/agent-2345noo35nnee1123ovo3
      Domain: EXAMPLE
      MountOptions: 
        Version: SMB3
      Password: !Ref Password
      ServerHostname: MyServer.example.com
      Subdirectory: /share
      User: user-1
```