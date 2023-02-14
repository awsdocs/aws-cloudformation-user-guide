# AWS::Batch::SchedulingPolicy ShareAttributes<a name="aws-properties-batch-schedulingpolicy-shareattributes"></a>

Specifies the weights for the fair share identifiers for the fair share policy\. Fair share identifiers that aren't included have a default weight of `1.0`\.

## Syntax<a name="aws-properties-batch-schedulingpolicy-shareattributes-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-batch-schedulingpolicy-shareattributes-syntax.json"></a>

```
{
  "[ShareIdentifier](#cfn-batch-schedulingpolicy-shareattributes-shareidentifier)" : String,
  "[WeightFactor](#cfn-batch-schedulingpolicy-shareattributes-weightfactor)" : Double
}
```

### YAML<a name="aws-properties-batch-schedulingpolicy-shareattributes-syntax.yaml"></a>

```
  [ShareIdentifier](#cfn-batch-schedulingpolicy-shareattributes-shareidentifier): String
  [WeightFactor](#cfn-batch-schedulingpolicy-shareattributes-weightfactor): Double
```

## Properties<a name="aws-properties-batch-schedulingpolicy-shareattributes-properties"></a>

`ShareIdentifier`  <a name="cfn-batch-schedulingpolicy-shareattributes-shareidentifier"></a>
A fair share identifier or fair share identifier prefix\. If the string ends with an asterisk \(\*\), this entry specifies the weight factor to use for fair share identifiers that start with that prefix\. The list of fair share identifiers in a fair share policy can't overlap\. For example, you can't have one that specifies a `shareIdentifier` of `UserA*` and another that specifies a `shareIdentifier` of `UserA-1`\.  
There can be no more than 500 fair share identifiers active in a job queue\.  
The string is limited to 255 alphanumeric characters, and can be followed by an asterisk \(\*\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WeightFactor`  <a name="cfn-batch-schedulingpolicy-shareattributes-weightfactor"></a>
The weight factor for the fair share identifier\. The default value is 1\.0\. A lower value has a higher priority for compute resources\. For example, jobs that use a share identifier with a weight factor of 0\.125 \(1/8\) get 8 times the compute resources of jobs that use a share identifier with a weight factor of 1\.  
The smallest supported value is 0\.0001, and the largest supported value is 999\.9999\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-batch-schedulingpolicy-shareattributes--seealso"></a>
+  [ShareAttributes](https://docs.aws.amazon.com/batch/latest/APIReference/API_ShareAttributes.html) in the *AWS Batch API Reference*\.