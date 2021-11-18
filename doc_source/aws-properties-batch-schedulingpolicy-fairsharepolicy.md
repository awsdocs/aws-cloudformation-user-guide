# AWS::Batch::SchedulingPolicy FairsharePolicy<a name="aws-properties-batch-schedulingpolicy-fairsharepolicy"></a>

The fair share policy for a scheduling policy\.

## Syntax<a name="aws-properties-batch-schedulingpolicy-fairsharepolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-batch-schedulingpolicy-fairsharepolicy-syntax.json"></a>

```
{
  "[ComputeReservation](#cfn-batch-schedulingpolicy-fairsharepolicy-computereservation)" : Double,
  "[ShareDecaySeconds](#cfn-batch-schedulingpolicy-fairsharepolicy-sharedecayseconds)" : Double,
  "[ShareDistribution](#cfn-batch-schedulingpolicy-fairsharepolicy-sharedistribution)" : [ ShareAttributes, ... ]
}
```

### YAML<a name="aws-properties-batch-schedulingpolicy-fairsharepolicy-syntax.yaml"></a>

```
  [ComputeReservation](#cfn-batch-schedulingpolicy-fairsharepolicy-computereservation): Double
  [ShareDecaySeconds](#cfn-batch-schedulingpolicy-fairsharepolicy-sharedecayseconds): Double
  [ShareDistribution](#cfn-batch-schedulingpolicy-fairsharepolicy-sharedistribution): 
    - ShareAttributes
```

## Properties<a name="aws-properties-batch-schedulingpolicy-fairsharepolicy-properties"></a>

`ComputeReservation`  <a name="cfn-batch-schedulingpolicy-fairsharepolicy-computereservation"></a>
A value used to reserve some of the available maximum vCPU for fair share identifiers that have not yet been used\.  
The reserved ratio is `(computeReservation/100)^ActiveFairShares ` where ` ActiveFairShares ` is the number of active fair share identifiers\.  
For example, a `computeReservation` value of 50 indicates that AWS Batch should reserve 50% of the maximum available vCPU if there is only one fair share identifier, 25% if there are two fair share identifiers, and 12\.5% if there are three fair share identifiers\. A `computeReservation` value of 25 indicates that AWS Batch should reserve 25% of the maximum available vCPU if there is only one fair share identifier, 6\.25% if there are two fair share identifiers, and 1\.56% if there are three fair share identifiers\.  
The minimum value is 0 and the maximum value is 99\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ShareDecaySeconds`  <a name="cfn-batch-schedulingpolicy-fairsharepolicy-sharedecayseconds"></a>
The time period to use to calculate a fair share percentage for each fair share identifier in use, in seconds\. A value of zero \(0\) indicates that only current usage should be measured\. The decay allows for more recently run jobs to have more weight than jobs that ran earlier\. The maximum supported value is 604800 \(1 week\)\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ShareDistribution`  <a name="cfn-batch-schedulingpolicy-fairsharepolicy-sharedistribution"></a>
An array of `SharedIdentifier` objects that contain the weights for the fair share identifiers for the fair share policy\. Fair share identifiers that aren't included have a default weight of `1.0`\.  
*Required*: No  
*Type*: List of [ShareAttributes](aws-properties-batch-schedulingpolicy-shareattributes.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-batch-schedulingpolicy-fairsharepolicy--seealso"></a>
+  [FairsharePolicy](https://docs.aws.amazon.com/batch/latest/APIReference/API_FairsharePolicy.html) in the *AWS Batch API Reference*\.