# AWS::SSM::ResourceDataSync AwsOrganizationsSource<a name="aws-properties-ssm-resourcedatasync-awsorganizationssource"></a>

Information about the AwsOrganizationsSource resource data sync source\. A sync source of this type can synchronize data from AWS Organizations or, if an AWS Organization is not present, from multiple AWS Regions\.

## Syntax<a name="aws-properties-ssm-resourcedatasync-awsorganizationssource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssm-resourcedatasync-awsorganizationssource-syntax.json"></a>

```
{
  "[OrganizationalUnits](#cfn-ssm-resourcedatasync-awsorganizationssource-organizationalunits)" : [ String, ... ],
  "[OrganizationSourceType](#cfn-ssm-resourcedatasync-awsorganizationssource-organizationsourcetype)" : String
}
```

### YAML<a name="aws-properties-ssm-resourcedatasync-awsorganizationssource-syntax.yaml"></a>

```
  [OrganizationalUnits](#cfn-ssm-resourcedatasync-awsorganizationssource-organizationalunits): 
    - String
  [OrganizationSourceType](#cfn-ssm-resourcedatasync-awsorganizationssource-organizationsourcetype): String
```

## Properties<a name="aws-properties-ssm-resourcedatasync-awsorganizationssource-properties"></a>

`OrganizationalUnits`  <a name="cfn-ssm-resourcedatasync-awsorganizationssource-organizationalunits"></a>
The AWS Organizations organization units included in the sync\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `1000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OrganizationSourceType`  <a name="cfn-ssm-resourcedatasync-awsorganizationssource-organizationsourcetype"></a>
If an AWS Organization is present, this is either `OrganizationalUnits` or `EntireOrganization`\. For `OrganizationalUnits`, the data is aggregated from a set of organization units\. For `EntireOrganization`, the data is aggregated from the entire AWS Organization\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)