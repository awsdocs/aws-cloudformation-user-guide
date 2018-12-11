# AWS::AmazonMQ::Broker<a name="aws-resource-amazonmq-broker"></a>

A *broker* is a message broker environment running on Amazon MQ\. It is the basic building block of Amazon MQ\.

The `AWS::AmazonMQ::Broker` resource lets you create Amazon MQ brokers, add configuration changes or modify users for the specified broker, return information about the specified broker, and delete the specified broker\. For more information, see [Amazon MQ Basic Elements](https://docs.aws.amazon.com/amazon-mq/latest/developer-guide/amazon-mq-basic-elements.html) in the *Amazon MQ Developer Guide*\.

## Syntax<a name="aws-resource-amazonmq-broker-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-amazonmq-broker-syntax.json"></a>

```
{
  "Type" : "AWS::AmazonMQ::Broker",
  "Properties" : {
    "[AutoMinorVersionUpgrade](#cfn-amazonmq-broker-autominorversionupgrade)" : Boolean,
    "[BrokerName](#cfn-amazonmq-broker-brokername)" : String,  
    "[Users](#cfn-amazonmq-broker-users)" : [ [User](aws-properties-amazonmq-broker-user.md), ... ],
    "[Configuration](#cfn-amazonmq-broker-configuration)" : [ConfigurationId](aws-properties-amazonmq-broker-configurationid.md),
    "[DeploymentMode](#cfn-amazonmq-broker-deploymentmode)" : String,
    "[EngineType](#cfn-amazonmq-broker-enginetype)" : String,
    "[EngineVersion](#cfn-amazonmq-broker-engineversion)" : String,
    "[HostInstanceType](#cfn-amazonmq-broker-hostinstancetype)" : String,
    "[Logs](#cfn-amazonmq-broker-logs)" : [LogsConfiguration](aws-properties-amazonmq-broker-logsconfiguration.md),
    "[MaintenanceWindowStartTime](#cfn-amazonmq-broker-maintenancewindowstarttime)" : [MaintenanceWindow](aws-properties-amazonmq-broker-maintenancewindow.md),
    "[PubliclyAccessible](#cfn-amazonmq-broker-publiclyaccessible)" : Boolean,
    "[SecurityGroups](#cfn-amazonmq-broker-securitygroups)" : [ String, ... ],
    "[SubnetIds](#cfn-amazonmq-broker-subnetids)" : [ String, ... ]
  }
}
```

### YAML<a name="aws-resource-amazonmq-broker-syntax.yaml"></a>

```
Type: "AWS::AmazonMQ::Broker"
Properties:
  [AutoMinorVersionUpgrade](#cfn-amazonmq-broker-autominorversionupgrade): Boolean
  [BrokerName](#cfn-amazonmq-broker-brokername): String
  [Users](#cfn-amazonmq-broker-users): 
    - [User](aws-properties-amazonmq-broker-user.md)
  [Configuration](#cfn-amazonmq-broker-configuration): [ConfigurationId](aws-properties-amazonmq-broker-configurationid.md)
  [DeploymentMode](#cfn-amazonmq-broker-deploymentmode): String
  [EngineType](#cfn-amazonmq-broker-enginetype): String
  [EngineVersion](#cfn-amazonmq-broker-engineversion): String
  [HostInstanceType](#cfn-amazonmq-broker-hostinstancetype): String
  [Logs](#cfn-amazonmq-broker-logs): [LogsConfiguration](aws-properties-amazonmq-broker-logsconfiguration.md)
  [MaintenanceWindowStartTime](#cfn-amazonmq-broker-maintenancewindowstarttime): [MaintenanceWindow](aws-properties-amazonmq-broker-maintenancewindow.md)
  [PubliclyAccessible](#cfn-amazonmq-broker-publiclyaccessible): Boolean              
  [SecurityGroups](#cfn-amazonmq-broker-securitygroups): 
    - String
  [SubnetIds](#cfn-amazonmq-broker-subnetids): 
    - String
```

## Properties<a name="aws-resource-amazonmq-broker-properties"></a>

`AutoMinorVersionUpgrade`  <a name="cfn-amazonmq-broker-autominorversionupgrade"></a>
Enables automatic upgrades to new minor versions for brokers, as Apache releases the versions\. The automatic upgrades occur during the maintenance window of the broker or after a manual broker reboot\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`BrokerName`  <a name="cfn-amazonmq-broker-brokername"></a>
The name of the broker\. This value must be unique in your AWS account, 1\-50 characters long, must contain only letters, numbers, dashes, and underscores, and must not contain whitespaces, brackets, wildcard characters, or special characters\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Users`  <a name="cfn-amazonmq-broker-users"></a>
The list of all ActiveMQ usernames for the specified broker\.  
*Required*: Yes  
*Type*: List of [User](aws-properties-amazonmq-broker-user.md) property types  
*Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)

`Configuration`  <a name="cfn-amazonmq-broker-configuration"></a>
The broker configuration\. If no configuration exists for a broker, Amazon MQ creates a default configuration\.  
You can use AWS CloudFormation to modify—but not delete—an Amazon MQ configuration\.
*Required*: No  
*Type*: [ConfigurationId](aws-properties-amazonmq-broker-configurationid.md)  
*Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)

`DeploymentMode`  <a name="cfn-amazonmq-broker-deploymentmode"></a>
The deployment mode of the broker\. `SINGLE_INSTANCE` creates a single\-instance broker in a single Availability Zone\. `ACTIVE_STANDBY_MULTI_AZ` creates an active/standby broker for high availability\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`EngineType`  <a name="cfn-amazonmq-broker-enginetype"></a>
The type of broker engine\.  
Currently, Amazon MQ supports only `ACTIVEMQ`\.
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`EngineVersion`  <a name="cfn-amazonmq-broker-engineversion"></a>
The version of the broker engine\.  
For a list of supported engine versions, see: [Broker Engine](https://docs.aws.amazon.com/amazon-mq/latest/developer-guide/broker-engine.html)\.
*Required*: Yes  
*Type*: String  
*Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)

`HostInstanceType`  <a name="cfn-amazonmq-broker-hostinstancetype"></a>
The broker's instance type\. For more information, see [Instance Types](https://docs.aws.amazon.com/amazon-mq/latest/developer-guide/broker.html#broker-instance-types) in the *Amazon MQ Developer Guide*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Logs`  <a name="cfn-amazonmq-broker-logs"></a>
The Amazon CloudWatch Logs configuration for the broker\.  
*Required*: No  
*Type*: [LogsConfiguration](aws-properties-amazonmq-broker-logsconfiguration.md)  
*Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)

