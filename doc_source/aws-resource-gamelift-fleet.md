# AWS::GameLift::Fleet<a name="aws-resource-gamelift-fleet"></a>

The `AWS::GameLift::Fleet` resource creates an Amazon GameLift \(GameLift\) fleet to host game servers\. A fleet is a set of EC2 instances, each of which can host multiple game sessions\.

## Syntax<a name="aws-resource-gamelift-fleet-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-gamelift-fleet-syntax.json"></a>

```
{
  "Type" : "AWS::GameLift::Fleet",
  "Properties" : {
      "[BuildId](#cfn-gamelift-fleet-buildid)" : String,
      "[CertificateConfiguration](#cfn-gamelift-fleet-certificateconfiguration)" : CertificateConfiguration,
      "[Description](#cfn-gamelift-fleet-description)" : String,
      "[DesiredEC2Instances](#cfn-gamelift-fleet-desiredec2instances)" : Integer,
      "[EC2InboundPermissions](#cfn-gamelift-fleet-ec2inboundpermissions)" : [ IpPermission, ... ],
      "[EC2InstanceType](#cfn-gamelift-fleet-ec2instancetype)" : String,
      "[FleetType](#cfn-gamelift-fleet-fleettype)" : String,
      "[InstanceRoleARN](#cfn-gamelift-fleet-instancerolearn)" : String,
      "[LogPaths](#cfn-gamelift-fleet-logpaths)" : [ String, ... ],
      "[MaxSize](#cfn-gamelift-fleet-maxsize)" : Integer,
      "[MetricGroups](#cfn-gamelift-fleet-metricgroups)" : [ String, ... ],
      "[MinSize](#cfn-gamelift-fleet-minsize)" : Integer,
      "[Name](#cfn-gamelift-fleet-name)" : String,
      "[NewGameSessionProtectionPolicy](#cfn-gamelift-fleet-newgamesessionprotectionpolicy)" : String,
      "[PeerVpcAwsAccountId](#cfn-gamelift-fleet-peervpcawsaccountid)" : String,
      "[PeerVpcId](#cfn-gamelift-fleet-peervpcid)" : String,
      "[ResourceCreationLimitPolicy](#cfn-gamelift-fleet-resourcecreationlimitpolicy)" : ResourceCreationLimitPolicy,
      "[RuntimeConfiguration](#cfn-gamelift-fleet-runtimeconfiguration)" : RuntimeConfiguration,
      "[ScriptId](#cfn-gamelift-fleet-scriptid)" : String,
      "[ServerLaunchParameters](#cfn-gamelift-fleet-serverlaunchparameters)" : String,
      "[ServerLaunchPath](#cfn-gamelift-fleet-serverlaunchpath)" : String
    }
}
```

### YAML<a name="aws-resource-gamelift-fleet-syntax.yaml"></a>

```
Type: AWS::GameLift::Fleet
Properties: 
  [BuildId](#cfn-gamelift-fleet-buildid): String
  [CertificateConfiguration](#cfn-gamelift-fleet-certificateconfiguration): 
    CertificateConfiguration
  [Description](#cfn-gamelift-fleet-description): String
  [DesiredEC2Instances](#cfn-gamelift-fleet-desiredec2instances): Integer
  [EC2InboundPermissions](#cfn-gamelift-fleet-ec2inboundpermissions): 
    - IpPermission
  [EC2InstanceType](#cfn-gamelift-fleet-ec2instancetype): String
  [FleetType](#cfn-gamelift-fleet-fleettype): String
  [InstanceRoleARN](#cfn-gamelift-fleet-instancerolearn): String
  [LogPaths](#cfn-gamelift-fleet-logpaths): 
    - String
  [MaxSize](#cfn-gamelift-fleet-maxsize): Integer
  [MetricGroups](#cfn-gamelift-fleet-metricgroups): 
    - String
  [MinSize](#cfn-gamelift-fleet-minsize): Integer
  [Name](#cfn-gamelift-fleet-name): String
  [NewGameSessionProtectionPolicy](#cfn-gamelift-fleet-newgamesessionprotectionpolicy): String
  [PeerVpcAwsAccountId](#cfn-gamelift-fleet-peervpcawsaccountid): String
  [PeerVpcId](#cfn-gamelift-fleet-peervpcid): String
  [ResourceCreationLimitPolicy](#cfn-gamelift-fleet-resourcecreationlimitpolicy): 
    ResourceCreationLimitPolicy
  [RuntimeConfiguration](#cfn-gamelift-fleet-runtimeconfiguration): 
    RuntimeConfiguration
  [ScriptId](#cfn-gamelift-fleet-scriptid): String
  [ServerLaunchParameters](#cfn-gamelift-fleet-serverlaunchparameters): String
  [ServerLaunchPath](#cfn-gamelift-fleet-serverlaunchpath): String
```

