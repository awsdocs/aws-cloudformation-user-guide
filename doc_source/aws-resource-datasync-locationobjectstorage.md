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
  [ServerHostname](#cfn-datasync-locationobjectstorage-serverhostname): String
  [ServerPort](#cfn-datasync-locationobjectstorage-serverport): Integer
  [ServerProtocol](#cfn-datasync-locationobjectstorage-serverprotocol): String
  [Subdirectory](#cfn-datasync-locationobjectstorage-subdirectory): String
  [Tags](#cfn-datasync-locationobjectstorage-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-datasync-locationobjectstorage-properties"></a>

`AccessKey`  <a name="cfn-datasync-locationobjectstorage-accesskey"></a>
Optional\. The access key is used if credentials are required to access the self\-managed object storage server\. If your object storage requires a user name and password to authenticate, use `AccessKey` and `SecretKey` to provide the user name and password, respectively\.  
*Required*: No  
*Type*: String  
*Minimum*: `8`  
*Maximum*: `200`  
*Pattern*: `^.+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`AgentArns`  <a name="cfn-datasync-locationobjectstorage-agentarns"></a>
The Amazon Resource Name \(ARN\) of the agents associated with the self\-managed object storage server location\.  
*Required*: Yes  
*Type*: List of String  
*Maximum*: `4`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`BucketName`  <a name="cfn-datasync-locationobjectstorage-bucketname"></a>
The bucket on the self\-managed object storage server that is used to read data from\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `63`  
*Pattern*: `^[a-zA-Z0-9_\-\+\./\(\)\$\p{Zs}]+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SecretKey`  <a name="cfn-datasync-locationobjectstorage-secretkey"></a>
Optional\. The secret key is used if credentials are required to access the self\-managed object storage server\. If your object storage requires a user name and password to authenticate, use `AccessKey` and `SecretKey` to provide the user name and password, respectively\.  
*Required*: No  
*Type*: String  
*Minimum*: `8`  
*Maximum*: `200`  
*Pattern*: `^.+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ServerHostname`  <a name="cfn-datasync-locationobjectstorage-serverhostname"></a>
The name of the self\-managed object storage server\. This value is the IP address or Domain Name Service \(DNS\) name of the object storage server\. An agent uses this host name to mount the object storage server in a network\.   
*Required*: Yes  
*Type*: String  
*Maximum*: `255`  
*Pattern*: `^(([a-zA-Z0-9\-]*[a-zA-Z0-9])\.)*([A-Za-z0-9\-]*[A-Za-z0-9])$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ServerPort`  <a name="cfn-datasync-locationobjectstorage-serverport"></a>
The port that your self\-managed object storage server accepts inbound network traffic on\. The server port is set by default to TCP 80 \(HTTP\) or TCP 443 \(HTTPS\)\. You can specify a custom port if your self\-managed object storage server requires one\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `65536`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ServerProtocol`  <a name="cfn-datasync-locationobjectstorage-serverprotocol"></a>
The protocol that the object storage server uses to communicate\. Valid values are HTTP or HTTPS\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HTTP | HTTPS`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Subdirectory`  <a name="cfn-datasync-locationobjectstorage-subdirectory"></a>
The subdirectory in the self\-managed object storage server that is used to read data from\.  
*Required*: No  
*Type*: String  
*Maximum*: `4096`  
*Pattern*: `^[a-zA-Z0-9_\-\+\./\(\)\p{Zs}]*$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-datasync-locationobjectstorage-tags"></a>
The key\-value pair that represents the tag that you want to add to the location\. The value can be an empty string\. We recommend using tags to name your resources\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-datasync-locationobjectstorage-return-values"></a>

### Ref<a name="aws-resource-datasync-locationobjectstorage-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the location resource ARN\. For example:

`arn:aws:datasync:us-east-2:111222333444:location/loc-07db7abfc326c50s3`

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-datasync-locationobjectstorage-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-datasync-locationobjectstorage-return-values-fn--getatt-fn--getatt"></a>

`LocationArn`  <a name="LocationArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the specified object storage location\.

`LocationUri`  <a name="LocationUri-fn::getatt"></a>
The URL of the specified object storage location\.

## Examples<a name="aws-resource-datasync-locationobjectstorage--examples"></a>



### Object storage location for DataSync<a name="aws-resource-datasync-locationobjectstorage--examples--Object_storage_location_for_DataSync"></a>

The following example specifies an object storage location for DataSync\. In this example, the object storage location uses the bucket named `MyBucket`, on the server named `MyServer@example.com`\. This example also specifies the server protocol `HTTPS` and the subdirectory `/Subdirectory`\. 

#### JSON<a name="aws-resource-datasync-locationobjectstorage--examples--Object_storage_location_for_DataSync--json"></a>

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

#### YAML<a name="aws-resource-datasync-locationobjectstorage--examples--Object_storage_location_for_DataSync--yaml"></a>

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