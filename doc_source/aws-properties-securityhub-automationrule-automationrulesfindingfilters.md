# AWS::SecurityHub::AutomationRule AutomationRulesFindingFilters<a name="aws-properties-securityhub-automationrule-automationrulesfindingfilters"></a>

 The criteria that determine which findings a rule applies to\. 

## Syntax<a name="aws-properties-securityhub-automationrule-automationrulesfindingfilters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-securityhub-automationrule-automationrulesfindingfilters-syntax.json"></a>

```
{
  "[AwsAccountId](#cfn-securityhub-automationrule-automationrulesfindingfilters-awsaccountid)" : [ StringFilter, ... ],
  "[CompanyName](#cfn-securityhub-automationrule-automationrulesfindingfilters-companyname)" : [ StringFilter, ... ],
  "[ComplianceAssociatedStandardsId](#cfn-securityhub-automationrule-automationrulesfindingfilters-complianceassociatedstandardsid)" : [ StringFilter, ... ],
  "[ComplianceSecurityControlId](#cfn-securityhub-automationrule-automationrulesfindingfilters-compliancesecuritycontrolid)" : [ StringFilter, ... ],
  "[ComplianceStatus](#cfn-securityhub-automationrule-automationrulesfindingfilters-compliancestatus)" : [ StringFilter, ... ],
  "[Confidence](#cfn-securityhub-automationrule-automationrulesfindingfilters-confidence)" : [ NumberFilter, ... ],
  "[CreatedAt](#cfn-securityhub-automationrule-automationrulesfindingfilters-createdat)" : [ DateFilter, ... ],
  "[Criticality](#cfn-securityhub-automationrule-automationrulesfindingfilters-criticality)" : [ NumberFilter, ... ],
  "[Description](#cfn-securityhub-automationrule-automationrulesfindingfilters-description)" : [ StringFilter, ... ],
  "[FirstObservedAt](#cfn-securityhub-automationrule-automationrulesfindingfilters-firstobservedat)" : [ DateFilter, ... ],
  "[GeneratorId](#cfn-securityhub-automationrule-automationrulesfindingfilters-generatorid)" : [ StringFilter, ... ],
  "[Id](#cfn-securityhub-automationrule-automationrulesfindingfilters-id)" : [ StringFilter, ... ],
  "[LastObservedAt](#cfn-securityhub-automationrule-automationrulesfindingfilters-lastobservedat)" : [ DateFilter, ... ],
  "[NoteText](#cfn-securityhub-automationrule-automationrulesfindingfilters-notetext)" : [ StringFilter, ... ],
  "[NoteUpdatedAt](#cfn-securityhub-automationrule-automationrulesfindingfilters-noteupdatedat)" : [ DateFilter, ... ],
  "[NoteUpdatedBy](#cfn-securityhub-automationrule-automationrulesfindingfilters-noteupdatedby)" : [ StringFilter, ... ],
  "[ProductArn](#cfn-securityhub-automationrule-automationrulesfindingfilters-productarn)" : [ StringFilter, ... ],
  "[ProductName](#cfn-securityhub-automationrule-automationrulesfindingfilters-productname)" : [ StringFilter, ... ],
  "[RecordState](#cfn-securityhub-automationrule-automationrulesfindingfilters-recordstate)" : [ StringFilter, ... ],
  "[RelatedFindingsId](#cfn-securityhub-automationrule-automationrulesfindingfilters-relatedfindingsid)" : [ StringFilter, ... ],
  "[RelatedFindingsProductArn](#cfn-securityhub-automationrule-automationrulesfindingfilters-relatedfindingsproductarn)" : [ StringFilter, ... ],
  "[ResourceDetailsOther](#cfn-securityhub-automationrule-automationrulesfindingfilters-resourcedetailsother)" : [ MapFilter, ... ],
  "[ResourceId](#cfn-securityhub-automationrule-automationrulesfindingfilters-resourceid)" : [ StringFilter, ... ],
  "[ResourcePartition](#cfn-securityhub-automationrule-automationrulesfindingfilters-resourcepartition)" : [ StringFilter, ... ],
  "[ResourceRegion](#cfn-securityhub-automationrule-automationrulesfindingfilters-resourceregion)" : [ StringFilter, ... ],
  "[ResourceTags](#cfn-securityhub-automationrule-automationrulesfindingfilters-resourcetags)" : [ MapFilter, ... ],
  "[ResourceType](#cfn-securityhub-automationrule-automationrulesfindingfilters-resourcetype)" : [ StringFilter, ... ],
  "[SeverityLabel](#cfn-securityhub-automationrule-automationrulesfindingfilters-severitylabel)" : [ StringFilter, ... ],
  "[SourceUrl](#cfn-securityhub-automationrule-automationrulesfindingfilters-sourceurl)" : [ StringFilter, ... ],
  "[Title](#cfn-securityhub-automationrule-automationrulesfindingfilters-title)" : [ StringFilter, ... ],
  "[Type](#cfn-securityhub-automationrule-automationrulesfindingfilters-type)" : [ StringFilter, ... ],
  "[UpdatedAt](#cfn-securityhub-automationrule-automationrulesfindingfilters-updatedat)" : [ DateFilter, ... ],
  "[UserDefinedFields](#cfn-securityhub-automationrule-automationrulesfindingfilters-userdefinedfields)" : [ MapFilter, ... ],
  "[VerificationState](#cfn-securityhub-automationrule-automationrulesfindingfilters-verificationstate)" : [ StringFilter, ... ],
  "[WorkflowStatus](#cfn-securityhub-automationrule-automationrulesfindingfilters-workflowstatus)" : [ StringFilter, ... ]
}
```

