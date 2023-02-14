# AWS::EC2::SpotFleet<a name="aws-resource-ec2-spotfleet"></a>

Specifies a Spot Fleet request\.

The Spot Fleet request specifies the total target capacity and the On\-Demand target capacity\. Amazon EC2 calculates the difference between the total capacity and On\-Demand capacity, and launches the difference as Spot capacity\.

You can submit a single request that includes multiple launch specifications that vary by instance type, AMI, Availability Zone, or subnet\.

By default, the Spot Fleet requests Spot Instances in the Spot Instance pool where the price per unit is the lowest\. Each launch specification can include its own instance weighting that reflects the value of the instance type to your application workload\.

Alternatively, you can specify that the Spot Fleet distribute the target capacity across the Spot pools included in its launch specifications\. By ensuring that the Spot Instances in your Spot Fleet are in different Spot pools, you can improve the availability of your fleet\.

You can specify tags for the Spot Fleet request and instances launched by the fleet\. You cannot tag other resource types in a Spot Fleet request because only the `spot-fleet-request` and `instance` resource types are supported\.

For more information, see [Spot Fleet](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/spot-fleet.html) in the *Amazon EC2 User Guide for Linux Instances*\.

**Important**  
We strongly discourage using the RequestSpotFleet API because it is a legacy API with no planned investment\. For options for requesting Spot Instances, see [Which is the best Spot request method to use?](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/spot-best-practices.html#which-spot-request-method-to-use) in the *Amazon EC2 User Guide for Linux Instances*\.

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
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ec2-spotfleet-return-values"></a>

### Ref<a name="aws-resource-ec2-spotfleet-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the Spot Fleet\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ec2-spotfleet-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ec2-spotfleet-return-values-fn--getatt-fn--getatt"></a>

`Id`  <a name="Id-fn::getatt"></a>
The ID of the Spot Fleet\.

## Examples<a name="aws-resource-ec2-spotfleet--examples"></a>



### Create a Spot Fleet<a name="aws-resource-ec2-spotfleet--examples--Create_a_Spot_Fleet"></a>

The following example specifies a Spot Fleet with two launch specifications\. The weighted capacities are the same, so Amazon EC2 launches the same number of instances for each specification\. For more information, see [How Spot Fleet Works](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/spot-fleet.html) in the *Amazon EC2 User Guide for Linux Instances*\.

#### JSON<a name="aws-resource-ec2-spotfleet--examples--Create_a_Spot_Fleet--json"></a>

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

#### YAML<a name="aws-resource-ec2-spotfleet--examples--Create_a_Spot_Fleet--yaml"></a>

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

