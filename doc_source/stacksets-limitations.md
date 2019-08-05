# Limitations of StackSets<a name="stacksets-limitations"></a>

The following limits apply to AWS CloudFormation StackSets\.
+ StackSets is supported in all commercial regions of AWS\. StackSets is not supported in the following regions\.
  + China \(Beijing\) Region
  + AWS GovCloud \(US\-West\)
+ You can create a maximum of 20 stack sets in your administrator account, and a maximum of 500 stack instances per stack set\.
+ You can have a maximum of 1500 stack instance operations running in a given region at the same time, per administrator account\.

  This limit applies *per region*, and is regardless of the number of stack sets involved\. It includes stack instances affected by StackSet creation and update operations, as well as creating, updating, or deleting stack instances directly\.
+ StackSets does not currently support templates that use macros, including transforms, which are macros hosted by AWS CloudFormation\. For more information about macros, see [Template Macros](template-macros.md)\.