### YAML<a name="aws-properties-securityhub-automationrule-automationrulesfindingfilters-syntax.yaml"></a>

```
  [AwsAccountId](#cfn-securityhub-automationrule-automationrulesfindingfilters-awsaccountid): 
    - StringFilter
  [CompanyName](#cfn-securityhub-automationrule-automationrulesfindingfilters-companyname): 
    - StringFilter
  [ComplianceAssociatedStandardsId](#cfn-securityhub-automationrule-automationrulesfindingfilters-complianceassociatedstandardsid): 
    - StringFilter
  [ComplianceSecurityControlId](#cfn-securityhub-automationrule-automationrulesfindingfilters-compliancesecuritycontrolid): 
    - StringFilter
  [ComplianceStatus](#cfn-securityhub-automationrule-automationrulesfindingfilters-compliancestatus): 
    - StringFilter
  [Confidence](#cfn-securityhub-automationrule-automationrulesfindingfilters-confidence): 
    - NumberFilter
  [CreatedAt](#cfn-securityhub-automationrule-automationrulesfindingfilters-createdat): 
    - DateFilter
  [Criticality](#cfn-securityhub-automationrule-automationrulesfindingfilters-criticality): 
    - NumberFilter
  [Description](#cfn-securityhub-automationrule-automationrulesfindingfilters-description): 
    - StringFilter
  [FirstObservedAt](#cfn-securityhub-automationrule-automationrulesfindingfilters-firstobservedat): 
    - DateFilter
  [GeneratorId](#cfn-securityhub-automationrule-automationrulesfindingfilters-generatorid): 
    - StringFilter
  [Id](#cfn-securityhub-automationrule-automationrulesfindingfilters-id): 
    - StringFilter
  [LastObservedAt](#cfn-securityhub-automationrule-automationrulesfindingfilters-lastobservedat): 
    - DateFilter
  [NoteText](#cfn-securityhub-automationrule-automationrulesfindingfilters-notetext): 
    - StringFilter
  [NoteUpdatedAt](#cfn-securityhub-automationrule-automationrulesfindingfilters-noteupdatedat): 
    - DateFilter
  [NoteUpdatedBy](#cfn-securityhub-automationrule-automationrulesfindingfilters-noteupdatedby): 
    - StringFilter
  [ProductArn](#cfn-securityhub-automationrule-automationrulesfindingfilters-productarn): 
    - StringFilter
  [ProductName](#cfn-securityhub-automationrule-automationrulesfindingfilters-productname): 
    - StringFilter
  [RecordState](#cfn-securityhub-automationrule-automationrulesfindingfilters-recordstate): 
    - StringFilter
  [RelatedFindingsId](#cfn-securityhub-automationrule-automationrulesfindingfilters-relatedfindingsid): 
    - StringFilter
  [RelatedFindingsProductArn](#cfn-securityhub-automationrule-automationrulesfindingfilters-relatedfindingsproductarn): 
    - StringFilter
  [ResourceDetailsOther](#cfn-securityhub-automationrule-automationrulesfindingfilters-resourcedetailsother): 
    - MapFilter
  [ResourceId](#cfn-securityhub-automationrule-automationrulesfindingfilters-resourceid): 
    - StringFilter
  [ResourcePartition](#cfn-securityhub-automationrule-automationrulesfindingfilters-resourcepartition): 
    - StringFilter
  [ResourceRegion](#cfn-securityhub-automationrule-automationrulesfindingfilters-resourceregion): 
    - StringFilter
  [ResourceTags](#cfn-securityhub-automationrule-automationrulesfindingfilters-resourcetags): 
    - MapFilter
  [ResourceType](#cfn-securityhub-automationrule-automationrulesfindingfilters-resourcetype): 
    - StringFilter
  [SeverityLabel](#cfn-securityhub-automationrule-automationrulesfindingfilters-severitylabel): 
    - StringFilter
  [SourceUrl](#cfn-securityhub-automationrule-automationrulesfindingfilters-sourceurl): 
    - StringFilter
  [Title](#cfn-securityhub-automationrule-automationrulesfindingfilters-title): 
    - StringFilter
  [Type](#cfn-securityhub-automationrule-automationrulesfindingfilters-type): 
    - StringFilter
  [UpdatedAt](#cfn-securityhub-automationrule-automationrulesfindingfilters-updatedat): 
    - DateFilter
  [UserDefinedFields](#cfn-securityhub-automationrule-automationrulesfindingfilters-userdefinedfields): 
    - MapFilter
  [VerificationState](#cfn-securityhub-automationrule-automationrulesfindingfilters-verificationstate): 
    - StringFilter
  [WorkflowStatus](#cfn-securityhub-automationrule-automationrulesfindingfilters-workflowstatus): 
    - StringFilter
```

