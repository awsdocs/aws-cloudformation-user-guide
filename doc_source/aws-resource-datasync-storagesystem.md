# AWS::DataSync::StorageSystem<a name="aws-resource-datasync-storagesystem"></a>

The `AWS::DataSync::StorageSystem` resource creates an AWS resource for an on\-premises storage system that you want DataSync Discovery to collect information about\. For more information, see [discovering your storage with DataSync Discovery\.](https://docs.aws.amazon.com/datasync/latest/userguide/understanding-your-storage.html)

## Syntax<a name="aws-resource-datasync-storagesystem-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-datasync-storagesystem-syntax.json"></a>

```
{
  "Type" : "AWS::DataSync::StorageSystem",
  "Properties" : {
      "[AgentArns](#cfn-datasync-storagesystem-agentarns)" : [ String, ... ],
      "[CloudWatchLogGroupArn](#cfn-datasync-storagesystem-cloudwatchloggrouparn)" : String,
      "[Name](#cfn-datasync-storagesystem-name)" : String,
      "[ServerConfiguration](#cfn-datasync-storagesystem-serverconfiguration)" : ServerConfiguration,
      "[ServerCredentials](#cfn-datasync-storagesystem-servercredentials)" : ServerCredentials,
      "[SystemType](#cfn-datasync-storagesystem-systemtype)" : String,
      "[Tags](#cfn-datasync-storagesystem-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-datasync-storagesystem-syntax.yaml"></a>

```
Type: AWS::DataSync::StorageSystem
Properties: 
  [AgentArns](#cfn-datasync-storagesystem-agentarns): 
    - String
  [CloudWatchLogGroupArn](#cfn-datasync-storagesystem-cloudwatchloggrouparn): String
  [Name](#cfn-datasync-storagesystem-name): String
  [ServerConfiguration](#cfn-datasync-storagesystem-serverconfiguration): 
    ServerConfiguration
  [ServerCredentials](#cfn-datasync-storagesystem-servercredentials): 
    ServerCredentials
  [SystemType](#cfn-datasync-storagesystem-systemtype): String
  [Tags](#cfn-datasync-storagesystem-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-datasync-storagesystem-properties"></a>

`AgentArns`  <a name="cfn-datasync-storagesystem-agentarns"></a>
Specifies the Amazon Resource Name \(ARN\) of the DataSync agent that connects to and reads from your on\-premises storage system's management interface\. You can only specify one ARN\.  
*Required*: Yes  
*Type*: List of String  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CloudWatchLogGroupArn`  <a name="cfn-datasync-storagesystem-cloudwatchloggrouparn"></a>
Specifies the ARN of the Amazon CloudWatch log group for monitoring and logging discovery job events\.  
*Required*: No  
*Type*: String  
*Maximum*: `562`  
*Pattern*: `^arn:(aws|aws-cn|aws-us-gov|aws-iso|aws-iso-b):logs:[a-z\-0-9]+:[0-9]{12}:log-group:([^:\*]*)(:\*)?$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-datasync-storagesystem-name"></a>
Specifies a familiar name for your on\-premises storage system\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `^[\p{L}\p{M}\p{N}\s+=._:@\/-]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServerConfiguration`  <a name="cfn-datasync-storagesystem-serverconfiguration"></a>
Specifies the server name and network port required to connect with the management interface of your on\-premises storage system\.  
*Required*: Yes  
*Type*: [ServerConfiguration](aws-properties-datasync-storagesystem-serverconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServerCredentials`  <a name="cfn-datasync-storagesystem-servercredentials"></a>
Specifies the user name and password for accessing your on\-premises storage system's management interface\.  
*Required*: No  
*Type*: [ServerCredentials](aws-properties-datasync-storagesystem-servercredentials.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SystemType`  <a name="cfn-datasync-storagesystem-systemtype"></a>
Specifies the type of on\-premises storage system that you want DataSync Discovery to collect information about\.  
DataSync Discovery currently supports NetApp Fabric\-Attached Storage \(FAS\) and All Flash FAS \(AFF\) systems running ONTAP 9\.7 or later\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `NetAppONTAP`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-datasync-storagesystem-tags"></a>
Specifies labels that help you categorize, filter, and search for your AWS resources\. We recommend creating at least a name tag for your on\-premises storage system\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-datasync-storagesystem-return-values"></a>

### Ref<a name="aws-resource-datasync-storagesystem-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the ARN of the on\-premises storage system that you created\. For example:

`arn:aws:datasync:us-east-1:111222333444:system/storage-system-abcdef01234567890`

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-datasync-storagesystem-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-datasync-storagesystem-return-values-fn--getatt-fn--getatt"></a>

`ConnectivityStatus`  <a name="ConnectivityStatus-fn::getatt"></a>
Indicates whether your DataSync agent can connect to your on\-premises storage system\.

`SecretsManagerArn`  <a name="SecretsManagerArn-fn::getatt"></a>
The ARN of the secret that stores your on\-premises storage system's credentials\. DataSync Discovery stores these credentials in [AWS Secrets Manager](https://docs.aws.amazon.com/datasync/latest/userguide/discovery-configure-storage.html#discovery-add-storage)\.

`StorageSystemArn`  <a name="StorageSystemArn-fn::getatt"></a>
The ARN of the on\-premises storage system that you're using with DataSync Discovery\.

## Examples<a name="aws-resource-datasync-storagesystem--examples"></a>

### Adding an on on\-premises storage system to use with DataSync Discovery<a name="aws-resource-datasync-storagesystem--examples--Adding_an_on_on-premises_storage_system_to_use_with_DataSync_Discovery"></a>

The following example adds an on\-premises storage system that you want to collect information about\.

#### JSON<a name="aws-resource-datasync-storagesystem--examples--Adding_an_on_on-premises_storage_system_to_use_with_DataSync_Discovery--json"></a>

```
{
    "Type": "AWS::DataSync::StorageSystem",
    "Properties": {
        "AgentArns": [
            "arn:aws:datasync:us-east-1:111222333444:agent/agent-012345abcde012345"
        ],
        "CloudWatchLogGroupArn": "arn:aws:logs:us-east-1:111222333444:log-group:/aws/datasync/discovery:*",
        "Name": "MyOnPremStorage",
        "ServerConfiguration": {
            "ServerHostname": "172.16.0.0",
            "ServerPort": 443
        },
        "ServerCredentials": {
            "Username": "admin",
            "Password": "1234"
        },
        "SystemType": "NetAppONTAP",
        "Tags": [
            {
                "Key": "Migration Plan",
                "Value": "1"
            }
        ]
    }
}
```

#### YAML<a name="aws-resource-datasync-storagesystem--examples--Adding_an_on_on-premises_storage_system_to_use_with_DataSync_Discovery--yaml"></a>

```
Type: 'AWS::DataSync::StorageSystem'
Properties:
  AgentArns:
    - 'arn:aws:datasync:us-east-1:111222333444:agent/agent-012345abcde012345'
  CloudWatchLogGroupArn: 'arn:aws:logs:us-east-1:111222333444:log-group:/aws/datasync/discovery:*'
  Name: MyOnPremStorage
  ServerConfiguration:
    ServerHostname: 172.16.0.0
    ServerPort: 443
  ServerCredentials:
    Username: admin
    Password: '1234'
  SystemType: NetAppONTAP
  Tags:
    - Key: Migration Plan
      Value: '1'
```