`MaintenanceWindowStartTime`  <a name="cfn-amazonmq-broker-maintenancewindowstarttime"></a>
The parameters that determine the `WeeklyStartTime`\.  
*Required*: No  
*Type*: [MaintenanceWindow](aws-properties-amazonmq-broker-maintenancewindow.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`PubliclyAccessible`  <a name="cfn-amazonmq-broker-publiclyaccessible"></a>
Enables connections from applications outside of the VPC that hosts the broker's subnets\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`SecurityGroups`  <a name="cfn-amazonmq-broker-securitygroups"></a>
The list of rules \(1 minimum, 125 maximum\) that authorize connections to brokers\.  
*Required*: No  
*Type*: List of String values  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`SubnetIds`  <a name="cfn-amazonmq-broker-subnetids"></a>
The list of groups \(2 maximum\) that define which subnets and IP ranges the broker can use from different Availability Zones\. A `SINGLE_INSTANCE` deployment requires one subnet \(for example, the default subnet\)\. An `ACTIVE_STANDBY_MULTI_AZ` deployment requires two subnets\.   
*Required*: No  
*Type*: List of String values  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Values<a name="aws-resource-amazonmq-broker-returnvalues"></a>

### Ref<a name="aws-resource-amazonmq-broker-ref"></a>

When you pass the logical ID of an `AWS::AmazonMQ::Broker` resource to the intrinsic `Ref` function, the function returns the Amazon MQ broker ID\. For example:

```
b-1234a5b6-78cd-901e-2fgh-3i45j6k178l9
```

For more information about using the `Ref` function, see `[Ref](intrinsic-function-reference-ref.md)`\.

### Fn::GetAtt<a name="aws-resource-amazonmq-broker-getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

`Arn`  
The Amazon Resource Name \(ARN\) of the Amazon MQ broker\.  

```
arn:aws:mq:us-east-2:123456789012:broker:MyBroker:b-1234a5b6-78cd-901e-2fgh-3i45j6k178l9
```

`ConfigurationId`  
The unique ID that Amazon MQ generates for the configuration\.  

```
c-1234a5b6-78cd-901e-2fgh-3i45j6k178l9
```

`ConfigurationRevision`  
The revision number of the configuration\.  

```
1
```

For more information about using `Fn::GetAtt`, see `[Fn::GetAtt](intrinsic-function-reference-getatt.md)`\.

## Examples<a name="aws-resource-amazonmq-broker-examples"></a>

### Basic Amazon MQ Broker<a name="aws-resource-amazonmq-broker-example-simple"></a>

The following example creates a basic Amazon MQ broker with one user that belongs to a group\.

**Note**  
We don't recommend including plaintext passwords in AWS CloudFormation templates\. To securely retrieve your user credentials, add a `Ref` to your template\. For example, you can create a Lambda function and use it to retrieve encrypted credentials stored in a DynamoDB table\. For more information, see [Using AWS Lambda with Amazon DynamoDB](https://docs.aws.amazon.com/lambda/latest/dg/with-ddb.html) in the *AWS Lambda Developer Guide*\.

#### JSON<a name="aws-resource-amazonmq-broker-example-simple.json"></a>

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

#### YAML<a name="aws-resource-amazonmq-broker-example-simple.yaml"></a>

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

### Complex Amazon MQ Broker<a name="aws-resource-amazonmq-broker-example-complex"></a>

The following example creates a complex Amazon MQ broker with two users that don't belong to a group and one user that belongs in a group\.

**Note**  
We don't recommend including plaintext passwords in AWS CloudFormation templates\. To securely retrieve your user credentials, add a `Ref` to your template\. For example, you can create a Lambda function and use it to retrieve encrypted credentials stored in a DynamoDB table\. For more information, see [Using AWS Lambda with Amazon DynamoDB](https://docs.aws.amazon.com/lambda/latest/dg/with-ddb.html) in the *AWS Lambda Developer Guide*\.

#### JSON<a name="aws-resource-amazonmq-broker-example-complex.json"></a>

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

#### YAML<a name="aws-resource-amazonmq-broker-example-complex.yaml"></a>

```
--- 
Description: "Create a complex AmazonMQ broker"
Resources: 
  ComplexBroker:
    Type: "AWS::AmazonMQ::Broker"
    Properties: 
      AutoMinorVersionUpgrade: "false"
      BrokerName: MyComplexBroker
      Configuration: 
        Id: !GetAtt Configuration1.Id
        Revision: !GetAtt Configuration1.Revision
      DeploymentMode: SINGLE_INSTANCE
      EngineType: ActiveMQ
      EngineVersion: "5.15.0"
      HostInstanceType: mq.t2.micro
      Logs:
        General: "true"
        Audit: "false"
      MaintenanceWindowStartTime: 
        DayOfWeek: Monday
        TimeOfDay: "22:45"
        TimeZone: America/Los_Angeles
      PubliclyAccessible: "true"
      SecurityGroups:
        - "sg-a1b234cd"
        - "sg-e5f678gh"
      SubnetIds:
        - "subnet-12a3b45c"
        - "subnet-67d8e90f"
      Users: 
        - 
          ConsoleAccess: "true"
          Password: 
            Ref: "BrokerPassword1"
          Username: 
            Ref: "BrokerUsername1"
        - 
          Password: 
            Ref: "BrokerPassword2"
          Username: 
            Ref: "BrokerUsername2"
        - 
          Groups: 
            - MyGroup1
            - MyGroup2
          Password: 
            Ref: "BrokerPassword3"
          Username: 
            Ref: "BrokerUsername3"
```