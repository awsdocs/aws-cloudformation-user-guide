# AWS::GameLift::Fleet<a name="aws-resource-gamelift-fleet"></a>

The `AWS::GameLift::Fleet` resource creates an Amazon GameLift \(GameLift\) fleet to host game servers\. A fleet is a set of EC2 instances, each of which can host multiple game sessions\.

## Syntax<a name="aws-resource-gamelift-fleet-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-gamelift-fleet-syntax.json"></a>

```
{
  "Type" : "AWS::GameLift::Fleet",
  "Properties" : {
      "[AnywhereConfiguration](#cfn-gamelift-fleet-anywhereconfiguration)" : AnywhereConfiguration,
      "[BuildId](#cfn-gamelift-fleet-buildid)" : String,
      "[CertificateConfiguration](#cfn-gamelift-fleet-certificateconfiguration)" : CertificateConfiguration,
      "[ComputeType](#cfn-gamelift-fleet-computetype)" : String,
      "[Description](#cfn-gamelift-fleet-description)" : String,
      "[DesiredEC2Instances](#cfn-gamelift-fleet-desiredec2instances)" : Integer,
      "[EC2InboundPermissions](#cfn-gamelift-fleet-ec2inboundpermissions)" : [ IpPermission, ... ],
      "[EC2InstanceType](#cfn-gamelift-fleet-ec2instancetype)" : String,
      "[FleetType](#cfn-gamelift-fleet-fleettype)" : String,
      "[InstanceRoleARN](#cfn-gamelift-fleet-instancerolearn)" : String,
      "[Locations](#cfn-gamelift-fleet-locations)" : [ LocationConfiguration, ... ],
      "[MaxSize](#cfn-gamelift-fleet-maxsize)" : Integer,
      "[MetricGroups](#cfn-gamelift-fleet-metricgroups)" : [ String, ... ],
      "[MinSize](#cfn-gamelift-fleet-minsize)" : Integer,
      "[Name](#cfn-gamelift-fleet-name)" : String,
      "[NewGameSessionProtectionPolicy](#cfn-gamelift-fleet-newgamesessionprotectionpolicy)" : String,
      "[PeerVpcAwsAccountId](#cfn-gamelift-fleet-peervpcawsaccountid)" : String,
      "[PeerVpcId](#cfn-gamelift-fleet-peervpcid)" : String,
      "[ResourceCreationLimitPolicy](#cfn-gamelift-fleet-resourcecreationlimitpolicy)" : ResourceCreationLimitPolicy,
      "[RuntimeConfiguration](#cfn-gamelift-fleet-runtimeconfiguration)" : RuntimeConfiguration,
      "[ScriptId](#cfn-gamelift-fleet-scriptid)" : String
    }
}
```

### YAML<a name="aws-resource-gamelift-fleet-syntax.yaml"></a>

```
Type: AWS::GameLift::Fleet
Properties: 
  [AnywhereConfiguration](#cfn-gamelift-fleet-anywhereconfiguration): 
    AnywhereConfiguration
  [BuildId](#cfn-gamelift-fleet-buildid): String
  [CertificateConfiguration](#cfn-gamelift-fleet-certificateconfiguration): 
    CertificateConfiguration
  [ComputeType](#cfn-gamelift-fleet-computetype): String
  [Description](#cfn-gamelift-fleet-description): String
  [DesiredEC2Instances](#cfn-gamelift-fleet-desiredec2instances): Integer
  [EC2InboundPermissions](#cfn-gamelift-fleet-ec2inboundpermissions): 
    - IpPermission
  [EC2InstanceType](#cfn-gamelift-fleet-ec2instancetype): String
  [FleetType](#cfn-gamelift-fleet-fleettype): String
  [InstanceRoleARN](#cfn-gamelift-fleet-instancerolearn): String
  [Locations](#cfn-gamelift-fleet-locations): 
    - LocationConfiguration
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
```

## Properties<a name="aws-resource-gamelift-fleet-properties"></a>

