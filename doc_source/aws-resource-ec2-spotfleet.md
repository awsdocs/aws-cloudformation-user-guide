# AWS::EC2::SpotFleet<a name="aws-resource-ec2-spotfleet"></a>

The `AWS::EC2::SpotFleet` resource creates a request for a collection of Spot instances\. The Spot fleet attempts to launch the number of Spot instances to meet the target capacity that you specified\. For more information, see [Spot Instances](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-spot-instances.html) in the *Amazon EC2 User Guide for Linux Instances*\.

**Topics**
+ [Syntax](#aws-resource-ec2-spotfleet-syntax)
+ [Properties](#w3ab2c21c10d479b9)
+ [Return Values](#w3ab2c21c10d479c11)
+ [Example](#w3ab2c21c10d479c13)
+ [Related Resources](#w3ab2c21c10d479c15)

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
Type: "AWS::EC2::SpotFleet"
Properties: 
  [SpotFleetRequestConfigData](#cfn-ec2-spotfleet-spotfleetrequestconfigdata):
    SpotFleetRequestConfigData
```

## Properties<a name="w3ab2c21c10d479b9"></a>

`SpotFleetRequestConfigData`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata"></a>
The configuration for a Spot fleet request\.  
*Required*: Yes  
*Type*: [Amazon EC2 SpotFleet SpotFleetRequestConfigData](aws-properties-ec2-spotfleet-spotfleetrequestconfigdata.md)  
*Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)

## Return Values<a name="w3ab2c21c10d479c11"></a>

### Ref<a name="w3ab2c21c10d479c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="w3ab2c21c10d479c13"></a>

The following example creates a Spot fleet with two launch specifications\. The weighted capacities are the same, so Amazon EC2 launches the same number of instances for each specification\. For more information, see [How Spot Fleet Works](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/spot-fleet.html) in the *Amazon EC2 User Guide for Linux Instances*\.

### JSON<a name="aws-resource-ec2-spotfleet-example-1.json"></a>

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

### YAML<a name="aws-resource-ec2-spotfleet-example-1.yaml"></a>

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

## Related Resources<a name="w3ab2c21c10d479c15"></a>

To use Application Auto Scaling to scale an Amazon ECS service in response to CloudWatch alarms, use the [AWS::ApplicationAutoScaling::ScalableTarget](aws-resource-applicationautoscaling-scalabletarget.md) and [AWS::ApplicationAutoScaling::ScalingPolicy](aws-resource-applicationautoscaling-scalingpolicy.md) resources\.