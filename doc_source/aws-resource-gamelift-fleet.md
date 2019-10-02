# AWS::GameLift::Fleet<a name="aws-resource-gamelift-fleet"></a>

The `AWS::GameLift::Fleet` resource creates an Amazon GameLift \(GameLift\) fleet to host game servers\. A fleet is a set of EC2 instances, each of which is a host in the fleet\. For more information, see the [CreateFleet](https://docs.aws.amazon.com/gamelift/latest/apireference/API_CreateFleet.html) action in the *Amazon GameLift API Reference*\.

## Syntax<a name="aws-resource-gamelift-fleet-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-gamelift-fleet-syntax.json"></a>

```
{
  "Type" : "AWS::GameLift::Fleet",
  "Properties" : {
      "[BuildId](#cfn-gamelift-fleet-buildid)" : String,
      "[Description](#cfn-gamelift-fleet-description)" : String,
      "[DesiredEC2Instances](#cfn-gamelift-fleet-desiredec2instances)" : Integer,
      "[EC2InboundPermissions](#cfn-gamelift-fleet-ec2inboundpermissions)" : [ [IpPermission](aws-properties-gamelift-fleet-ec2inboundpermission.md), ... ],
      "[EC2InstanceType](#cfn-gamelift-fleet-ec2instancetype)" : String,
      "[LogPaths](#cfn-gamelift-fleet-logpaths)" : [ String, ... ],
      "[MaxSize](#cfn-gamelift-fleet-maxsize)" : Integer,
      "[MinSize](#cfn-gamelift-fleet-minsize)" : Integer,
      "[Name](#cfn-gamelift-fleet-name)" : String,
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
  [Description](#cfn-gamelift-fleet-description): String
  [DesiredEC2Instances](#cfn-gamelift-fleet-desiredec2instances): Integer
  [EC2InboundPermissions](#cfn-gamelift-fleet-ec2inboundpermissions): 
    - [IpPermission](aws-properties-gamelift-fleet-ec2inboundpermission.md)
  [EC2InstanceType](#cfn-gamelift-fleet-ec2instancetype): String
  [LogPaths](#cfn-gamelift-fleet-logpaths): 
    - String
  [MaxSize](#cfn-gamelift-fleet-maxsize): Integer
  [MinSize](#cfn-gamelift-fleet-minsize): Integer
  [Name](#cfn-gamelift-fleet-name): String
  [ServerLaunchParameters](#cfn-gamelift-fleet-serverlaunchparameters): String
  [ServerLaunchPath](#cfn-gamelift-fleet-serverlaunchpath): String
```

## Properties<a name="aws-resource-gamelift-fleet-properties"></a>

`BuildId`  <a name="cfn-gamelift-fleet-buildid"></a>
Unique identifier for a build to be deployed on the new fleet\. The custom game server build must have been successfully uploaded to Amazon GameLift and be in a `READY` status\. This fleet setting cannot be changed once the fleet is created\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `^build-\S+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-gamelift-fleet-description"></a>
Human\-readable description of a fleet\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DesiredEC2Instances`  <a name="cfn-gamelift-fleet-desiredec2instances"></a>
Number of EC2 instances you want this fleet to host\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EC2InboundPermissions`  <a name="cfn-gamelift-fleet-ec2inboundpermissions"></a>
Range of IP addresses and port settings that permit inbound traffic to access game sessions that running on the fleet\. For fleets using a custom game build, this parameter is required before game sessions running on the fleet can accept connections\. For Realtime Servers fleets, Amazon GameLift automatically sets TCP and UDP ranges for use by the Realtime servers\. You can specify multiple permission settings or add more by updating the fleet\.  
*Required*: No  
*Type*: List of [IpPermission](aws-properties-gamelift-fleet-ec2inboundpermission.md)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EC2InstanceType`  <a name="cfn-gamelift-fleet-ec2instancetype"></a>
Name of an EC2 instance type that is supported in Amazon GameLift\. A fleet instance type determines the computing resources of each instance in the fleet, including CPU, memory, storage, and networking capacity\. For more information about the instance types that are supported by GameLift, see the [EC2InstanceType](https://docs.aws.amazon.com/gamelift/latest/apireference/API_CreateFleet.html#gamelift-CreateFleet-request-EC2InstanceType) parameter in the *Amazon GameLift API Reference*\.  
*Required*: Yes  
*Type*: String  
*Allowed Values*: `c3.2xlarge | c3.4xlarge | c3.8xlarge | c3.large | c3.xlarge | c4.2xlarge | c4.4xlarge | c4.8xlarge | c4.large | c4.xlarge | m3.2xlarge | m3.large | m3.medium | m3.xlarge | m4.10xlarge | m4.2xlarge | m4.4xlarge | m4.large | m4.xlarge | r3.2xlarge | r3.4xlarge | r3.8xlarge | r3.large | r3.xlarge | r4.16xlarge | r4.2xlarge | r4.4xlarge | r4.8xlarge | r4.large | r4.xlarge | t2.large | t2.medium | t2.micro | t2.small`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LogPaths`  <a name="cfn-gamelift-fleet-logpaths"></a>
This parameter is no longer used\. Instead, to specify where Amazon GameLift should store log files once a server process shuts down, use the Amazon GameLift server API `ProcessReady()` and specify one or more directory paths in `logParameters`\. See more information in the [Server API Reference](https://docs.aws.amazon.com/gamelift/latest/developerguide/gamelift-sdk-server-api-ref.html#gamelift-sdk-server-api-ref-dataypes-process)\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MaxSize`  <a name="cfn-gamelift-fleet-maxsize"></a>
Maximum value allowed for the fleet's instance count\. Default if not set is 1\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinSize`  <a name="cfn-gamelift-fleet-minsize"></a>
Minimum value allowed for the fleet's instance count\. Default if not set is 0\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-gamelift-fleet-name"></a>
Descriptive label that is associated with a fleet\. Fleet names do not need to be unique\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServerLaunchParameters`  <a name="cfn-gamelift-fleet-serverlaunchparameters"></a>
The parameters that are required to launch your game server\. Specify these parameters as a string of command\-line parameters, such as `+sv_port 33435 +start_lobby`\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ServerLaunchPath`  <a name="cfn-gamelift-fleet-serverlaunchpath"></a>
The location of your game server that GameLift launches\. You must escape the slashes \(\\\) and use the following pattern: `C:\\game\\launchpath`\. For example, if your game server files are in the `MyGame` folder, the path should be `C:\\game\\MyGame\\server.exe`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return Values<a name="aws-resource-gamelift-fleet-return-values"></a>

### Ref<a name="aws-resource-gamelift-fleet-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the fleet ID, such as `myfleet-a01234b56-7890-1de2-f345-g67h8i901j2k`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-gamelift-fleet--examples"></a>

### Create GameLift fleet<a name="aws-resource-gamelift-fleet--examples--Create_GameLift_fleet"></a>

The following example creates a GameLift fleet named `MyGameFleet` with two inbound permissions\. The fleet uses a `Ref` intrinsic function to specify a build, which can be declared elsewhere in the same template\. For the log path and server launch path, the example uses the escape character \(`\`\) to escape the slashes \(`\`\)\.

#### JSON<a name="aws-resource-gamelift-fleet--examples--Create_GameLift_fleet--json"></a>

```
"FleetResource": {
  "Type": "AWS::GameLift::Fleet",
  "Properties": {
    "Name": "MyGameFleet",
    "Description": "A fleet for my game",
    "BuildId": { "Ref": "BuildResource" },
    "ServerLaunchPath": "c:\\game\\TestApplicationServer.exe",
    "LogPaths": [
      "c:\\game\\testlog.log",
      "c:\\game\\testlog2.log"
    ],
    "EC2InstanceType": "t2.small",
    "DesiredEC2Instances": "2",
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
    ]
  } 
}
```

#### YAML<a name="aws-resource-gamelift-fleet--examples--Create_GameLift_fleet--yaml"></a>

```
FleetResource: 
  Type: AWS::GameLift::Fleet
  Properties: 
    Name: "MyGameFleet"
    Description: "A fleet for my game"
    BuildId: 
      Ref: "BuildResource"
    ServerLaunchPath: "c:\\game\\TestApplicationServer.exe"
    LogPaths: 
      - "c:\\game\\testlog.log"
      - "c:\\game\\testlog2.log"
    EC2InstanceType: "t2.small"
    DesiredEC2Instances: "2"
    EC2InboundPermissions: 
      - 
        FromPort: "1234"
        ToPort: "1324"
        IpRange: "0.0.0.0/24"
        Protocol: "TCP"
      - 
        FromPort: "1356"
        ToPort: "1578"
        IpRange: "192.168.0.0/24"
        Protocol: "UDP"
```

## See Also<a name="aws-resource-gamelift-fleet--seealso"></a>
+  [CreateFleet](https://docs.aws.amazon.com/gamelift/latest/apireference/API_CreateFleet.html) in the *Amazon GameLift API Reference* 

## Supported Regions

This ResourceType is supported by ***all*** regions.