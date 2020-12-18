# AWS::EC2::SpotFleet<a name="aws-resource-ec2-spotfleet"></a>

Specifies a Spot Fleet request\. A Spot Fleet request contains the configuration information to launch a fleet, or group, of instances\.

The Spot Fleet request specifies the total target capacity and the On\-Demand target capacity for the fleet\. Amazon EC2 calculates the difference between the total capacity and On\-Demand capacity, and launches the difference as Spot capacity\.

The Spot Fleet request can include multiple launch specifications that vary by instance type, AMI, Availability Zone, or subnet\.

By default, the Spot Fleet requests Spot Instances in the Spot pool where the price per unit is the lowest\. Each launch specification can include its own instance weighting that reflects the value of the instance type to your application workload\.

Alternatively, you can specify that the Spot Fleet distribute the target capacity across the Spot pools included in its launch specifications\. By ensuring that the Spot Instances in your Spot Fleet are in different Spot pools, you can improve the availability of your fleet\.

You can specify tags for the Spot Instances\. You cannot tag other resource types in a Spot Fleet request because only the `instance` resource type is supported\.

For more information, see [Spot Fleet Requests](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/spot-fleet-requests.html) in the *Amazon EC2 User Guide for Linux Instances*\.

## Syntax<a name="aws-resource-ec2-spotfleet-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-spotfleet-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::SpotFleet",
  "Properties" : {
      "[SpotFleetRequestConfigData](#cfn-ec2-spotfleet-spotfleetrequestconfigdata)" : SpotFleetRequestConfigData
    }
}
```

### YAML<a name="aws-resource-ec2-spotfleet-syntax.yaml"></a>

```
Type: AWS::EC2::SpotFleet
Properties: 
  [SpotFleetRequestConfigData](#cfn-ec2-spotfleet-spotfleetrequestconfigdata): 
    SpotFleetRequestConfigData
```

## Properties<a name="aws-resource-ec2-spotfleet-properties"></a>

`SpotFleetRequestConfigData`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata"></a>
Describes the configuration of a Spot Fleet request\.  
*Required*: Yes  
*Type*: [SpotFleetRequestConfigData](aws-properties-ec2-spotfleet-spotfleetrequestconfigdata.md)  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

## Return values<a name="aws-resource-ec2-spotfleet-return-values"></a>

### Ref<a name="aws-resource-ec2-spotfleet-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the Spot Fleet\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-ec2-spotfleet--examples"></a>



### Spot Fleet<a name="aws-resource-ec2-spotfleet--examples--Spot_Fleet"></a>

The following example specifies a Spot Fleet with two launch specifications\. The weighted capacities are the same, so Amazon EC2 launches the same number of instances for each specification\. For more information, see [How Spot Fleet Works](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/spot-fleet.html) in the *Amazon EC2 User Guide for Linux Instances*\.

#### JSON<a name="aws-resource-ec2-spotfleet--examples--Spot_Fleet--json"></a>

```
"SpotFleet": {
  "Type": "AWS::EC2::SpotFleet",
  "Properties": {
    "SpotFleetRequestConfigData": {
     "IamFleetRole": { "Fn::GetAtt": [ "IAMFleetRole", "Arn"] },
     "SpotPrice": "1000",
     "TargetCapacity": { "Ref": "TargetCapacity" },
     "LaunchSpecifications": [
     {
         "EbsOptimized": "false",
         "InstanceType": { "Ref": "InstanceType" },
         "ImageId": { "Fn::FindInMap": [ "AWSRegionArch2AMI", { "Ref": "AWS::Region" },
                      { "Fn::FindInMap": [ "AWSInstanceType2Arch", { "Ref": "InstanceType" }, "Arch" ] }
                     ]},
          "SubnetId": { "Ref": "Subnet1" },
          "WeightedCapacity": "8"
     },
     {
         "EbsOptimized": "true",
         "InstanceType": { "Ref": "InstanceType" },
         "ImageId": { "Fn::FindInMap": [ "AWSRegionArch2AMI", { "Ref": "AWS::Region" },
                      { "Fn::FindInMap": [ "AWSInstanceType2Arch", { "Ref": "InstanceType" }, "Arch" ] }
                     ]},
          "Monitoring": { "Enabled": "true" },
          "SecurityGroups": [ { "GroupId": { "Fn::GetAtt": [ "SG0", "GroupId" ] } } ],
          "SubnetId": { "Ref": "Subnet0" },
          "IamInstanceProfile": { "Arn": { "Fn::GetAtt": [ "RootInstanceProfile", "Arn" ] } },
          "WeightedCapacity": "8"
         }
         ]
     }
   }
}
```

#### YAML<a name="aws-resource-ec2-spotfleet--examples--Spot_Fleet--yaml"></a>

```
SpotFleet:
  Type: AWS::EC2::SpotFleet
  Properties:
    SpotFleetRequestConfigData:
      IamFleetRole: !GetAtt [IAMFleetRole, Arn]
      SpotPrice: '1000'
      TargetCapacity:
        Ref: TargetCapacity
      LaunchSpecifications:
      - EbsOptimized: 'false'
        InstanceType:
          Ref: InstanceType
      ImageId:
        Fn::FindInMap:
        - AWSRegionArch2AMI
        - Ref: AWS::Region
        - Fn::FindInMap:
          - AWSInstanceType2Arch
          - Ref: InstanceType
          - Arch
      SubnetId:
        Ref: Subnet1
      WeightedCapacity: '8'
    - EbsOptimized: 'true'
      InstanceType:
        Ref: InstanceType
      ImageId:
        Fn::FindInMap:
        - AWSRegionArch2AMI
        - Ref: AWS::Region
        - Fn::FindInMap:
        - AWSInstanceType2Arch
        - Ref: InstanceType
        - Arch
      Monitoring:
        Enabled: 'true'
        SecurityGroups:
         - GroupId:
             Fn::GetAtt:
             - SG0
             - GroupId
       SubnetId:
          Ref: Subnet0
       IamInstanceProfile:
         Arn:
         Fn::GetAtt:
         - RootInstanceProfile
         - Arn
       WeightedCapacity: '8'
```

## See also<a name="aws-resource-ec2-spotfleet--seealso"></a>
+  [AWS::ApplicationAutoScaling::ScalableTarget](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-applicationautoscaling-scalabletarget.html)
+  [AWS::ApplicationAutoScaling::ScalingPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-applicationautoscaling-scalingpolicy.html)

