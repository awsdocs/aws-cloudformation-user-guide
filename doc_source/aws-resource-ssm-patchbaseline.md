# AWS::SSM::PatchBaseline<a name="aws-resource-ssm-patchbaseline"></a>

The `AWS::SSM::PatchBaseline` resource defines the basic information for an AWS Systems Manager patch baseline\. A patch baseline defines which patches are approved for installation on your instances\. 

For more information, see [CreatePatchBaseline](https://docs.aws.amazon.com/systems-manager/latest/APIReference/API_CreatePatchBaseline.html) in the *AWS Systems Manager API Reference*\.

## Syntax<a name="aws-resource-ssm-patchbaseline-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ssm-patchbaseline-syntax.json"></a>

```
{
  "Type" : "AWS::SSM::PatchBaseline",
  "Properties" : {
      "[ApprovalRules](#cfn-ssm-patchbaseline-approvalrules)" : [RuleGroup](aws-properties-ssm-patchbaseline-rulegroup.md),
      "[ApprovedPatches](#cfn-ssm-patchbaseline-approvedpatches)" : [ String, ... ],
      "[ApprovedPatchesComplianceLevel](#cfn-ssm-patchbaseline-approvedpatchescompliancelevel)" : String,
      "[ApprovedPatchesEnableNonSecurity](#cfn-ssm-patchbaseline-approvedpatchesenablenonsecurity)" : Boolean,
      "[Description](#cfn-ssm-patchbaseline-description)" : String,
      "[GlobalFilters](#cfn-ssm-patchbaseline-globalfilters)" : [PatchFilterGroup](aws-properties-ssm-patchbaseline-patchfiltergroup.md),
      "[Name](#cfn-ssm-patchbaseline-name)" : String,
      "[OperatingSystem](#cfn-ssm-patchbaseline-operatingsystem)" : String,
      "[PatchGroups](#cfn-ssm-patchbaseline-patchgroups)" : [ String, ... ],
      "[RejectedPatches](#cfn-ssm-patchbaseline-rejectedpatches)" : [ String, ... ],
      "[RejectedPatchesAction](#cfn-ssm-patchbaseline-rejectedpatchesaction)" : String,
      "[Sources](#cfn-ssm-patchbaseline-sources)" : [ [PatchSource](aws-properties-ssm-patchbaseline-patchsource.md), ... ],
      "[Tags](#cfn-ssm-patchbaseline-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-ssm-patchbaseline-syntax.yaml"></a>

```
Type: AWS::SSM::PatchBaseline
Properties: 
  [ApprovalRules](#cfn-ssm-patchbaseline-approvalrules): 
    [RuleGroup](aws-properties-ssm-patchbaseline-rulegroup.md)
  [ApprovedPatches](#cfn-ssm-patchbaseline-approvedpatches): 
    - String
  [ApprovedPatchesComplianceLevel](#cfn-ssm-patchbaseline-approvedpatchescompliancelevel): String
  [ApprovedPatchesEnableNonSecurity](#cfn-ssm-patchbaseline-approvedpatchesenablenonsecurity): Boolean
  [Description](#cfn-ssm-patchbaseline-description): String
  [GlobalFilters](#cfn-ssm-patchbaseline-globalfilters): 
    [PatchFilterGroup](aws-properties-ssm-patchbaseline-patchfiltergroup.md)
  [Name](#cfn-ssm-patchbaseline-name): String
  [OperatingSystem](#cfn-ssm-patchbaseline-operatingsystem): String
  [PatchGroups](#cfn-ssm-patchbaseline-patchgroups): 
    - String
  [RejectedPatches](#cfn-ssm-patchbaseline-rejectedpatches): 
    - String
  [RejectedPatchesAction](#cfn-ssm-patchbaseline-rejectedpatchesaction): String
  [Sources](#cfn-ssm-patchbaseline-sources): 
    - [PatchSource](aws-properties-ssm-patchbaseline-patchsource.md)
  [Tags](#cfn-ssm-patchbaseline-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-ssm-patchbaseline-properties"></a>

`ApprovalRules`  <a name="cfn-ssm-patchbaseline-approvalrules"></a>
A set of rules used to include patches in the baseline\.  
*Required*: No  
*Type*: [RuleGroup](aws-properties-ssm-patchbaseline-rulegroup.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ApprovedPatches`  <a name="cfn-ssm-patchbaseline-approvedpatches"></a>
A list of explicitly approved patches for the baseline\.  
For information about accepted formats for lists of approved patches and rejected patches, see [Package Name Formats for Approved and Rejected Patch Lists](https://docs.aws.amazon.com/systems-manager/latest/userguide/patch-manager-approved-rejected-package-name-formats.html) in the *AWS Systems Manager User Guide*\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ApprovedPatchesComplianceLevel`  <a name="cfn-ssm-patchbaseline-approvedpatchescompliancelevel"></a>
Defines the compliance level for approved patches\. This means that if an approved patch is reported as missing, this is the severity of the compliance violation\. The default value is UNSPECIFIED\.  
*Required*: No  
*Type*: String  
*Allowed Values*: `CRITICAL | HIGH | INFORMATIONAL | LOW | MEDIUM | UNSPECIFIED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ApprovedPatchesEnableNonSecurity`  <a name="cfn-ssm-patchbaseline-approvedpatchesenablenonsecurity"></a>
Indicates whether the list of approved patches includes non\-security updates that should be applied to the instances\. The default value is 'false'\. Applies to Linux instances only\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-ssm-patchbaseline-description"></a>
A description of the patch baseline\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GlobalFilters`  <a name="cfn-ssm-patchbaseline-globalfilters"></a>
A set of global filters used to include patches in the baseline\.  
*Required*: No  
*Type*: [PatchFilterGroup](aws-properties-ssm-patchbaseline-patchfiltergroup.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-ssm-patchbaseline-name"></a>
The name of the patch baseline\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `128`  
*Pattern*: `^[a-zA-Z0-9_\-.]{3,128}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OperatingSystem`  <a name="cfn-ssm-patchbaseline-operatingsystem"></a>
Defines the operating system the patch baseline applies to\. The Default value is WINDOWS\.   
*Required*: No  
*Type*: String  
*Allowed Values*: `AMAZON_LINUX | AMAZON_LINUX_2 | CENTOS | REDHAT_ENTERPRISE_LINUX | SUSE | UBUNTU | WINDOWS`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PatchGroups`  <a name="cfn-ssm-patchbaseline-patchgroups"></a>
The name of the patch group that should be registered with the patch baseline\.  
*Required*: No  
*Type*: List of String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `^([\p{L}\p{Z}\p{N}_.:/=+\-@]*)$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RejectedPatches`  <a name="cfn-ssm-patchbaseline-rejectedpatches"></a>
A list of explicitly rejected patches for the baseline\.  
For information about accepted formats for lists of approved patches and rejected patches, see [Package Name Formats for Approved and Rejected Patch Lists](https://docs.aws.amazon.com/systems-manager/latest/userguide/patch-manager-approved-rejected-package-name-formats.html) in the *AWS Systems Manager User Guide*\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RejectedPatchesAction`  <a name="cfn-ssm-patchbaseline-rejectedpatchesaction"></a>
The action for Patch Manager to take on patches included in the RejectedPackages list\.  
+  **ALLOW\_AS\_DEPENDENCY**: A package in the Rejected patches list is installed only if it is a dependency of another package\. It is considered compliant with the patch baseline, and its status is reported as *InstalledOther*\. This is the default action if no option is specified\.
+  **BLOCK**: Packages in the RejectedPatches list, and packages that include them as dependencies, are not installed under any circumstances\. If a package was installed before it was added to the Rejected patches list, it is considered non\-compliant with the patch baseline, and its status is reported as *InstalledRejected*\.
*Required*: No  
*Type*: String  
*Allowed Values*: `ALLOW_AS_DEPENDENCY | BLOCK`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Sources`  <a name="cfn-ssm-patchbaseline-sources"></a>
Information about the patches to use to update the instances, including target operating systems and source repositories\. Applies to Linux instances only\.  
*Required*: No  
*Type*: List of [PatchSource](aws-properties-ssm-patchbaseline-patchsource.md)  
*Maximum*: `20`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-ssm-patchbaseline-tags"></a>
Optional metadata that you assign to a resource\. Tags enable you to categorize a resource in different ways, such as by purpose, owner, or environment\. For example, you might want to tag a patch baseline to identify the severity level of patches it specifies and the operating system family it applies to\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `1000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-ssm-patchbaseline-return-values"></a>

### Ref<a name="aws-resource-ssm-patchbaseline-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the patch baseline ID, such as `pb-abcde1234567890yz`\.

**Note**  
The ID of the default patch baseline provided by AWS is an ARN, for example `arn:aws:ssm:us-west-2:123456789012:patchbaseline/abcde1234567890yz`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## See Also<a name="aws-resource-ssm-patchbaseline--seealso"></a>
+  [CreatePatchBaseline](https://docs.aws.amazon.com/systems-manager/latest/APIReference/API_CreatePatchBaseline.html) in the *AWS Systems Manager API Reference*\.