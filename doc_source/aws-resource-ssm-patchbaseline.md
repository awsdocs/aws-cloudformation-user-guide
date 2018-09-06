# AWS::SSM::PatchBaseline<a name="aws-resource-ssm-patchbaseline"></a>

The `AWS::SSM::PatchBaseline` resource defines the basic information for an AWS Systems Manager patch baseline\. A patch baseline defines which patches are approved for installation on your instances\. For more information, see [ CreatePatchBaseline](http://docs.aws.amazon.com/systems-manager/latest/APIReference/API_CreatePatchBaseline.html) in the *AWS Systems Manager API Reference*\.

## Syntax<a name="aws-resource-ssm-patchbaseline-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ssm-patchbaseline-syntax.json"></a>

```
{
  "Type" : "AWS::SSM::PatchBaseline",
  "Properties" : {
    "[OperatingSystem](#cfn-ssm-patchbaseline-operatingsystem)" : String,
    "[ApprovedPatches](#cfn-ssm-patchbaseline-approvedpatches)" : [ String, ... ],
    "[PatchGroups](#cfn-ssm-patchbaseline-patchgroups)" : [ String, ... ],
    "[Description](#cfn-ssm-patchbaseline-description)" : String,
    "[ApprovedPatchesComplianceLevel](#cfn-ssm-patchbaseline-approvedpatchescompliancelevel)" : String,
    "[ApprovalRules](#cfn-ssm-patchbaseline-approvalrules)" : [*RuleGroup*](aws-properties-ssm-patchbaseline-rulegroup.md),
    "[GlobalFilters](#cfn-ssm-patchbaseline-globalfilters)" : [*PatchFilterGroup*](aws-properties-ssm-patchbaseline-patchfiltergroup.md),
    "[Name](#cfn-ssm-patchbaseline-name)" : String,
    "[RejectedPatches](#cfn-ssm-patchbaseline-rejectedpatches)" : [ String, ... ]
  }
}
```

### YAML<a name="aws-resource-ssm-patchbaseline-syntax.yaml"></a>

```
Type: "AWS::SSM::PatchBaseline"
Properties:
  [OperatingSystem](#cfn-ssm-patchbaseline-operatingsystem): String
  [ApprovedPatches](#cfn-ssm-patchbaseline-approvedpatches): 
    - String
  [PatchGroups](#cfn-ssm-patchbaseline-patchgroups): 
    - String
  [Description](#cfn-ssm-patchbaseline-description): String
  [ApprovedPatchesComplianceLevel](#cfn-ssm-patchbaseline-approvedpatchescompliancelevel): String
  [ApprovalRules](#cfn-ssm-patchbaseline-approvalrules):
    [*RuleGroup*](aws-properties-ssm-patchbaseline-rulegroup.md)
  [GlobalFilters](#cfn-ssm-patchbaseline-globalfilters):
    [*PatchFilterGroup*](aws-properties-ssm-patchbaseline-patchfiltergroup.md)
  [Name](#cfn-ssm-patchbaseline-name): String
  [RejectedPatches](#cfn-ssm-patchbaseline-rejectedpatches): 
    - String
```

## Properties<a name="aws-resource-ssm-patchbaseline-properties"></a>

`OperatingSystem`  <a name="cfn-ssm-patchbaseline-operatingsystem"></a>
Defines the operating system that the patch baseline applies to\. Supported operating systems include `WINDOWS`, `AMAZON_LINUX`, `UBUNTU`, `REDHAT_ENTERPRISE_LINUX`, `SUSE`, and `CENTOS`\. The default value is `WINDOWS`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`ApprovedPatches`  <a name="cfn-ssm-patchbaseline-approvedpatches"></a>
A list of explicitly approved patches for the baseline\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`PatchGroups`  <a name="cfn-ssm-patchbaseline-patchgroups"></a>
The names of the patch groups to register with the patch baseline\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Description`  <a name="cfn-ssm-patchbaseline-description"></a>
A description of the patch baseline\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ApprovedPatchesComplianceLevel`  <a name="cfn-ssm-patchbaseline-approvedpatchescompliancelevel"></a>
The compliance level for approved patches\. This means that if an approved patch is reported as missing, this is the severity of the compliance violation\. Valid compliance severity levels include the following: `CRITICAL`, `HIGH`, `MEDIUM`, `LOW`, `INFORMATIONAL`, and `UNSPECIFIED`\. The default value is `UNSPECIFIED`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ApprovalRules`  <a name="cfn-ssm-patchbaseline-approvalrules"></a>
A set of rules that are used to include patches in the baseline\.  
 *Required*: No  
 *Type*: [Systems Manager PatchBaseline RuleGroup](aws-properties-ssm-patchbaseline-rulegroup.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`GlobalFilters`  <a name="cfn-ssm-patchbaseline-globalfilters"></a>
A set of global filters that are used to exclude patches from the baseline\.  
 *Required*: No  
 *Type*: [Systems Manager PatchBaseline PatchFilterGroup](aws-properties-ssm-patchbaseline-patchfiltergroup.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Name`  <a name="cfn-ssm-patchbaseline-name"></a>
The name of the patch baseline\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`RejectedPatches`  <a name="cfn-ssm-patchbaseline-rejectedpatches"></a>
A list of explicitly rejected patches for the baseline\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-ssm-patchbaseline-returnvalues"></a>

### Ref<a name="w3ab2c21c10e1168b9b3"></a>

When you pass the logical ID of an `AWS::SSM::PatchBaseline` resource to the intrinsic `Ref` function, the function returns the physical ID of the resource, such as `pb-abcde1234567890yz`\. 

**Note**  
The ID of the default patch baseline provided by AWS is an ARN—for example `arn:aws:ssm:us-west-2:123456789012:patchbaseline/abcde1234567890yz`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

## See Also<a name="aws-resource-ssm-patchbaseline-seealso"></a>
+ [ CreatePatchBaseline](http://docs.aws.amazon.com/systems-manager/latest/APIReference/API_CreatePatchBaseline.html) in the *AWS Systems Manager API Reference*