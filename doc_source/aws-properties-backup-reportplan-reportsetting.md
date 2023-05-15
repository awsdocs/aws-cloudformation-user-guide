# AWS::Backup::ReportPlan ReportSetting<a name="aws-properties-backup-reportplan-reportsetting"></a>

Contains detailed information about a report setting\.

## Syntax<a name="aws-properties-backup-reportplan-reportsetting-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-backup-reportplan-reportsetting-syntax.json"></a>

```
{
  "[Accounts](#cfn-backup-reportplan-reportsetting-accounts)" : [ String, ... ],
  "[FrameworkArns](#cfn-backup-reportplan-reportsetting-frameworkarns)" : [ String, ... ],
  "[OrganizationUnits](#cfn-backup-reportplan-reportsetting-organizationunits)" : [ String, ... ],
  "[Regions](#cfn-backup-reportplan-reportsetting-regions)" : [ String, ... ],
  "[ReportTemplate](#cfn-backup-reportplan-reportsetting-reporttemplate)" : String
}
```

### YAML<a name="aws-properties-backup-reportplan-reportsetting-syntax.yaml"></a>

```
  [Accounts](#cfn-backup-reportplan-reportsetting-accounts): 
    - String
  [FrameworkArns](#cfn-backup-reportplan-reportsetting-frameworkarns): 
    - String
  [OrganizationUnits](#cfn-backup-reportplan-reportsetting-organizationunits): 
    - String
  [Regions](#cfn-backup-reportplan-reportsetting-regions): 
    - String
  [ReportTemplate](#cfn-backup-reportplan-reportsetting-reporttemplate): String
```

## Properties<a name="aws-properties-backup-reportplan-reportsetting-properties"></a>

`Accounts`  <a name="cfn-backup-reportplan-reportsetting-accounts"></a>
These are the accounts to be included in the report\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FrameworkArns`  <a name="cfn-backup-reportplan-reportsetting-frameworkarns"></a>
The Amazon Resource Names \(ARNs\) of the frameworks a report covers\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OrganizationUnits`  <a name="cfn-backup-reportplan-reportsetting-organizationunits"></a>
These are the Organizational Units to be included in the report\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Regions`  <a name="cfn-backup-reportplan-reportsetting-regions"></a>
These are the Regions to be included in the report\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReportTemplate`  <a name="cfn-backup-reportplan-reportsetting-reporttemplate"></a>
Identifies the report template for the report\. Reports are built using a report template\. The report templates are:  
 `RESOURCE_COMPLIANCE_REPORT | CONTROL_COMPLIANCE_REPORT | BACKUP_JOB_REPORT | COPY_JOB_REPORT | RESTORE_JOB_REPORT`   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)