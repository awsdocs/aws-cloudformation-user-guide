# AWS::SSM::ResourceDataSync SyncSource<a name="aws-properties-ssm-resourcedatasync-syncsource"></a>

Information about the source of the data included in the resource data sync\.

## Syntax<a name="aws-properties-ssm-resourcedatasync-syncsource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssm-resourcedatasync-syncsource-syntax.json"></a>

```
{
  "[AwsOrganizationsSource](#cfn-ssm-resourcedatasync-syncsource-awsorganizationssource)" : AwsOrganizationsSource,
  "[IncludeFutureRegions](#cfn-ssm-resourcedatasync-syncsource-includefutureregions)" : Boolean,
  "[SourceRegions](#cfn-ssm-resourcedatasync-syncsource-sourceregions)" : [ String, ... ],
  "[SourceType](#cfn-ssm-resourcedatasync-syncsource-sourcetype)" : String
}
```

### YAML<a name="aws-properties-ssm-resourcedatasync-syncsource-syntax.yaml"></a>

```
  [AwsOrganizationsSource](#cfn-ssm-resourcedatasync-syncsource-awsorganizationssource): 
    AwsOrganizationsSource
  [IncludeFutureRegions](#cfn-ssm-resourcedatasync-syncsource-includefutureregions): Boolean
  [SourceRegions](#cfn-ssm-resourcedatasync-syncsource-sourceregions): 
    - String
  [SourceType](#cfn-ssm-resourcedatasync-syncsource-sourcetype): String
```

## Properties<a name="aws-properties-ssm-resourcedatasync-syncsource-properties"></a>

`AwsOrganizationsSource`  <a name="cfn-ssm-resourcedatasync-syncsource-awsorganizationssource"></a>
Information about the AwsOrganizationsSource resource data sync source\. A sync source of this type can synchronize data from AWS Organizations\.  
*Required*: No  
*Type*: [AwsOrganizationsSource](aws-properties-ssm-resourcedatasync-awsorganizationssource.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludeFutureRegions`  <a name="cfn-ssm-resourcedatasync-syncsource-includefutureregions"></a>
Whether to automatically synchronize and aggregate data from new AWS Regions when those Regions come online\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceRegions`  <a name="cfn-ssm-resourcedatasync-syncsource-sourceregions"></a>
The `SyncSource` AWS Regions included in the resource data sync\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceType`  <a name="cfn-ssm-resourcedatasync-syncsource-sourcetype"></a>
The type of data source for the resource data sync\. `SourceType` is either `AwsOrganizations` \(if an organization is present in AWS Organizations\) or `singleAccountMultiRegions`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)