# AWS::RolesAnywhere::TrustAnchor Source<a name="aws-properties-rolesanywhere-trustanchor-source"></a>

The trust anchor type and its related certificate data\.

## Syntax<a name="aws-properties-rolesanywhere-trustanchor-source-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-rolesanywhere-trustanchor-source-syntax.json"></a>

```
{
  "[SourceData](#cfn-rolesanywhere-trustanchor-source-sourcedata)" : SourceData,
  "[SourceType](#cfn-rolesanywhere-trustanchor-source-sourcetype)" : String
}
```

### YAML<a name="aws-properties-rolesanywhere-trustanchor-source-syntax.yaml"></a>

```
  [SourceData](#cfn-rolesanywhere-trustanchor-source-sourcedata): 
    SourceData
  [SourceType](#cfn-rolesanywhere-trustanchor-source-sourcetype): String
```

## Properties<a name="aws-properties-rolesanywhere-trustanchor-source-properties"></a>

`SourceData`  <a name="cfn-rolesanywhere-trustanchor-source-sourcedata"></a>
The data field of the trust anchor depending on its type\.   
*Required*: No  
*Type*: [SourceData](aws-properties-rolesanywhere-trustanchor-sourcedata.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceType`  <a name="cfn-rolesanywhere-trustanchor-source-sourcetype"></a>
The type of the trust anchor\.   
*Required*: No  
*Type*: String  
*Allowed values*: `AWS_ACM_PCA | CERTIFICATE_BUNDLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)