# AWS::AmazonMQ::Broker<a name="aws-resource-amazonmq-broker"></a>

A *broker* is a message broker environment running on Amazon MQ\. It is the basic building block of Amazon MQ\.

The `AWS::AmazonMQ::Broker` resource lets you create Amazon MQ brokers, add configuration changes or modify users for the specified broker, return information about the specified broker, and delete the specified broker\. For more information, see [Amazon MQ Basic Elements](https://docs.aws.amazon.com/amazon-mq/latest/developer-guide/amazon-mq-basic-elements.html) in the *Amazon MQ Developer Guide*\.
+ `ec2:CreateNetworkInterface`

  This permission is required to allow Amazon MQ to create an elastic network interface \(ENI\) on behalf of your account\.
+ `ec2:CreateNetworkInterfacePermission`

  This permission is required to attach the ENI to the broker instance\.
+ `ec2:DeleteNetworkInterface`
+ `ec2:DeleteNetworkInterfacePermission`
+ `ec2:DetachNetworkInterface`
+ `ec2:DescribeInternetGateways`
+ `ec2:DescribeNetworkInterfaces`
+ `ec2:DescribeNetworkInterfacePermissions`
+ `ec2:DescribeRouteTables`
+ `ec2:DescribeSecurityGroups`
+ `ec2:DescribeSubnets`
+ `ec2:DescribeVpcs`

## Syntax<a name="aws-resource-amazonmq-broker-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-amazonmq-broker-syntax.json"></a>

```
{
  "Type" : "AWS::AmazonMQ::Broker",
  "Properties" : {
      "[AuthenticationStrategy](#cfn-amazonmq-broker-authenticationstrategy)" : String,
      "[AutoMinorVersionUpgrade](#cfn-amazonmq-broker-autominorversionupgrade)" : Boolean,
      "[BrokerName](#cfn-amazonmq-broker-brokername)" : String,
      "[Configuration](#cfn-amazonmq-broker-configuration)" : ConfigurationId,
      "[DeploymentMode](#cfn-amazonmq-broker-deploymentmode)" : String,
      "[EncryptionOptions](#cfn-amazonmq-broker-encryptionoptions)" : EncryptionOptions,
      "[EngineType](#cfn-amazonmq-broker-enginetype)" : String,
      "[EngineVersion](#cfn-amazonmq-broker-engineversion)" : String,
      "[HostInstanceType](#cfn-amazonmq-broker-hostinstancetype)" : String,
      "[LdapMetadata](#cfn-amazonmq-broker-ldapmetadata)" : LdapMetadata,
      "[LdapServerMetadata](#cfn-amazonmq-broker-ldapservermetadata)" : LdapServerMetadata,
      "[Logs](#cfn-amazonmq-broker-logs)" : LogList,
      "[MaintenanceWindowStartTime](#cfn-amazonmq-broker-maintenancewindowstarttime)" : MaintenanceWindow,
      "[PubliclyAccessible](#cfn-amazonmq-broker-publiclyaccessible)" : Boolean,
      "[SecurityGroups](#cfn-amazonmq-broker-securitygroups)" : [ String, ... ],
      "[StorageType](#cfn-amazonmq-broker-storagetype)" : String,
      "[SubnetIds](#cfn-amazonmq-broker-subnetids)" : [ String, ... ],
      "[Tags](#cfn-amazonmq-broker-tags)" : [ TagsEntry, ... ],
      "[Users](#cfn-amazonmq-broker-users)" : [ User, ... ]
    }
}
```

### YAML<a name="aws-resource-amazonmq-broker-syntax.yaml"></a>

```
Type: AWS::AmazonMQ::Broker
Properties: 
  [AuthenticationStrategy](#cfn-amazonmq-broker-authenticationstrategy): String
  [AutoMinorVersionUpgrade](#cfn-amazonmq-broker-autominorversionupgrade): Boolean
  [BrokerName](#cfn-amazonmq-broker-brokername): String
  [Configuration](#cfn-amazonmq-broker-configuration): 
    ConfigurationId
  [DeploymentMode](#cfn-amazonmq-broker-deploymentmode): String
  [EncryptionOptions](#cfn-amazonmq-broker-encryptionoptions): 
    EncryptionOptions
  [EngineType](#cfn-amazonmq-broker-enginetype): String
  [EngineVersion](#cfn-amazonmq-broker-engineversion): String
  [HostInstanceType](#cfn-amazonmq-broker-hostinstancetype): String
  [LdapMetadata](#cfn-amazonmq-broker-ldapmetadata): 
    LdapMetadata
  [LdapServerMetadata](#cfn-amazonmq-broker-ldapservermetadata): 
    LdapServerMetadata
  [Logs](#cfn-amazonmq-broker-logs): 
    LogList
  [MaintenanceWindowStartTime](#cfn-amazonmq-broker-maintenancewindowstarttime): 
    MaintenanceWindow
  [PubliclyAccessible](#cfn-amazonmq-broker-publiclyaccessible): Boolean
  [SecurityGroups](#cfn-amazonmq-broker-securitygroups): 
    - String
  [StorageType](#cfn-amazonmq-broker-storagetype): String
  [SubnetIds](#cfn-amazonmq-broker-subnetids): 
    - String
  [Tags](#cfn-amazonmq-broker-tags): 
    - TagsEntry
  [Users](#cfn-amazonmq-broker-users): 
    - User
```

## Properties<a name="aws-resource-amazonmq-broker-properties"></a>

`AuthenticationStrategy`  <a name="cfn-amazonmq-broker-authenticationstrategy"></a>
Optional\. The authentication strategy used to secure the broker\. The default is `SIMPLE`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`AutoMinorVersionUpgrade`  <a name="cfn-amazonmq-broker-autominorversionupgrade"></a>
Enables automatic upgrades to new minor versions for brokers, as Apache releases the versions\. The automatic upgrades occur during the maintenance window of the broker or after a manual broker reboot\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BrokerName`  <a name="cfn-amazonmq-broker-brokername"></a>
The name of the broker\. This value must be unique in your AWS account, 1\-50 characters long, must contain only letters, numbers, dashes, and underscores, and must not contain white spaces, brackets, wildcard characters, or special characters\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Configuration`  <a name="cfn-amazonmq-broker-configuration"></a>
A list of information about the configuration\.  
*Required*: No  
*Type*: [ConfigurationId](aws-properties-amazonmq-broker-configurationid.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeploymentMode`  <a name="cfn-amazonmq-broker-deploymentmode"></a>
The deployment mode of the broker\. Available values:  
+ `SINGLE_INSTANCE`
+ `ACTIVE_STANDBY_MULTI_AZ`
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EncryptionOptions`  <a name="cfn-amazonmq-broker-encryptionoptions"></a>
Encryption options for the broker\.  
*Required*: No  
*Type*: [EncryptionOptions](aws-properties-amazonmq-broker-encryptionoptions.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EngineType`  <a name="cfn-amazonmq-broker-enginetype"></a>
The type of broker engine\. Note: Currently, Amazon MQ supports only ACTIVEMQ\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EngineVersion`  <a name="cfn-amazonmq-broker-engineversion"></a>
The version of the broker engine\. For a list of supported engine versions, see [Engine](https://docs.aws.amazon.com/amazon-mq/latest/developer-guide/broker-engine.html) in the *Amazon MQ Developer Guide*\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HostInstanceType`  <a name="cfn-amazonmq-broker-hostinstancetype"></a>
The broker's instance type\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LdapMetadata`  <a name="cfn-amazonmq-broker-ldapmetadata"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: [LdapMetadata](aws-properties-amazonmq-broker-ldapmetadata.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LdapServerMetadata`  <a name="cfn-amazonmq-broker-ldapservermetadata"></a>
Optional\. The metadata of the LDAP server used to authenticate and authorize connections to the broker\.  
*Required*: No  
*Type*: [LdapServerMetadata](aws-properties-amazonmq-broker-ldapservermetadata.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Logs`  <a name="cfn-amazonmq-broker-logs"></a>
Enables Amazon CloudWatch logging for brokers\.  
*Required*: No  
*Type*: [LogList](aws-properties-amazonmq-broker-loglist.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaintenanceWindowStartTime`  <a name="cfn-amazonmq-broker-maintenancewindowstarttime"></a>
The scheduled time period relative to UTC during which Amazon MQ begins to apply pending updates or patches to the broker\.\.  
*Required*: No  
*Type*: [MaintenanceWindow](aws-properties-amazonmq-broker-maintenancewindow.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PubliclyAccessible`  <a name="cfn-amazonmq-broker-publiclyaccessible"></a>
Enables connections from applications outside of the VPC that hosts the broker's subnets\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SecurityGroups`  <a name="cfn-amazonmq-broker-securitygroups"></a>
The list of rules \(1 minimum, 125 maximum\) that authorize connections to brokers\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StorageType`  <a name="cfn-amazonmq-broker-storagetype"></a>
The broker's storage type\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SubnetIds`  <a name="cfn-amazonmq-broker-subnetids"></a>
The list of groups \(2 maximum\) that define which subnets and IP ranges the broker can use from different Availability Zones\. A SINGLE\_INSTANCE deployment requires one subnet \(for example, the default subnet\)\. An ACTIVE\_STANDBY\_MULTI\_AZ deployment requires two subnets\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-amazonmq-broker-tags"></a>
An array of key\-value pairs\. For more information, see [Using Cost Allocation Tags](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/cost-alloc-tags.html) in the *AWS Billing and Cost Management User Guide*\.   
*Required*: No  
*Type*: List of [TagsEntry](aws-properties-amazonmq-broker-tagsentry.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Users`  <a name="cfn-amazonmq-broker-users"></a>
The list of ActiveMQ users \(persons or applications\) who can access queues and topics\. This value can contain only alphanumeric characters, dashes, periods, underscores, and tildes \(\- \. \_ \~\)\. This value must be 2\-100 characters long\.  
*Required*: Yes  
*Type*: List of [User](aws-properties-amazonmq-broker-user.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-amazonmq-broker-return-values"></a>

### Ref<a name="aws-resource-amazonmq-broker-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Amazon MQ broker ID\. For example: 

 `b-1234a5b6-78cd-901e-2fgh-3i45j6k178l9` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-amazonmq-broker-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-amazonmq-broker-return-values-fn--getatt-fn--getatt"></a>

`AmqpEndpoints`  <a name="AmqpEndpoints-fn::getatt"></a>
The AMQP endpoints of each broker instance as a list of strings\.  
 `amqp+ssl://b-4aada85d-a80c-4be0-9d30-e344a01b921e-1.mq.eu-central-amazonaws.com:5671` 

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the Amazon MQ broker\.  
 `arn:aws:mq:us-east-2:123456789012:broker:MyBroker:b-1234a5b6-78cd-901e-2fgh-3i45j6k178l9` 

`ConfigurationId`  <a name="ConfigurationId-fn::getatt"></a>
The unique ID that Amazon MQ generates for the configuration\.  
 `c-1234a5b6-78cd-901e-2fgh-3i45j6k178l9` 

`ConfigurationRevision`  <a name="ConfigurationRevision-fn::getatt"></a>
The revision number of the configuration\.  
 `1` 

`IpAddresses`  <a name="IpAddresses-fn::getatt"></a>
The IP addresses of each broker instance as a list of strings\.  
 `['198.51.100.2', '203.0.113.9']` 

`MqttEndpoints`  <a name="MqttEndpoints-fn::getatt"></a>
The MQTT endpoints of each broker instance as a list of strings\.  
 `mqtt+ssl://b-4aada85d-a80c-4be0-9d30-e344a01b921e-1.mq.eu-central-amazonaws.com:8883` 

`OpenWireEndpoints`  <a name="OpenWireEndpoints-fn::getatt"></a>
The OpenWire endpoints of each broker instance as a list of strings\.  
 `ssl://b-4aada85d-a80c-4be0-9d30-e344a01b921e-1.mq.eu-central-amazonaws.com:61617` 

`StompEndpoints`  <a name="StompEndpoints-fn::getatt"></a>
The STOMP endpoints of each broker instance as a list of strings\.  
 `stomp+ssl://b-4aada85d-a80c-4be0-9d30-e344a01b921e-1.mq.eu-central-amazonaws.com:61614` 

`WssEndpoints`  <a name="WssEndpoints-fn::getatt"></a>
The WSS endpoints of each broker instance as a list of strings\.  
 `wss://b-4aada85d-a80c-4be0-9d30-e344a01b921e-1.mq.eu-central-amazonaws.com:61619` 

## Examples<a name="aws-resource-amazonmq-broker--examples"></a>

### Basic Amazon MQ Broker<a name="aws-resource-amazonmq-broker--examples--Basic_Amazon_MQ_Broker"></a>

The following example creates a basic Amazon MQ broker with one user that belongs to a group\. 

#### JSON<a name="aws-resource-amazonmq-broker--examples--Basic_Amazon_MQ_Broker--json"></a>

```
{
  "Description": "Create a basic AmazonMQ broker",
  "Resources": {
    "BasicBroker": {
      "Type": "AWS::AmazonMQ::Broker",
      "Properties": {
        "AutoMinorVersionUpgrade": "false",
        "BrokerName": "MyBasicBroker",
        "DeploymentMode": "SINGLE_INSTANCE",
        "EngineType": "ActiveMQ",
        "EngineVersion": "5.15.0",
        "HostInstanceType": "mq.t2.micro",
        "PubliclyAccessible": "true",
        "Users": [
          {
            "ConsoleAccess": "true",
            "Groups": [
              "MyGroup"
            ],
            "Password" : { "Ref" : "AmazonMqPassword" },
            "Username" : { "Ref" : "AmazonMqUsername" }
          }
        ]
      }
    }
  }
}
```

#### YAML<a name="aws-resource-amazonmq-broker--examples--Basic_Amazon_MQ_Broker--yaml"></a>

```
--- 
Description: "Create a basic AmazonMQ broker"
Resources: 
  BasicBroker:
    Type: "AWS::AmazonMQ::Broker"
    Properties: 
      AutoMinorVersionUpgrade: "false"
      BrokerName: MyBasicBroker
      DeploymentMode: SINGLE_INSTANCE
      EngineType: ActiveMQ
      EngineVersion: "5.15.0"
      HostInstanceType: mq.t2.micro
      PubliclyAccessible: "true"
      Users: 
        - 
          ConsoleAccess: "true"
          Groups: 
            - MyGroup
          Password: 
            Ref: "BrokerPassword"            
          Username: 
            Ref: "BrokerUsername"
```

### Complex Amazon MQ Broker<a name="aws-resource-amazonmq-broker--examples--Complex_Amazon_MQ_Broker"></a>

The following example creates a complex Amazon MQ broker with two users that don't belong to a group and one user that belongs in a group\. 

#### JSON<a name="aws-resource-amazonmq-broker--examples--Complex_Amazon_MQ_Broker--json"></a>

```
{
  "Description": "Create a complex AmazonMQ broker",
  "Resources": {
    "ComplexBroker": {
      "Type": "AWS::AmazonMQ::Broker",
      "Properties": {
        "AutoMinorVersionUpgrade": "false",
        "BrokerName": "MyComplexBroker",
        "Configuration": {
          "Id": { "Ref": "Configuration1" },
          "Revision" : { "Fn::GetAtt": ["Configuration1", "Revision"] }
        },
        "DeploymentMode": "SINGLE_INSTANCE",
        "EngineType": "ActiveMQ",
        "EngineVersion": "5.15.0",
        "HostInstanceType": "mq.t2.micro",
        "Logs": {
            "General": true,
            "Audit": false
        },
        "MaintenanceWindowStartTime": {
          "DayOfWeek": "Monday",
          "TimeOfDay": "22:45",
          "TimeZone": "America/Los_Angeles"
        },
        "PubliclyAccessible": "true",
        "SecurityGroups": [
          "sg-a1b234cd",
          "sg-e5f678gh"
        ],
        "SubnetIds": [
          "subnet-12a3b45c",
          "subnet-67d8e90f"
        ],         
        "Users": [{
          "ConsoleAccess": "true",
          "Password" : { "Ref" : "AmazonMqPassword1" },
          "Username" : { "Ref" : "AmazonMqUsername1" }
        }, {
          "Password" : { "Ref" : "AmazonMqPassword2" },
          "Username" : { "Ref" : "AmazonMqUsername2" }
        }, {
          "Groups": [
            "MyGroup1",
            "MyGroup2"
          ],
          "Password" : { "Ref" : "AmazonMqPassword3" },          
          "Username" : { "Ref" : "AmazonMqUsername3" }
        }]
      }
    }
  }
}
```

#### YAML<a name="aws-resource-amazonmq-broker--examples--Complex_Amazon_MQ_Broker--yaml"></a>

```
Description: Create a complex AmazonMQ broker
Resources:
  ComplexBroker:
    Type: 'AWS::AmazonMQ::Broker'
    Properties:
      AutoMinorVersionUpgrade: 'false'
      BrokerName: MyComplexBroker
      Configuration:
        Id: !Ref Configuration1
        Revision: !GetAtt 
          - Configuration1
          - Revision
      DeploymentMode: SINGLE_INSTANCE
      EngineType: ActiveMQ
      EngineVersion: 5.15.0
      HostInstanceType: mq.t2.micro
      Logs:
        General: true
        Audit: false
      MaintenanceWindowStartTime:
        DayOfWeek: Monday
        TimeOfDay: '22:45'
        TimeZone: America/Los_Angeles
      PubliclyAccessible: 'true'
      SecurityGroups:
        - sg-a1b234cd
        - sg-e5f678gh
      SubnetIds:
        - subnet-12a3b45c
        - subnet-67d8e90f
      Users:
        - ConsoleAccess: 'true'
          Password: !Ref AmazonMqPassword1
          Username: !Ref AmazonMqUsername1
        - Password: !Ref AmazonMqPassword2
          Username: !Ref AmazonMqUsername2
        - Groups:
            - MyGroup1
            - MyGroup2
          Password: !Ref AmazonMqPassword3
          Username: !Ref AmazonMqUsername3
```