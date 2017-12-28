# AWS::SSM::PatchBaseline<a name="aws-resource-ssm-patchbaseline"></a>

The `AWS::SSM::PatchBaseline` resource defines the basic information for an Amazon EC2 Systems Manager patch baseline\. A patch baseline defines which patches are approved for installation on your instances\. For more information, see [ CreatePatchBaseline](http://docs.aws.amazon.com/systems-manager/latest/APIReference/API_CreatePatchBaseline.html) in the *Amazon EC2 Systems Manager API Reference*\.

## Syntax<a name="aws-resource-ssm-patchbaseline-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ssm-patchbaseline-syntax.json"></a>

```
{
  "Type" : "AWS::SSM::PatchBaseline",
  "Properties" : {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-patchbaseline-operatingsystem)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-patchbaseline-approvedpatches)" : [ String, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-patchbaseline-patchgroups)" : [ String, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-patchbaseline-description)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-patchbaseline-approvedpatchescompliancelevel)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-patchbaseline-approvalrules)" : RuleGroup,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-patchbaseline-globalfilters)" : PatchFilterGroup,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-patchbaseline-name)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-patchbaseline-rejectedpatches)" : [ String, ... ]
  }
}
```

### YAML<a name="aws-resource-ssm-patchbaseline-syntax.yaml"></a>

```
Type: "AWS::SSM::PatchBaseline"
Properties:
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-patchbaseline-operatingsystem): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-patchbaseline-approvedpatches): 
    - String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-patchbaseline-patchgroups): 
    - String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-patchbaseline-description): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-patchbaseline-approvedpatchescompliancelevel): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-patchbaseline-approvalrules):
    RuleGroup
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-patchbaseline-globalfilters):
    PatchFilterGroup
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-patchbaseline-name): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-patchbaseline-rejectedpatches): 
    - String
```

## Properties<a name="aws-resource-ssm-patchbaseline-properties"></a>

`OperatingSystem`  
Defines the operating system that the patch baseline applies to\. Supported operating systems include `WINDOWS`, `AMAZON_LINUX`, `UBUNTU`, and `REDHAT_ENTERPRISE_LINUX`\. The default value is `WINDOWS`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: Replacement 

`ApprovedPatches`  
A list of explicitly approved patches for the baseline\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: No interruption 

`PatchGroups`  
The names of the patch groups to register with the patch baseline\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: No interruption 

`Description`  
A description of the patch baseline\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

`ApprovedPatchesComplianceLevel`  
The compliance level for approved patches\. This means that if an approved patch is reported as missing, this is the severity of the compliance violation\. Valid compliance severity levels include the following: `CRITICAL`, `HIGH`, `MEDIUM`, `LOW`, `INFORMATIONAL`, and `UNSPECIFIED`\. The default value is `UNSPECIFIED`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

`ApprovalRules`  
A set of rules that are used to include patches in the baseline\.  
 *Required*: No  
 *Type*: [SSM PatchBaseline RuleGroup](aws-properties-ssm-patchbaseline-rulegroup.md)  
 *Update requires*: No interruption 

`GlobalFilters`  
A set of global filters that are used to exclude patches from the baseline\.  
 *Required*: No  
 *Type*: [SSM PatchBaseline PatchFilterGroup](aws-properties-ssm-patchbaseline-patchfiltergroup.md)  
 *Update requires*: No interruption 

`Name`  
The name of the patch baseline\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: No interruption 

`RejectedPatches`  
A list of explicitly rejected patches for the baseline\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: No interruption 

## Return Values<a name="aws-resource-ssm-patchbaseline-returnvalues"></a>

### Ref<a name="w3ab2c21c10e1024b9b3"></a>

When you pass the logical ID of an `AWS::SSM::PatchBaseline` resource to the intrinsic `Ref` function, the function returns the physical ID of the resource, such as `pb-abcde1234567890yz`\. 

**Note**  
The ID of the default patch baseline provided by AWS is an ARN—for example `arn:aws:ssm:us-west-2:123456789012:patchbaseline/abcde1234567890yz`\.

For more information about using the `Ref` function, see Ref\. 

## See Also<a name="aws-resource-ssm-patchbaseline-seealso"></a>

+ [ CreatePatchBaseline](http://docs.aws.amazon.com/systems-manager/latest/APIReference/API_CreatePatchBaseline.html) in the *Amazon EC2 Systems Manager API Reference*