## Properties<a name="aws-properties-securityhub-automationrule-automationrulesfindingfilters-properties"></a>

`AwsAccountId`  <a name="cfn-securityhub-automationrule-automationrulesfindingfilters-awsaccountid"></a>
 The AWS account ID in which a finding was generated\.   
 Array Members: Minimum number of 1 item\. Maximum number of 100 items\.   
*Required*: No  
*Type*: List of [StringFilter](aws-properties-securityhub-automationrule-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CompanyName`  <a name="cfn-securityhub-automationrule-automationrulesfindingfilters-companyname"></a>
 The name of the company for the product that generated the finding\. For control\-based findings, the company is AWS\.   
 Array Members: Minimum number of 1 item\. Maximum number of 20 items\.   
*Required*: No  
*Type*: List of [StringFilter](aws-properties-securityhub-automationrule-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ComplianceAssociatedStandardsId`  <a name="cfn-securityhub-automationrule-automationrulesfindingfilters-complianceassociatedstandardsid"></a>
The unique identifier of a standard in which a control is enabled\. This field consists of the resource portion of the Amazon Resource Name \(ARN\) returned for a standard in the [DescribeStandards](https://docs.aws.amazon.com/securityhub/1.0/APIReference/API_DescribeStandards.html) API response\.  
 Array Members: Minimum number of 1 item\. Maximum number of 20 items\.   
*Required*: No  
*Type*: List of [StringFilter](aws-properties-securityhub-automationrule-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ComplianceSecurityControlId`  <a name="cfn-securityhub-automationrule-automationrulesfindingfilters-compliancesecuritycontrolid"></a>
 The security control ID for which a finding was generated\. Security control IDs are the same across standards\.  
 Array Members: Minimum number of 1 item\. Maximum number of 20 items\.   
*Required*: No  
*Type*: List of [StringFilter](aws-properties-securityhub-automationrule-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ComplianceStatus`  <a name="cfn-securityhub-automationrule-automationrulesfindingfilters-compliancestatus"></a>
 The result of a security check\. This field is only used for findings generated from controls\.   
 Array Members: Minimum number of 1 item\. Maximum number of 20 items\.   
*Required*: No  
*Type*: List of [StringFilter](aws-properties-securityhub-automationrule-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Confidence`  <a name="cfn-securityhub-automationrule-automationrulesfindingfilters-confidence"></a>
The likelihood that a finding accurately identifies the behavior or issue that it was intended to identify\. `Confidence` is scored on a 0–100 basis using a ratio scale\. A value of `0` means 0 percent confidence, and a value of `100` means 100 percent confidence\. For example, a data exfiltration detection based on a statistical deviation of network traffic has low confidence because an actual exfiltration hasn't been verified\. For more information, see [Confidence](https://docs.aws.amazon.com/securityhub/latest/userguide/asff-top-level-attributes.html#asff-confidence) in the * AWS Security Hub User Guide*\.  
 Array Members: Minimum number of 1 item\. Maximum number of 20 items\.   
*Required*: No  
*Type*: List of [NumberFilter](aws-properties-securityhub-automationrule-numberfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CreatedAt`  <a name="cfn-securityhub-automationrule-automationrulesfindingfilters-createdat"></a>
 A timestamp that indicates when this finding record was created\.   
Uses the `date-time` format specified in [RFC 3339 section 5\.6, Internet Date/Time Format](https://tools.ietf.org/html/rfc3339#section-5.6)\. The value cannot contain spaces\. For example, `2020-03-22T13:22:13.933Z`\.  
 Array Members: Minimum number of 1 item\. Maximum number of 20 items\.   
*Required*: No  
*Type*: List of [DateFilter](aws-properties-securityhub-automationrule-datefilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Criticality`  <a name="cfn-securityhub-automationrule-automationrulesfindingfilters-criticality"></a>
 The level of importance that is assigned to the resources that are associated with a finding\. `Criticality` is scored on a 0–100 basis, using a ratio scale that supports only full integers\. A score of `0` means that the underlying resources have no criticality, and a score of `100` is reserved for the most critical resources\. For more information, see [Criticality](https://docs.aws.amazon.com/securityhub/latest/userguide/asff-top-level-attributes.html#asff-criticality) in the * AWS Security Hub User Guide*\.  
 Array Members: Minimum number of 1 item\. Maximum number of 20 items\.   
*Required*: No  
*Type*: List of [NumberFilter](aws-properties-securityhub-automationrule-numberfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-securityhub-automationrule-automationrulesfindingfilters-description"></a>
 A finding's description\.   
 Array Members: Minimum number of 1 item\. Maximum number of 20 items\.   
*Required*: No  
*Type*: List of [StringFilter](aws-properties-securityhub-automationrule-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FirstObservedAt`  <a name="cfn-securityhub-automationrule-automationrulesfindingfilters-firstobservedat"></a>
 A timestamp that indicates when the potential security issue captured by a finding was first observed by the security findings product\.   
Uses the `date-time` format specified in [RFC 3339 section 5\.6, Internet Date/Time Format](https://tools.ietf.org/html/rfc3339#section-5.6)\. The value cannot contain spaces\. For example, `2020-03-22T13:22:13.933Z`\.  
 Array Members: Minimum number of 1 item\. Maximum number of 20 items\.   
*Required*: No  
*Type*: List of [DateFilter](aws-properties-securityhub-automationrule-datefilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GeneratorId`  <a name="cfn-securityhub-automationrule-automationrulesfindingfilters-generatorid"></a>
 The identifier for the solution\-specific component that generated a finding\.   
 Array Members: Minimum number of 1 item\. Maximum number of 100 items\.   
*Required*: No  
*Type*: List of [StringFilter](aws-properties-securityhub-automationrule-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Id`  <a name="cfn-securityhub-automationrule-automationrulesfindingfilters-id"></a>
 The product\-specific identifier for a finding\.   
 Array Members: Minimum number of 1 item\. Maximum number of 20 items\.   
*Required*: No  
*Type*: List of [StringFilter](aws-properties-securityhub-automationrule-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LastObservedAt`  <a name="cfn-securityhub-automationrule-automationrulesfindingfilters-lastobservedat"></a>
 A timestamp that indicates when the potential security issue captured by a finding was most recently observed by the security findings product\.   
Uses the `date-time` format specified in [RFC 3339 section 5\.6, Internet Date/Time Format](https://tools.ietf.org/html/rfc3339#section-5.6)\. The value cannot contain spaces\. For example, `2020-03-22T13:22:13.933Z`\.  
 Array Members: Minimum number of 1 item\. Maximum number of 20 items\.   
*Required*: No  
*Type*: List of [DateFilter](aws-properties-securityhub-automationrule-datefilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NoteText`  <a name="cfn-securityhub-automationrule-automationrulesfindingfilters-notetext"></a>
 The text of a user\-defined note that's added to a finding\.   
 Array Members: Minimum number of 1 item\. Maximum number of 20 items\.   
*Required*: No  
*Type*: List of [StringFilter](aws-properties-securityhub-automationrule-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NoteUpdatedAt`  <a name="cfn-securityhub-automationrule-automationrulesfindingfilters-noteupdatedat"></a>
 The timestamp of when the note was updated\. Uses the date\-time format specified in [RFC 3339 section 5\.6, Internet Date/Time Format](https://www.rfc-editor.org/rfc/rfc3339#section-5.6)\. The value cannot contain spaces\. For example, `2020-03-22T13:22:13.933Z`\.   
 Array Members: Minimum number of 1 item\. Maximum number of 20 items\.   
*Required*: No  
*Type*: List of [DateFilter](aws-properties-securityhub-automationrule-datefilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NoteUpdatedBy`  <a name="cfn-securityhub-automationrule-automationrulesfindingfilters-noteupdatedby"></a>
 The principal that created a note\.   
 Array Members: Minimum number of 1 item\. Maximum number of 20 items\.   
*Required*: No  
*Type*: List of [StringFilter](aws-properties-securityhub-automationrule-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProductArn`  <a name="cfn-securityhub-automationrule-automationrulesfindingfilters-productarn"></a>
 The Amazon Resource Name \(ARN\) for a third\-party product that generated a finding in Security Hub\.   
 Array Members: Minimum number of 1 item\. Maximum number of 20 items\.   
*Required*: No  
*Type*: List of [StringFilter](aws-properties-securityhub-automationrule-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProductName`  <a name="cfn-securityhub-automationrule-automationrulesfindingfilters-productname"></a>
 Provides the name of the product that generated the finding\. For control\-based findings, the product name is Security Hub\.   
 Array Members: Minimum number of 1 item\. Maximum number of 20 items\.   
*Required*: No  
*Type*: List of [StringFilter](aws-properties-securityhub-automationrule-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RecordState`  <a name="cfn-securityhub-automationrule-automationrulesfindingfilters-recordstate"></a>
 Provides the current state of a finding\.   
 Array Members: Minimum number of 1 item\. Maximum number of 20 items\.   
*Required*: No  
*Type*: List of [StringFilter](aws-properties-securityhub-automationrule-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RelatedFindingsId`  <a name="cfn-securityhub-automationrule-automationrulesfindingfilters-relatedfindingsid"></a>
 The product\-generated identifier for a related finding\.   
 Array Members: Minimum number of 1 item\. Maximum number of 20 items\.   
*Required*: No  
*Type*: List of [StringFilter](aws-properties-securityhub-automationrule-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RelatedFindingsProductArn`  <a name="cfn-securityhub-automationrule-automationrulesfindingfilters-relatedfindingsproductarn"></a>
 The ARN for the product that generated a related finding\.   
 Array Members: Minimum number of 1 item\. Maximum number of 20 items\.   
*Required*: No  
*Type*: List of [StringFilter](aws-properties-securityhub-automationrule-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceDetailsOther`  <a name="cfn-securityhub-automationrule-automationrulesfindingfilters-resourcedetailsother"></a>
 Custom fields and values about the resource that a finding pertains to\.   
 Array Members: Minimum number of 1 item\. Maximum number of 20 items\.   
*Required*: No  
*Type*: List of [MapFilter](aws-properties-securityhub-automationrule-mapfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceId`  <a name="cfn-securityhub-automationrule-automationrulesfindingfilters-resourceid"></a>
 The identifier for the given resource type\. For AWS resources that are identified by Amazon Resource Names \(ARNs\), this is the ARN\. For AWS resources that lack ARNs, this is the identifier as defined by the AWS service that created the resource\. For non\-AWS resources, this is a unique identifier that is associated with the resource\.   
 Array Members: Minimum number of 1 item\. Maximum number of 100 items\.   
*Required*: No  
*Type*: List of [StringFilter](aws-properties-securityhub-automationrule-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourcePartition`  <a name="cfn-securityhub-automationrule-automationrulesfindingfilters-resourcepartition"></a>
 The partition in which the resource that the finding pertains to is located\. A partition is a group of AWS Regions\. Each AWS account is scoped to one partition\.   
 Array Members: Minimum number of 1 item\. Maximum number of 20 items\.   
*Required*: No  
*Type*: List of [StringFilter](aws-properties-securityhub-automationrule-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceRegion`  <a name="cfn-securityhub-automationrule-automationrulesfindingfilters-resourceregion"></a>
 The AWS Region where the resource that a finding pertains to is located\.   
 Array Members: Minimum number of 1 item\. Maximum number of 20 items\.   
*Required*: No  
*Type*: List of [StringFilter](aws-properties-securityhub-automationrule-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceTags`  <a name="cfn-securityhub-automationrule-automationrulesfindingfilters-resourcetags"></a>
 A list of AWS tags associated with a resource at the time the finding was processed\.   
 Array Members: Minimum number of 1 item\. Maximum number of 20 items\.   
*Required*: No  
*Type*: List of [MapFilter](aws-properties-securityhub-automationrule-mapfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceType`  <a name="cfn-securityhub-automationrule-automationrulesfindingfilters-resourcetype"></a>
 A finding's title\.   
 Array Members: Minimum number of 1 item\. Maximum number of 100 items\.   
*Required*: No  
*Type*: List of [StringFilter](aws-properties-securityhub-automationrule-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SeverityLabel`  <a name="cfn-securityhub-automationrule-automationrulesfindingfilters-severitylabel"></a>
 The severity value of the finding\.   
 Array Members: Minimum number of 1 item\. Maximum number of 20 items\.   
*Required*: No  
*Type*: List of [StringFilter](aws-properties-securityhub-automationrule-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceUrl`  <a name="cfn-securityhub-automationrule-automationrulesfindingfilters-sourceurl"></a>
 Provides a URL that links to a page about the current finding in the finding product\.   
 Array Members: Minimum number of 1 item\. Maximum number of 20 items\.   
*Required*: No  
*Type*: List of [StringFilter](aws-properties-securityhub-automationrule-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Title`  <a name="cfn-securityhub-automationrule-automationrulesfindingfilters-title"></a>
 A finding's title\.   
 Array Members: Minimum number of 1 item\. Maximum number of 100 items\.   
*Required*: No  
*Type*: List of [StringFilter](aws-properties-securityhub-automationrule-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-securityhub-automationrule-automationrulesfindingfilters-type"></a>
 One or more finding types in the format of namespace/category/classifier that classify a finding\. For a list of namespaces, classifiers, and categories, see [Types taxonomy for ASFF](https://docs.aws.amazon.com/securityhub/latest/userguide/securityhub-findings-format-type-taxonomy.html) in the * AWS Security Hub User Guide*\.  
 Array Members: Minimum number of 1 item\. Maximum number of 20 items\.   
*Required*: No  
*Type*: List of [StringFilter](aws-properties-securityhub-automationrule-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UpdatedAt`  <a name="cfn-securityhub-automationrule-automationrulesfindingfilters-updatedat"></a>
 A timestamp that indicates when the finding record was most recently updated\.   
Uses the `date-time` format specified in [RFC 3339 section 5\.6, Internet Date/Time Format](https://tools.ietf.org/html/rfc3339#section-5.6)\. The value cannot contain spaces\. For example, `2020-03-22T13:22:13.933Z`\.  
 Array Members: Minimum number of 1 item\. Maximum number of 20 items\.   
*Required*: No  
*Type*: List of [DateFilter](aws-properties-securityhub-automationrule-datefilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserDefinedFields`  <a name="cfn-securityhub-automationrule-automationrulesfindingfilters-userdefinedfields"></a>
 A list of user\-defined name and value string pairs added to a finding\.   
 Array Members: Minimum number of 1 item\. Maximum number of 20 items\.   
*Required*: No  
*Type*: List of [MapFilter](aws-properties-securityhub-automationrule-mapfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VerificationState`  <a name="cfn-securityhub-automationrule-automationrulesfindingfilters-verificationstate"></a>
 Provides the veracity of a finding\.   
 Array Members: Minimum number of 1 item\. Maximum number of 20 items\.   
*Required*: No  
*Type*: List of [StringFilter](aws-properties-securityhub-automationrule-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WorkflowStatus`  <a name="cfn-securityhub-automationrule-automationrulesfindingfilters-workflowstatus"></a>
 Provides information about the status of the investigation into a finding\.   
 Array Members: Minimum number of 1 item\. Maximum number of 20 items\.   
*Required*: No  
*Type*: List of [StringFilter](aws-properties-securityhub-automationrule-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)