## Properties<a name="aws-resource-gamelift-fleet-properties"></a>

`BuildId`  <a name="cfn-gamelift-fleet-buildid"></a>
A unique identifier for a build to be deployed on the new fleet\. If you are deploying the fleet with a custom game build, you must specify this property\. The build must have been successfully uploaded to Amazon GameLift and be in a `READY` status\. This fleet setting cannot be changed once the fleet is created\.   
*Required*: Conditional  
*Type*: String  
*Pattern*: `^build-\S+|^arn:.*:build\/build-\S+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`CertificateConfiguration`  <a name="cfn-gamelift-fleet-certificateconfiguration"></a>
Indicates whether to generate a TLS/SSL certificate for the new fleet\. TLS certificates are used for encrypting traffic between game clients and game servers running on GameLift\. If this parameter is not set, certificate generation is disabled\. This fleet setting cannot be changed once the fleet is created\. Learn more at [Securing Client/Server Communication](https://docs.aws.amazon.com/gamelift/latest/developerguide/gamelift-howitworks.html#gamelift-howitworks-security)\.  
Note: This feature requires the AWS Certificate Manager \(ACM\) service, which is available in the AWS global partition but not in all other partitions\. When working in a partition that does not support this feature, a request for a new fleet with certificate generation results fails with a 4xx unsupported region error\.  
*Required*: No  
*Type*: [CertificateConfiguration](aws-properties-gamelift-fleet-certificateconfiguration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-gamelift-fleet-description"></a>
A human\-readable description of a fleet\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DesiredEC2Instances`  <a name="cfn-gamelift-fleet-desiredec2instances"></a>
The number of EC2 instances that you want this fleet to host\. When creating a new fleet, GameLift automatically sets this value to "1" and initiates a single instance\. Once the fleet is active, update this value to trigger GameLift to add or remove instances from the fleet\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EC2InboundPermissions`  <a name="cfn-gamelift-fleet-ec2inboundpermissions"></a>
A range of IP addresses and port settings that allow inbound traffic to connect to server processes on an Amazon GameLift server\.  
*Required*: No  
*Type*: List of [IpPermission](aws-properties-gamelift-fleet-ec2inboundpermission.md)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EC2InstanceType`  <a name="cfn-gamelift-fleet-ec2instancetype"></a>
The name of an EC2 instance type that is supported in Amazon GameLift\. A fleet instance type determines the computing resources of each instance in the fleet, including CPU, memory, storage, and networking capacity\. Amazon GameLift supports the following EC2 instance types\. See [Amazon EC2 Instance Types](http://aws.amazon.com/ec2/instance-types/) for detailed descriptions\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `c3.2xlarge | c3.4xlarge | c3.8xlarge | c3.large | c3.xlarge | c4.2xlarge | c4.4xlarge | c4.8xlarge | c4.large | c4.xlarge | c5.12xlarge | c5.18xlarge | c5.24xlarge | c5.2xlarge | c5.4xlarge | c5.9xlarge | c5.large | c5.xlarge | c5a.12xlarge | c5a.16xlarge | c5a.24xlarge | c5a.2xlarge | c5a.4xlarge | c5a.8xlarge | c5a.large | c5a.xlarge | m3.2xlarge | m3.large | m3.medium | m3.xlarge | m4.10xlarge | m4.2xlarge | m4.4xlarge | m4.large | m4.xlarge | m5.12xlarge | m5.16xlarge | m5.24xlarge | m5.2xlarge | m5.4xlarge | m5.8xlarge | m5.large | m5.xlarge | m5a.12xlarge | m5a.16xlarge | m5a.24xlarge | m5a.2xlarge | m5a.4xlarge | m5a.8xlarge | m5a.large | m5a.xlarge | r3.2xlarge | r3.4xlarge | r3.8xlarge | r3.large | r3.xlarge | r4.16xlarge | r4.2xlarge | r4.4xlarge | r4.8xlarge | r4.large | r4.xlarge | r5.12xlarge | r5.16xlarge | r5.24xlarge | r5.2xlarge | r5.4xlarge | r5.8xlarge | r5.large | r5.xlarge | r5a.12xlarge | r5a.16xlarge | r5a.24xlarge | r5a.2xlarge | r5a.4xlarge | r5a.8xlarge | r5a.large | r5a.xlarge | t2.large | t2.medium | t2.micro | t2.small`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FleetType`  <a name="cfn-gamelift-fleet-fleettype"></a>
Indicates whether to use On\-Demand instances or Spot instances for this fleet\. If empty, the default is `ON_DEMAND`\. Both categories of instances use identical hardware and configurations based on the instance type selected for this fleet\. Learn more about [ On\-Demand versus Spot Instances](https://docs.aws.amazon.com/gamelift/latest/developerguide/gamelift-ec2-instances.html#gamelift-ec2-instances-spot)\.   
*Required*: No  
*Type*: String  
*Allowed values*: `ON_DEMAND | SPOT`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InstanceRoleARN`  <a name="cfn-gamelift-fleet-instancerolearn"></a>
A unique identifier for an AWS IAM role that manages access to your AWS services\. With an instance role ARN set, any application that runs on an instance in this fleet can assume the role, including install scripts, server processes, and daemons \(background processes\)\. Create a role or look up a role's ARN from the [IAM dashboard](https://console.aws.amazon.com/iam/) in the AWS Management Console\. Learn more about using on\-box credentials for your game servers at [ Access external resources from a game server](https://docs.aws.amazon.com/gamelift/latest/developerguide/gamelift-sdk-server-resources.html)\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LogPaths`  <a name="cfn-gamelift-fleet-logpaths"></a>
This parameter is no longer used\. When hosting a custom game build, specify where Amazon GameLift should store log files using the Amazon GameLift server API call `ProcessReady()`\. See more information in the [Server API Reference](https://docs.aws.amazon.com/gamelift/latest/developerguide/gamelift-sdk-server-api-ref.html#gamelift-sdk-server-api-ref-dataypes-process)\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MaxSize`  <a name="cfn-gamelift-fleet-maxsize"></a>
The maximum value that is allowed for the fleet's instance count\. When creating a new fleet, GameLift automatically sets this value to "1"\. Once the fleet is active, you can change this value\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricGroups`  <a name="cfn-gamelift-fleet-metricgroups"></a>
The name of an Amazon CloudWatch metric group\. A metric group aggregates the metrics for all fleets in the group\. Specify a string containing the metric group name\. You can use an existing name or use a new name to create a new metric group\. Currently, this parameter can have only one string\.   
*Required*: No  
*Type*: List of String  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinSize`  <a name="cfn-gamelift-fleet-minsize"></a>
The minimum value allowed for the fleet's instance count\. When creating a new fleet, GameLift automatically sets this value to "0"\. After the fleet is active, you can change this value\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-gamelift-fleet-name"></a>
A descriptive label that is associated with a fleet\. Fleet names do not need to be unique\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NewGameSessionProtectionPolicy`  <a name="cfn-gamelift-fleet-newgamesessionprotectionpolicy"></a>
A game session protection policy to apply to all game sessions hosted on instances in this fleet\. When protected, active game sessions cannot be terminated during a scale\-down event\. If this parameter is not set, instances in this fleet default to no protection\. You can change a fleet's protection policy to affect future game sessions on the fleet\. You can also set protection for individual game sessions\.  
*Required*: No  
*Type*: String  
*Allowed values*: `FullProtection | NoProtection`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PeerVpcAwsAccountId`  <a name="cfn-gamelift-fleet-peervpcawsaccountid"></a>
A unique identifier for the AWS account with the VPC that you want to peer your Amazon GameLift fleet with\. You can find your account ID in the AWS Management Console under account settings\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PeerVpcId`  <a name="cfn-gamelift-fleet-peervpcid"></a>
A unique identifier for a VPC with resources to be accessed by your Amazon GameLift fleet\. The VPC must be in the same Region as your fleet\. To look up a VPC ID, use the [VPC Dashboard](https://console.aws.amazon.com/vpc/) in the AWS Management Console\. Learn more about VPC peering in [VPC Peering with Amazon GameLift Fleets](https://docs.aws.amazon.com/gamelift/latest/developerguide/vpc-peering.html)\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ResourceCreationLimitPolicy`  <a name="cfn-gamelift-fleet-resourcecreationlimitpolicy"></a>
A policy that limits the number of game sessions an individual player can create over a span of time for this fleet\.  
*Required*: No  
*Type*: [ResourceCreationLimitPolicy](aws-properties-gamelift-fleet-resourcecreationlimitpolicy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RuntimeConfiguration`  <a name="cfn-gamelift-fleet-runtimeconfiguration"></a>
Instructions for launching server processes on each instance in the fleet\. Server processes run either a custom game build executable or a Realtime script\. The runtime configuration defines the server executables or launch script file, launch parameters, and the number of processes to run concurrently on each instance\. When creating a fleet, the runtime configuration must have at least one server process configuration; otherwise the request fails with an invalid request exception\.  
This parameter is required unless the parameters `ServerLaunchPath` and `ServerLaunchParameters` are defined\. Runtime configuration has replaced these parameters, but fleets that use them will continue to work\.   
*Required*: Conditional  
*Type*: [RuntimeConfiguration](aws-properties-gamelift-fleet-runtimeconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScriptId`  <a name="cfn-gamelift-fleet-scriptid"></a>
A unique identifier for a Realtime script to be deployed on a new Realtime Servers fleet\. The script must have been successfully uploaded to Amazon GameLift\. This fleet setting cannot be changed once the fleet is created\.  
Note: It is not currently possible to use the `!Ref` command to reference a script created with a CloudFormation template for the fleet property `ScriptId`\. Instead, use `Fn::GetAtt Script.Arn` or `Fn::GetAtt Script.Id` to retrieve either of these properties as input for `ScriptId`\. Alternatively, enter a `ScriptId` string manually\.  
*Required*: Conditional  
*Type*: String  
*Pattern*: `^script-\S+|^arn:.*:script\/script-\S+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ServerLaunchParameters`  <a name="cfn-gamelift-fleet-serverlaunchparameters"></a>
This parameter is no longer used but is retained for backward compatibility\. Instead, specify server launch parameters in the `RuntimeConfiguration` parameter\. A request must specify either a runtime configuration or values for both ServerLaunchParameters and ServerLaunchPath\.  
*Required*: Conditional  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ServerLaunchPath`  <a name="cfn-gamelift-fleet-serverlaunchpath"></a>
This parameter is no longer used\. Instead, specify a server launch path using the `RuntimeConfiguration` parameter\. Requests that specify a server launch path and launch parameters instead of a runtime configuration will continue to work\.  
*Required*: Conditional  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-gamelift-fleet-return-values"></a>

### Ref<a name="aws-resource-gamelift-fleet-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the fleet ID, such as `fleet-1111aaaa-22bb-33cc-44dd-5555eeee66ff`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-gamelift-fleet--examples"></a>



### Create GameLift fleet with a Build<a name="aws-resource-gamelift-fleet--examples--Create_GameLift_fleet_with_a_Build"></a>

The following example creates and configures a GameLift fleet for a custom game build\. The fleet uses a `Ref` intrinsic function to specify a build, which can be declared elsewhere in the same template\. The example syntax for log path and server launch path uses values for a Windows build\.

Note: the JSON example shows how to escape the slashes \(`\\`\)\.

#### JSON<a name="aws-resource-gamelift-fleet--examples--Create_GameLift_fleet_with_a_Build--json"></a>

```
{
    "Resources": {
        "FleetResource": {
            "Type": "AWS::GameLift::Fleet",
            "Properties": {
                "BuildId": {
                    "Ref": "BuildResource"
                },
                "CertificateConfiguration": {
                    "CertificateType": "DISABLED"
                },
                "Description": "Description of my Fleet",
                "DesiredEc2Instances": 1,
                "EC2InboundPermissions": [
                    {
                        "FromPort": "1234",
                        "ToPort": "1324",
                        "IpRange": "0.0.0.0/24",
                        "Protocol": "TCP"
                    },
                    {
                        "FromPort": "1356",
                        "ToPort": "1578",
                        "IpRange": "192.168.0.0/24",
                        "Protocol": "UDP"
                    }
                ],
                "EC2InstanceType": "c4.large",
                "FleetType": "SPOT",
                "LogPaths": [
                    "c:\\game\\testlog.log",
                    "c:\\game\\testlog2.log"
                ],
                "MetricGroups": [
                    "MetricGroupName"
                ],
                "Name": "MyGameFleet",
                "NewGameSessionProtectionPolicy": "FullProtection",
                "ResourceCreationLimitPolicy": {
                    "NewGameSessionsPerCreator": 5,
                    "PolicyPeriodInMinutes": 2
                },
                "RuntimeConfiguration": {
                    "GameSessionActivationTimeoutSeconds": 300,
                    "MaxConcurrentGameSessionActivations": 1,
                    "ServerProcesses": [
                        {
                            "ConcurrentExecutions": 1,
                            "LaunchPath": "c:\\game\\TestApplicationServer.exe"
                        }
                    ]
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-gamelift-fleet--examples--Create_GameLift_fleet_with_a_Build--yaml"></a>

```
Resources:
  FleetResource:
    Type: AWS::GameLift::Fleet    
    Properties:
      BuildId: !Ref BuildResource
      CertificateConfiguration:
        CertificateType: DISABLED
      Description: Description of my Game Fleet
      DesiredEc2Instances: 1
      EC2InboundPermissions:
        - FromPort: '1234'
          ToPort: '1324'
          IpRange: 0.0.0.0/24
          Protocol: TCP
        - FromPort: '1356'
          ToPort: '1578'
          IpRange: 192.168.0.0/24
          Protocol: UDP
      EC2InstanceType: c4.large
      FleetType: SPOT
      LogPaths:
        - c:\game\testlog.log
        - c:\game\testlog2.log      
      MetricGroups: 
        - MetricGroupName
      Name: MyGameFleet
      NewGameSessionProtectionPolicy: FullProtection      
      ResourceCreationLimitPolicy:
        NewGameSessionsPerCreator: 5
        PolicyPeriodInMinutes: 2
      RuntimeConfiguration:
        GameSessionActivationTimeoutSeconds: 300
        MaxConcurrentGameSessionActivations: 1
        ServerProcesses:
          - ConcurrentExecutions: 1
            LaunchPath: c:\game\TestApplicationServer.exe
```

### Create GameLift fleet with a Script<a name="aws-resource-gamelift-fleet--examples--Create_GameLift_fleet_with_a_Script"></a>

The following example creates and configures a GameLift fleet to run Realtime Servers\. The fleet uses a `GetAtt` intrinsic function to specify a script, which can be declared elsewhere in the same template\. Note that the syntax example for the log path and server launch path are for Linux, as all Realtime Servers are deployed with Linux\.

#### JSON<a name="aws-resource-gamelift-fleet--examples--Create_GameLift_fleet_with_a_Script--json"></a>

```
{
    "Resources": {
        "FleetResource": {
            "Type": "AWS::GameLift::Fleet",
            "Properties": {
                "CertificateConfiguration": {
                    "CertificateType": "DISABLED"
                },
                "Description": "Description of my Game Fleet",
                "DesiredEC2Instances": 1,
                "EC2InboundPermissions": [
                    {
                        "FromPort": "1234",
                        "ToPort": "1324",
                        "IpRange": "0.0.0.0/24",
                        "Protocol": "TCP"
                    },
                    {
                        "FromPort": "1356",
                        "ToPort": "1578",
                        "IpRange": "192.168.0.0/24",
                        "Protocol": "UDP"
                    }
                ],
                "EC2InstanceType": "c4.large",
                "FleetType": "SPOT",
                "LogPaths": [
                    "/local/game/testlog.log",
                    "/local/game/testlog2.log"
                ],
                "MetricGroups": [
                    "MetricGroupName"
                ],
                "Name": "MyGameFleet",
                "NewGameSessionProtectionPolicy": "FullProtection",
                "ResourceCreationLimitPolicy": {
                    "NewGameSessionsPerCreator": 5,
                    "PolicyPeriodInMinutes": 2
                },
                "RuntimeConfiguration": {
                    "GameSessionActivationTimeoutSeconds": 300,
                    "MaxConcurrentGameSessionActivations": 1,
                    "ServerProcesses": [
                        {
                            "ConcurrentExecutions": 1,
                            "LaunchPath": "/local/game/myscript.js"
                        }
                    ]
                },
                "ScriptId": {
                    "Fn::GetAtt": [
                        "ScriptResource",
                        "Id"
                    ]
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-gamelift-fleet--examples--Create_GameLift_fleet_with_a_Script--yaml"></a>

```
Resources:    
  FleetResource:
    Type: AWS::GameLift::Fleet    
    Properties:      
      CertificateConfiguration:
        CertificateType: DISABLED
      Description: Description of my game fleet
      DesiredEC2Instances: 1     
      EC2InboundPermissions:
        - FromPort: '1234'
          ToPort: '1324'
          IpRange: 0.0.0.0/24
          Protocol: TCP
        - FromPort: '1356'
          ToPort: '1578'
          IpRange: 192.168.0.0/24
          Protocol: UDP
      EC2InstanceType: c4.large
      FleetType: SPOT
      LogPaths:
        - '/local/game/testlog.log'
        - '/local/game/testlog2.log'
      MetricGroups: 
        - MetricGroupName
      Name: MyGameFleet
      NewGameSessionProtectionPolicy: FullProtection      
      ResourceCreationLimitPolicy:
        NewGameSessionsPerCreator: 5
        PolicyPeriodInMinutes: 2
      RuntimeConfiguration:
        GameSessionActivationTimeoutSeconds: 300
        MaxConcurrentGameSessionActivations: 1
        ServerProcesses:
          - ConcurrentExecutions: 1
            LaunchPath: '/local/game/myscript.js'
      ScriptId: !GetAtt ScriptResource.Id
```

## See also<a name="aws-resource-gamelift-fleet--seealso"></a>
+ [ Create GameLift Resources Using AWS CloudFormation](https://docs.aws.amazon.com/gamelift/latest/developerguide/resources-cloudformation.html) in the *Amazon GameLift Developer Guide*
+  [Setting Up GameLift Fleets](https://docs.aws.amazon.com/gamelift/latest/developerguide/fleets-intro.html) in the *Amazon GameLift Developer Guide* 
+ [CreateFleet](https://docs.aws.amazon.com/gamelift/latest/apireference/API_CreateFleet.html) in the *Amazon GameLift API Reference* 

