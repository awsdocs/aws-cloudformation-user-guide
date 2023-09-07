# AWS::PCAConnectorAD::Template GeneralFlagsV3<a name="aws-properties-pcaconnectorad-template-generalflagsv3"></a>

General flags for v3 template schema that defines if the template is for a machine or a user and if the template can be issued using autoenrollment\.

## Syntax<a name="aws-properties-pcaconnectorad-template-generalflagsv3-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pcaconnectorad-template-generalflagsv3-syntax.json"></a>

```
{
  "[AutoEnrollment](#cfn-pcaconnectorad-template-generalflagsv3-autoenrollment)" : Boolean,
  "[MachineType](#cfn-pcaconnectorad-template-generalflagsv3-machinetype)" : Boolean
}
```

### YAML<a name="aws-properties-pcaconnectorad-template-generalflagsv3-syntax.yaml"></a>

```
  [AutoEnrollment](#cfn-pcaconnectorad-template-generalflagsv3-autoenrollment): Boolean
  [MachineType](#cfn-pcaconnectorad-template-generalflagsv3-machinetype): Boolean
```

## Properties<a name="aws-properties-pcaconnectorad-template-generalflagsv3-properties"></a>

`AutoEnrollment`  <a name="cfn-pcaconnectorad-template-generalflagsv3-autoenrollment"></a>
Allows certificate issuance using autoenrollment\. Set to TRUE to allow autoenrollment\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MachineType`  <a name="cfn-pcaconnectorad-template-generalflagsv3-machinetype"></a>
Defines if the template is for machines or users\. Set to TRUE if the template is for machines\. Set to FALSE if the template is for users  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)