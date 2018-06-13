# Amazon EMR Cluster PlacementType<a name="aws-properties-emr-cluster-jobflowinstancesconfig-placementtype"></a>

The `PlacementType` property type specifies the Availability Zone \(AZ\) in which the job flow runs\. `PlacementType` is the property type for the `Placement` subproperty of the [Amazon EMR Cluster JobFlowInstancesConfig](aws-properties-emr-cluster-jobflowinstancesconfig.md) property type\.

## Syntax<a name="w3ab2c21c14e1107b5"></a>

### JSON<a name="aws-properties-emr-cluster-jobflowinstancesconfig-placementtype-syntax.json"></a>

```
{
  "[AvailabilityZone](#cfn-emr-cluster-jobflowinstancesconfig-placementtype-availabilityzone)" : String
}
```

### YAML<a name="aws-properties-emr-cluster-jobflowinstancesconfig-placementtype-syntax.yaml"></a>

```
[AvailabilityZone](#cfn-emr-cluster-jobflowinstancesconfig-placementtype-availabilityzone): String
```

## Properties<a name="w3ab2c21c14e1107b7"></a>

`AvailabilityZone`  <a name="cfn-emr-cluster-jobflowinstancesconfig-placementtype-availabilityzone"></a>
The Amazon Elastic Compute Cloud \(Amazon EC2\) AZ for the job flow\. For more information, see [http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-regions-availability-zones.html](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-regions-availability-zones.html) in the *Amazon EC2 User Guide for Linux Instances*\.  
*Required*: Yes  
*Type*: String