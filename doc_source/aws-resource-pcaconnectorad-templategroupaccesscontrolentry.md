# AWS::PCAConnectorAD::TemplateGroupAccessControlEntry<a name="aws-resource-pcaconnectorad-templategroupaccesscontrolentry"></a>

Create a group access control entry\. Allow or deny Active Directory groups from enrolling and/or autoenrolling with the template based on the group security identifiers \(SIDs\)\.

## Syntax<a name="aws-resource-pcaconnectorad-templategroupaccesscontrolentry-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-pcaconnectorad-templategroupaccesscontrolentry-syntax.json"></a>

```
{
  "Type" : "AWS::PCAConnectorAD::TemplateGroupAccessControlEntry",
  "Properties" : {
      "[AccessRights](#cfn-pcaconnectorad-templategroupaccesscontrolentry-accessrights)" : AccessRights,
      "[GroupDisplayName](#cfn-pcaconnectorad-templategroupaccesscontrolentry-groupdisplayname)" : String,
      "[GroupSecurityIdentifier](#cfn-pcaconnectorad-templategroupaccesscontrolentry-groupsecurityidentifier)" : String,
      "[TemplateArn](#cfn-pcaconnectorad-templategroupaccesscontrolentry-templatearn)" : String
    }
}
```

### YAML<a name="aws-resource-pcaconnectorad-templategroupaccesscontrolentry-syntax.yaml"></a>

```
Type: AWS::PCAConnectorAD::TemplateGroupAccessControlEntry
Properties: 
  [AccessRights](#cfn-pcaconnectorad-templategroupaccesscontrolentry-accessrights): 
    AccessRights
  [GroupDisplayName](#cfn-pcaconnectorad-templategroupaccesscontrolentry-groupdisplayname): String
  [GroupSecurityIdentifier](#cfn-pcaconnectorad-templategroupaccesscontrolentry-groupsecurityidentifier): String
  [TemplateArn](#cfn-pcaconnectorad-templategroupaccesscontrolentry-templatearn): String
```

## Properties<a name="aws-resource-pcaconnectorad-templategroupaccesscontrolentry-properties"></a>

`AccessRights`  <a name="cfn-pcaconnectorad-templategroupaccesscontrolentry-accessrights"></a>
Permissions to allow or deny an Active Directory group to enroll or autoenroll certificates issued against a template\.  
*Required*: Yes  
*Type*: [AccessRights](aws-properties-pcaconnectorad-templategroupaccesscontrolentry-accessrights.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GroupDisplayName`  <a name="cfn-pcaconnectorad-templategroupaccesscontrolentry-groupdisplayname"></a>
Name of the Active Directory group\. This name does not need to match the group name in Active Directory\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Pattern*: `[\x20-\x7E]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GroupSecurityIdentifier`  <a name="cfn-pcaconnectorad-templategroupaccesscontrolentry-groupsecurityidentifier"></a>
Security identifier \(SID\) of the group object from Active Directory\. The SID starts with "S\-"\.  
*Required*: No  
*Type*: String  
*Minimum*: `7`  
*Maximum*: `256`  
*Pattern*: `S-[0-9]-([0-9]+-){1,14}[0-9]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TemplateArn`  <a name="cfn-pcaconnectorad-templategroupaccesscontrolentry-templatearn"></a>
The Amazon Resource Name \(ARN\) that was returned when you called [CreateTemplate](https://docs.aws.amazon.com/pca-connector-ad/latest/APIReference/API_CreateTemplate.html)\.  
*Required*: No  
*Type*: String  
*Minimum*: `5`  
*Maximum*: `200`  
*Pattern*: `arn:[\w-]+:pca-connector-ad:[\w-]+:[0-9]+:connector\/[0-9a-f]{8}(-[0-9a-f]{4}){3}-[0-9a-f]{12}\/template\/[0-9a-f]{8}(-[0-9a-f]{4}){3}-[0-9a-f]{12}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)