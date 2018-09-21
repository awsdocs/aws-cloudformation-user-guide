# Limitations of StackSets<a name="stacksets-limitations"></a>

The following limits apply to AWS CloudFormation StackSets\.
+ StackSets is supported in all commercial regions of AWS\. StackSets is not supported in the following regions\.
  + China \(Beijing\) Region
  + AWS GovCloud \(US\)
+ You can create a maximum of 20 stack sets in your administrator account, and a maximum of 500 stack instances per stack set\.
+ StackSets does not currently support templates that use transforms\. For more information about transforms, see [Transform](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/transform-section-structure.html) in this guide\.