`AnywhereConfiguration`  <a name="cfn-gamelift-fleet-anywhereconfiguration"></a>
Property description not available\.  
*Required*: No  
*Type*: [AnywhereConfiguration](aws-properties-gamelift-fleet-anywhereconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BuildId`  <a name="cfn-gamelift-fleet-buildid"></a>
A unique identifier for a build to be deployed on the new fleet\. If you are deploying the fleet with a custom game build, you must specify this property\. The build must have been successfully uploaded to Amazon GameLift and be in a `READY` status\. This fleet setting cannot be changed once the fleet is created\.   
*Required*: Conditional  
*Type*: String  
*Pattern*: `^build-\S+|^arn:.*:build\/build-\S+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`CertificateConfiguration`  <a name="cfn-gamelift-fleet-certificateconfiguration"></a>
Prompts GameLift to generate a TLS/SSL certificate for the fleet\. GameLift uses the certificates to encrypt traffic between game clients and the game servers running on GameLift\. By default, the `CertificateConfiguration` is `DISABLED`\. You can't change this property after you create the fleet\.   
 AWS Certificate Manager \(ACM\) certificates expire after 13 months\. Certificate expiration can cause fleets to fail, preventing players from connecting to instances in the fleet\. We recommend you replace fleets before 13 months, consider using fleet aliases for a smooth transition\.  
ACM isn't available in all AWS regions\. A fleet creation request with certificate generation enabled in an unsupported Region, fails with a 4xx error\. For more information about the supported Regions, see [Supported Regions](https://docs.aws.amazon.com/acm/latest/userguide/acm-regions.html) in the * AWS Certificate Manager User Guide*\.
*Required*: No  
*Type*: [CertificateConfiguration](aws-properties-gamelift-fleet-certificateconfiguration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ComputeType`  <a name="cfn-gamelift-fleet-computetype"></a>
The type of compute resource used to host your game servers\. You can use your own compute resources with GameLift Anywhere or use Amazon EC2 instances with managed GameLift\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ANYWHERE | EC2`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-gamelift-fleet-description"></a>
A description for the fleet\.  
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
The allowed IP address ranges and port settings that allow inbound traffic to access game sessions on this fleet\. If the fleet is hosting a custom game build, this property must be set before players can connect to game sessions\. For Realtime Servers fleets, GameLift automatically sets TCP and UDP ranges\.   
*Required*: No  
*Type*: List of [IpPermission](aws-properties-gamelift-fleet-ippermission.md)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EC2InstanceType`  <a name="cfn-gamelift-fleet-ec2instancetype"></a>
The GameLift\-supported Amazon EC2 instance type to use for all fleet instances\. Instance type determines the computing resources that will be used to host your game servers, including CPU, memory, storage, and networking capacity\. See [Amazon Elastic Compute Cloud Instance Types](http://aws.amazon.com/ec2/instance-types/) for detailed descriptions of Amazon EC2 instance types\.  
*Required*: No  
*Type*: String  
*Allowed values*: `c3.2xlarge | c3.4xlarge | c3.8xlarge | c3.large | c3.xlarge | c4.2xlarge | c4.4xlarge | c4.8xlarge | c4.large | c4.xlarge | c5.12xlarge | c5.18xlarge | c5.24xlarge | c5.2xlarge | c5.4xlarge | c5.9xlarge | c5.large | c5.xlarge | c5a.12xlarge | c5a.16xlarge | c5a.24xlarge | c5a.2xlarge | c5a.4xlarge | c5a.8xlarge | c5a.large | c5a.xlarge | c5d.12xlarge | c5d.18xlarge | c5d.24xlarge | c5d.2xlarge | c5d.4xlarge | c5d.9xlarge | c5d.large | c5d.xlarge | c6a.12xlarge | c6a.16xlarge | c6a.24xlarge | c6a.2xlarge | c6a.4xlarge | c6a.8xlarge | c6a.large | c6a.xlarge | c6i.12xlarge | c6i.16xlarge | c6i.24xlarge | c6i.2xlarge | c6i.4xlarge | c6i.8xlarge | c6i.large | c6i.xlarge | m3.2xlarge | m3.large | m3.medium | m3.xlarge | m4.10xlarge | m4.2xlarge | m4.4xlarge | m4.large | m4.xlarge | m5.12xlarge | m5.16xlarge | m5.24xlarge | m5.2xlarge | m5.4xlarge | m5.8xlarge | m5.large | m5.xlarge | m5a.12xlarge | m5a.16xlarge | m5a.24xlarge | m5a.2xlarge | m5a.4xlarge | m5a.8xlarge | m5a.large | m5a.xlarge | r3.2xlarge | r3.4xlarge | r3.8xlarge | r3.large | r3.xlarge | r4.16xlarge | r4.2xlarge | r4.4xlarge | r4.8xlarge | r4.large | r4.xlarge | r5.12xlarge | r5.16xlarge | r5.24xlarge | r5.2xlarge | r5.4xlarge | r5.8xlarge | r5.large | r5.xlarge | r5a.12xlarge | r5a.16xlarge | r5a.24xlarge | r5a.2xlarge | r5a.4xlarge | r5a.8xlarge | r5a.large | r5a.xlarge | r5d.12xlarge | r5d.16xlarge | r5d.24xlarge | r5d.2xlarge | r5d.4xlarge | r5d.8xlarge | r5d.large | r5d.xlarge | t2.large | t2.medium | t2.micro | t2.small`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FleetType`  <a name="cfn-gamelift-fleet-fleettype"></a>
Indicates whether to use On\-Demand or Spot instances for this fleet\. By default, this property is set to `ON_DEMAND`\. Learn more about when to use [ On\-Demand versus Spot Instances](https://docs.aws.amazon.com/gamelift/latest/developerguide/gamelift-ec2-instances.html#gamelift-ec2-instances-spot)\. This property cannot be changed after the fleet is created\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ON_DEMAND | SPOT`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InstanceRoleARN`  <a name="cfn-gamelift-fleet-instancerolearn"></a>
A unique identifier for an IAM role that manages access to your AWS services\. With an instance role ARN set, any application that runs on an instance in this fleet can assume the role, including install scripts, server processes, and daemons \(background processes\)\. Create a role or look up a role's ARN by using the [IAM dashboard](https://console.aws.amazon.com/iam/) in the AWS Management Console\. Learn more about using on\-box credentials for your game servers at [ Access external resources from a game server](https://docs.aws.amazon.com/gamelift/latest/developerguide/gamelift-sdk-server-resources.html)\. This property cannot be changed after the fleet is created\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Locations`  <a name="cfn-gamelift-fleet-locations"></a>
A set of remote locations to deploy additional instances to and manage as part of the fleet\. This parameter can only be used when creating fleets in AWS Regions that support multiple locations\. You can add any GameLift\-supported AWS Region as a remote location, in the form of an AWS Region code such as `us-west-2`\. To create a fleet with instances in the home Region only, omit this parameter\.   
*Required*: No  
*Type*: List of [LocationConfiguration](aws-properties-gamelift-fleet-locationconfiguration.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxSize`  <a name="cfn-gamelift-fleet-maxsize"></a>
The maximum number of instances that are allowed in the specified fleet location\. If this parameter is not set, the default is 1\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricGroups`  <a name="cfn-gamelift-fleet-metricgroups"></a>
The name of an AWS CloudWatch metric group to add this fleet to\. A metric group is used to aggregate the metrics for multiple fleets\. You can specify an existing metric group name or set a new name to create a new metric group\. A fleet can be included in only one metric group at a time\.   
*Required*: No  
*Type*: List of String  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinSize`  <a name="cfn-gamelift-fleet-minsize"></a>
The minimum number of instances that are allowed in the specified fleet location\. If this parameter is not set, the default is 0\.  
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
The status of termination protection for active game sessions on the fleet\. By default, this property is set to `NoProtection`\.  
+  **NoProtection** \- Game sessions can be terminated during active gameplay as a result of a scale\-down event\. 
+  **FullProtection** \- Game sessions in `ACTIVE` status cannot be terminated during a scale\-down event\.
*Required*: No  
*Type*: String  
*Allowed values*: `FullProtection | NoProtection`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PeerVpcAwsAccountId`  <a name="cfn-gamelift-fleet-peervpcawsaccountid"></a>
Used when peering your GameLift fleet with a VPC, the unique identifier for the AWS account that owns the VPC\. You can find your account ID in the AWS Management Console under account settings\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PeerVpcId`  <a name="cfn-gamelift-fleet-peervpcid"></a>
A unique identifier for a VPC with resources to be accessed by your GameLift fleet\. The VPC must be in the same Region as your fleet\. To look up a VPC ID, use the [VPC Dashboard](https://console.aws.amazon.com/vpc/) in the AWS Management Console\. Learn more about VPC peering in [VPC Peering with GameLift Fleets](https://docs.aws.amazon.com/gamelift/latest/developerguide/vpc-peering.html)\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ResourceCreationLimitPolicy`  <a name="cfn-gamelift-fleet-resourcecreationlimitpolicy"></a>
A policy that limits the number of game sessions that an individual player can create on instances in this fleet within a specified span of time\.  
*Required*: No  
*Type*: [ResourceCreationLimitPolicy](aws-properties-gamelift-fleet-resourcecreationlimitpolicy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RuntimeConfiguration`  <a name="cfn-gamelift-fleet-runtimeconfiguration"></a>
Instructions for how to launch and maintain server processes on instances in the fleet\. The runtime configuration defines one or more server process configurations, each identifying a build executable or Realtime script file and the number of processes of that type to run concurrently\.   
The `RuntimeConfiguration` parameter is required unless the fleet is being configured using the older parameters `ServerLaunchPath` and `ServerLaunchParameters`, which are still supported for backward compatibility\.
*Required*: Conditional  
*Type*: [RuntimeConfiguration](aws-properties-gamelift-fleet-runtimeconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScriptId`  <a name="cfn-gamelift-fleet-scriptid"></a>
The unique identifier for a Realtime configuration script to be deployed on fleet instances\. You can use either the script ID or ARN\. Scripts must be uploaded to GameLift prior to creating the fleet\. This fleet property cannot be changed later\.  
You can't use the `!Ref` command to reference a script created with a CloudFormation template for the fleet property `ScriptId`\. Instead, use `Fn::GetAtt Script.Arn` or `Fn::GetAtt Script.Id` to retrieve either of these properties as input for `ScriptId`\. Alternatively, enter a `ScriptId` string manually\.
*Required*: Conditional  
*Type*: String  
*Pattern*: `^script-\S+|^arn:.*:script\/script-\S+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-gamelift-fleet-return-values"></a>

### Ref<a name="aws-resource-gamelift-fleet-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the fleet ID, such as `fleet-1111aaaa-22bb-33cc-44dd-5555eeee66ff`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-gamelift-fleet-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-gamelift-fleet-return-values-fn--getatt-fn--getatt"></a>

`FleetId`  <a name="FleetId-fn::getatt"></a>
A unique identifier for the fleet\. 

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
                "DesiredEC2Instances": 1,
                "EC2InboundPermissions": [
                    {
                        "FromPort": 1234,
                        "ToPort": 1324,
                        "IpRange": "0.0.0.0/24",
                        "Protocol": "TCP"
                    },
                    {
                        "FromPort": 1356,
                        "ToPort": 1578,
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
                },
                "Locations": [
                  "us-west-2",
                  "us-east-1",
                  "eu-west-1"
                ]
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
      DesiredEC2Instances: 1
      EC2InboundPermissions:
        - FromPort: 1234
          ToPort: 1324
          IpRange: 0.0.0.0/24
          Protocol: TCP
        - FromPort: 1356
          ToPort: 1578
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
        Locations:
          - Location: 'us-west-2'
          - Location: 'us-east-1'
          - Location: 'eu-west-1'
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
                        "FromPort": 1234,
                        "ToPort": 1324,
                        "IpRange": "0.0.0.0/24",
                        "Protocol": "TCP"
                    },
                    {
                        "FromPort": 1356,
                        "ToPort": 1578,
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
                },
                "Locations": [
                  "us-west-2",
                  "us-east-1",
                  "eu-west-1"
                ]
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
        - FromPort: 1234
          ToPort: 1324
          IpRange: 0.0.0.0/24
          Protocol: TCP
        - FromPort: 1356
          ToPort: 1578
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
      Locations:
          - Location: 'us-west-2'
          - Location: 'us-east-1'
          - Location: 'eu-west-1'
```

## See also<a name="aws-resource-gamelift-fleet--seealso"></a>
+ [ Create GameLift resources using Amazon CloudFront](https://docs.aws.amazon.com/gamelift/latest/developerguide/resources-cloudformation.html) in the *Amazon GameLift Developer Guide*
+  [Setting up GameLift fleets](https://docs.aws.amazon.com/gamelift/latest/developerguide/fleets-intro.html) in the *Amazon GameLift Developer Guide* 
+ [CreateFleet](https://docs.aws.amazon.com/gamelift/latest/apireference/API_CreateFleet.html) in the *Amazon GameLift API Reference* 

