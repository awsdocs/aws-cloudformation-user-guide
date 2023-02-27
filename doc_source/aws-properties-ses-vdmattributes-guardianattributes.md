# AWS::SES::VdmAttributes GuardianAttributes<a name="aws-properties-ses-vdmattributes-guardianattributes"></a>

Settings for your VDM configuration as applicable to the Guardian\.

## Syntax<a name="aws-properties-ses-vdmattributes-guardianattributes-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ses-vdmattributes-guardianattributes-syntax.json"></a>

```
{
  "[OptimizedSharedDelivery](#cfn-ses-vdmattributes-guardianattributes-optimizedshareddelivery)" : String
}
```

### YAML<a name="aws-properties-ses-vdmattributes-guardianattributes-syntax.yaml"></a>

```
  [OptimizedSharedDelivery](#cfn-ses-vdmattributes-guardianattributes-optimizedshareddelivery): String
```

## Properties<a name="aws-properties-ses-vdmattributes-guardianattributes-properties"></a>

`OptimizedSharedDelivery`  <a name="cfn-ses-vdmattributes-guardianattributes-optimizedshareddelivery"></a>
Specifies the status of your VDM optimized shared delivery\. Can be one of the following:  
+ `ENABLED` – Amazon SES enables optimized shared delivery for your account\.
+ `DISABLED` – Amazon SES disables optimized shared delivery for your account\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)