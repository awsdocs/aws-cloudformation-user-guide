# AWS::PCAConnectorAD::TemplateGroupAccessControlEntry AccessRights<a name="aws-properties-pcaconnectorad-templategroupaccesscontrolentry-accessrights"></a>

 Allow or deny permissions for an Active Directory group to enroll or autoenroll certificates for a template\.

## Syntax<a name="aws-properties-pcaconnectorad-templategroupaccesscontrolentry-accessrights-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pcaconnectorad-templategroupaccesscontrolentry-accessrights-syntax.json"></a>

```
{
  "[AutoEnroll](#cfn-pcaconnectorad-templategroupaccesscontrolentry-accessrights-autoenroll)" : String,
  "[Enroll](#cfn-pcaconnectorad-templategroupaccesscontrolentry-accessrights-enroll)" : String
}
```

### YAML<a name="aws-properties-pcaconnectorad-templategroupaccesscontrolentry-accessrights-syntax.yaml"></a>

```
  [AutoEnroll](#cfn-pcaconnectorad-templategroupaccesscontrolentry-accessrights-autoenroll): String
  [Enroll](#cfn-pcaconnectorad-templategroupaccesscontrolentry-accessrights-enroll): String
```

## Properties<a name="aws-properties-pcaconnectorad-templategroupaccesscontrolentry-accessrights-properties"></a>

`AutoEnroll`  <a name="cfn-pcaconnectorad-templategroupaccesscontrolentry-accessrights-autoenroll"></a>
Allow or deny an Active Directory group from autoenrolling certificates issued against a template\. The Active Directory group must be allowed to enroll to allow autoenrollment  
*Required*: No  
*Type*: String  
*Allowed values*: `ALLOW | DENY`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enroll`  <a name="cfn-pcaconnectorad-templategroupaccesscontrolentry-accessrights-enroll"></a>
Allow or deny an Active Directory group from enrolling certificates issued against a template\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ALLOW | DENY`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)