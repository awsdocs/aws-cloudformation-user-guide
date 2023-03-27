# AWS::DataSync::LocationObjectStorage<a name="aws-resource-datasync-locationobjectstorage"></a>

The `AWS::DataSync::LocationObjectStorage` resource specifies an endpoint for a self\-managed object storage bucket\. For more information about self\-managed object storage locations, see [Creating a Location for Object Storage](https://docs.aws.amazon.com/datasync/latest/userguide/create-object-location.html)\. 

## Syntax<a name="aws-resource-datasync-locationobjectstorage-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-datasync-locationobjectstorage-syntax.json"></a>

```
{
  "Type" : "AWS::DataSync::LocationObjectStorage",
  "Properties" : {
      "[AccessKey](#cfn-datasync-locationobjectstorage-accesskey)" : String,
      "[AgentArns](#cfn-datasync-locationobjectstorage-agentarns)" : [ String, ... ],
      "[BucketName](#cfn-datasync-locationobjectstorage-bucketname)" : String,
      "[SecretKey](#cfn-datasync-locationobjectstorage-secretkey)" : String,
      "[ServerCertificate](#cfn-datasync-locationobjectstorage-servercertificate)" : String,
      "[ServerHostname](#cfn-datasync-locationobjectstorage-serverhostname)" : String,
      "[ServerPort](#cfn-datasync-locationobjectstorage-serverport)" : Integer,
      "[ServerProtocol](#cfn-datasync-locationobjectstorage-serverprotocol)" : String,
      "[Subdirectory](#cfn-datasync-locationobjectstorage-subdirectory)" : String,
      "[Tags](#cfn-datasync-locationobjectstorage-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-datasync-locationobjectstorage-syntax.yaml"></a>

```
Type: AWS::DataSync::LocationObjectStorage
Properties: 
  [AccessKey](#cfn-datasync-locationobjectstorage-accesskey): String
  [AgentArns](#cfn-datasync-locationobjectstorage-agentarns): 
    - String
  [BucketName](#cfn-datasync-locationobjectstorage-bucketname): String
  [SecretKey](#cfn-datasync-locationobjectstorage-secretkey): String
  [ServerCertificate](#cfn-datasync-locationobjectstorage-servercertificate): String
  [ServerHostname](#cfn-datasync-locationobjectstorage-serverhostname): String
  [ServerPort](#cfn-datasync-locationobjectstorage-serverport): Integer
  [ServerProtocol](#cfn-datasync-locationobjectstorage-serverprotocol): String
  [Subdirectory](#cfn-datasync-locationobjectstorage-subdirectory): String
  [Tags](#cfn-datasync-locationobjectstorage-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-datasync-locationobjectstorage-properties"></a>

`AccessKey`  <a name="cfn-datasync-locationobjectstorage-accesskey"></a>
Specifies the access key \(for example, a user name\) if credentials are required to authenticate with the object storage server\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `200`  
*Pattern*: `^.+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AgentArns`  <a name="cfn-datasync-locationobjectstorage-agentarns"></a>
Specifies the Amazon Resource Names \(ARNs\) of the DataSync agents that can securely connect with your location\.  
*Required*: Yes  
*Type*: List of String  
*Maximum*: `4`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BucketName`  <a name="cfn-datasync-locationobjectstorage-bucketname"></a>
Specifies the name of the object storage bucket involved in the transfer\.  
*Required*: No  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `63`  
*Pattern*: `^[a-zA-Z0-9_\-\+\./\(\)\$\p{Zs}]+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SecretKey`  <a name="cfn-datasync-locationobjectstorage-secretkey"></a>
Specifies the secret key \(for example, a password\) if credentials are required to authenticate with the object storage server\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `200`  
*Pattern*: `^.+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServerCertificate`  <a name="cfn-datasync-locationobjectstorage-servercertificate"></a>
Specifies a certificate to authenticate with an object storage system that uses a private or self\-signed certificate authority \(CA\)\. You must specify a Base64\-encoded `.pem` file \(for example, `file:///home/user/.ssh/storage_sys_certificate.pem`\)\. The certificate can be up to 32768 bytes \(before Base64 encoding\)\.  
To use this parameter, configure `ServerProtocol` to `HTTPS`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServerHostname`  <a name="cfn-datasync-locationobjectstorage-serverhostname"></a>
Specifies the domain name or IP address of the object storage server\. A DataSync agent uses this hostname to mount the object storage server in a network\.  
*Required*: No  
*Type*: String  
*Maximum*: `255`  
*Pattern*: `^(([a-zA-Z0-9\-]*[a-zA-Z0-9])\.)*([A-Za-z0-9\-]*[A-Za-z0-9])$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ServerPort`  <a name="cfn-datasync-locationobjectstorage-serverport"></a>
Specifies the port that your object storage server accepts inbound network traffic on \(for example, port 443\)\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `65536`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServerProtocol`  <a name="cfn-datasync-locationobjectstorage-serverprotocol"></a>
Specifies the protocol that your object storage server uses to communicate\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HTTP | HTTPS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Subdirectory`  <a name="cfn-datasync-locationobjectstorage-subdirectory"></a>
Specifies the object prefix for your object storage server\. If this is a source location, DataSync only copies objects with this prefix\. If this is a destination location, DataSync writes all objects with this prefix\.   
*Required*: No  
*Type*: String  
*Maximum*: `4096`  
*Pattern*: `^[a-zA-Z0-9_\-\+\./\(\)\p{Zs}]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-datasync-locationobjectstorage-tags"></a>
Specifies the key\-value pair that represents a tag that you want to add to the resource\. Tags can help you manage, filter, and search for your resources\. We recommend creating a name tag for your location\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-datasync-locationobjectstorage-return-values"></a>

### Ref<a name="aws-resource-datasync-locationobjectstorage-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the location resource Amazon Resource Name \(ARN\)\. For example:

`arn:aws:datasync:us-east-2:111222333444:location/loc-07db7abfc326c50s3`

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-datasync-locationobjectstorage-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-datasync-locationobjectstorage-return-values-fn--getatt-fn--getatt"></a>

`LocationArn`  <a name="LocationArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the specified object storage location\.

`LocationUri`  <a name="LocationUri-fn::getatt"></a>
The URI of the specified object storage location\.

## Examples<a name="aws-resource-datasync-locationobjectstorage--examples"></a>



### Create an object storage location for DataSync<a name="aws-resource-datasync-locationobjectstorage--examples--Create_an_object_storage_location_for_DataSync"></a>

The following example specifies an object storage location for DataSync\. In this example, the object storage location uses the bucket named `MyBucket`, on the server named `MyServer@example.com`\. This example also specifies the server protocol `HTTPS` and the subdirectory `/Subdirectory`\. 

#### JSON<a name="aws-resource-datasync-locationobjectstorage--examples--Create_an_object_storage_location_for_DataSync--json"></a>

```
{
"AWSTemplateFormatVersion": "2010-09-09",
"Description": "Specifies an object storage location for DataSync",
"Resources": 
{
  "LocationObjectStorage": {
    "Type": "AWS::DataSync::LocationObjectStorage",
    "Properties": {
      "AgentArns": [
        "arn:aws:datasync:us-east-2:111222333444:agent/agent-0b0addbeef44b3nfs"
      ],
      "BucketName": "MyBucket",
      "ServerHostname": "MyServer@example.com",
      "ServerProtocol": "HTTPS",
      "Subdirectory": "/MySubdirectory"
    }
  }
}
```

#### YAML<a name="aws-resource-datasync-locationobjectstorage--examples--Create_an_object_storage_location_for_DataSync--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: Specifies an object storage location for DataSync
Resources:
  LocationObjectStorage:
    Type: AWS::DataSync::LocationObjectStorage
    Properties: 
      AgentArns: 
        - arn:aws:datasync:us-east-2:111222333444:agent/agent-0b0addbeef44b3nfs
      BucketName: MyBucket
      ServerHostname: MyServer@example.com
      ServerProtocol: HTTPS
      Subdirectory: /MySubdirectory
```