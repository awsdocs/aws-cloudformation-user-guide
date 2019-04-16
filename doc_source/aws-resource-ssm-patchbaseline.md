# AWS::SSM::PatchBaseline<a name="aws-resource-ssm-patchbaseline"></a>

The `AWS::SSM::PatchBaseline` resource defines the basic information for an AWS Systems Manager patch baseline\. A patch baseline defines which patches are approved for installation on your instances\. For more information, see [ CreatePatchBaseline](https://docs.aws.amazon.com/systems-manager/latest/APIReference/API_CreatePatchBaseline.html) in the *AWS Systems Manager API Reference*\.

## Syntax<a name="aws-resource-ssm-patchbaseline-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ssm-patchbaseline-syntax.json"></a>

```
{
  "Type" : "AWS::SSM::PatchBaseline",
  "Properties" : {
    "[Name](#cfn-ssm-patchbaseline-name)" : String,
    "[OperatingSystem](#cfn-ssm-patchbaseline-operatingsystem)" : String,
    "[Description](#cfn-ssm-patchbaseline-description)" : String,
    "[PatchGroups](#cfn-ssm-patchbaseline-patchgroups)" : [ String, ... ],
    "[ApprovalRules](#cfn-ssm-patchbaseline-approvalrules)" : [*RuleGroup*](aws-properties-ssm-patchbaseline-rulegroup.md),
    "[ApprovedPatches](#cfn-ssm-patchbaseline-approvedpatches)" : [ String, ... ],
    "[ApprovedPatchesComplianceLevel](#cfn-ssm-patchbaseline-approvedpatchescompliancelevel)" : String,
    "[ApprovedPatchesEnableNonSecurity](#cfn-ssm-patchbaseline-approvedpatchesenablenonsecurity)" : Boolean,
    "[RejectedPatches](#cfn-ssm-patchbaseline-rejectedpatches)" : [ String, ... ],
    "[RejectedPatchesAction](#cfn-ssm-patchbaseline-rejectedpatchesaction)" : String,
    "[GlobalFilters](#cfn-ssm-patchbaseline-globalfilters)" : [*PatchFilterGroup*](aws-properties-ssm-patchbaseline-patchfiltergroup.md),
    "[Sources](#cfn-ssm-patchbaseline-patchsource)" : [*PatchSource*](aws-properties-ssm-patchbaseline-patchsource.md)    
  }
}
```

### YAML<a name="aws-resource-ssm-patchbaseline-syntax.yaml"></a>

```
Type: "AWS::SSM::PatchBaseline"
Properties:
  [Name](#cfn-ssm-patchbaseline-name): String
  [OperatingSystem](#cfn-ssm-patchbaseline-operatingsystem): String
  [Description](#cfn-ssm-patchbaseline-description): String
  [PatchGroups](#cfn-ssm-patchbaseline-patchgroups):
    - String
  [ApprovalRules](#cfn-ssm-patchbaseline-approvalrules):
    [*RuleGroup*](aws-properties-ssm-patchbaseline-rulegroup.md)        
  [ApprovedPatches](#cfn-ssm-patchbaseline-approvedpatches):
    - String
  [ApprovedPatchesComplianceLevel](#cfn-ssm-patchbaseline-approvedpatchescompliancelevel): String
  [ApprovedPatchesEnableNonSecurity](#cfn-ssm-patchbaseline-approvedpatchesenablenonsecurity): Boolean
  [RejectedPatches](#cfn-ssm-patchbaseline-rejectedpatches):
    - String
  [RejectedPatchesAction](#cfn-ssm-patchbaseline-rejectedpatchesaction): String
  [GlobalFilters](#cfn-ssm-patchbaseline-globalfilters):
    [*PatchFilterGroup*](aws-properties-ssm-patchbaseline-patchfiltergroup.md)
  [Sources](#cfn-ssm-patchbaseline-patchsource): [*PatchSource*](aws-properties-ssm-patchbaseline-patchsource.md)
```

## Properties<a name="aws-resource-ssm-patchbaseline-properties"></a>

`Name`  <a name="cfn-ssm-patchbaseline-name"></a>
The name of the patch baseline\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`OperatingSystem`  <a name="cfn-ssm-patchbaseline-operatingsystem"></a>
Defines the operating system that the patch baseline applies to\. Supported operating systems include `WINDOWS`, `AMAZON_LINUX`, `AMAZON_LINUX_2`, `UBUNTU`, `REDHAT_ENTERPRISE_LINUX`, `SUSE`, and `CENTOS`\. The default value is `WINDOWS`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Description`  <a name="cfn-ssm-patchbaseline-description"></a>
A description of the patch baseline\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`PatchGroups`  <a name="cfn-ssm-patchbaseline-patchgroups"></a>
The names of the patch groups to register with the patch baseline\.  
*Required*: No  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ApprovalRules`  <a name="cfn-ssm-patchbaseline-approvalrules"></a>
A set of rules that are used to include patches in the baseline\.  
*Required*: No  
 *Type*: [RuleGroup](aws-properties-ssm-patchbaseline-rulegroup.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ApprovedPatches`  <a name="cfn-ssm-patchbaseline-approvedpatches"></a>
A list of explicitly approved patches for the baseline\.  
*Required*: No  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ApprovedPatchesComplianceLevel`  <a name="cfn-ssm-patchbaseline-approvedpatchescompliancelevel"></a>
The compliance level for approved patches\. This means that if an approved patch is reported as missing, this is the severity of the compliance violation\. Valid compliance severity levels include the following: `CRITICAL`, `HIGH`, `MEDIUM`, `LOW`, `INFORMATIONAL`, and `UNSPECIFIED`\. The default value is `UNSPECIFIED`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

ApprovedPatchesEnableNonSecurity  <a name="cfn-ssm-patchbaseline-approvedpatchesenablenonsecurity"></a>
Indicates whether the list of approved patches includes non\-security updates that should be applied to the instances\. The default value is 'false'\. Applies to Linux instances only\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`RejectedPatches`  <a name="cfn-ssm-patchbaseline-rejectedpatches"></a>
A list of explicitly rejected patches for the baseline\.  
*Required*: No  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

RejectedPatchesAction  <a name="cfn-ssm-patchbaseline-rejectedpatchesaction"></a>
The action for Patch Manager to take on patches included in the RejectedPackages list\.  
+ **ALLOW\_AS\_DEPENDENCY**: A package in the Rejected patches list is installed only if it is a dependency of another package\. It is considered compliant with the patch baseline, and its status is reported as *InstalledOther*\. This is the default action if no option is specified\.
+ **BLOCK**: Packages in the RejectedPatches list, and packages that include them as dependencies, are not installed under any circumstances\. If a package was installed before it was added to the Rejected patches list, it is considered non\-compliant with the patch baseline, and its status is reported as *InstalledRejected*\.
*Required*: No  
*Type*: String
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`GlobalFilters`  <a name="cfn-ssm-patchbaseline-globalfilters"></a>
A set of global filters that are used to exclude patches from the baseline\.  
*Required*: No  
 *Type*: [PatchFilterGroup](aws-properties-ssm-patchbaseline-patchfiltergroup.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

Sources  <a name="cfn-ssm-patchbaseline-patchsource"></a>
Information about the patches to use to update the instances, including target operating systems and source repositories\. Applies to Linux instances only\.   
*Required*: No  
 *Type*: Array of [PatchSource](aws-properties-ssm-patchbaseline-patchsource.md) objects  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Values<a name="aws-resource-ssm-patchbaseline-returnvalues"></a>

### Ref<a name="w13ab1c21c10d231c31b9b3"></a>

When you pass the logical ID of an `AWS::SSM::PatchBaseline` resource to the intrinsic `Ref` function, the function returns the physical ID of the resource, such as `pb-abcde1234567890yz`\.

**Note**  
The ID of the default patch baseline provided by AWS is an ARN—for example `arn:aws:ssm:us-west-2:123456789012:patchbaseline/abcde1234567890yz`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## See Also<a name="aws-resource-ssm-patchbaseline-seealso"></a>
+ [ CreatePatchBaseline](https://docs.aws.amazon.com/systems-manager/latest/APIReference/API_CreatePatchBaseline.html) in the *AWS Systems Manager API Reference*
