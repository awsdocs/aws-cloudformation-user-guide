# AWS::SSM::Association InstanceAssociationOutputLocation<a name="aws-properties-ssm-association-instanceassociationoutputlocation"></a>

 `InstanceAssociationOutputLocation` is a property of the [AWS::SSM::Association](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ssm-association.html) resource that specifies an Amazon S3 bucket where you want to store the results of this association request\.

## Syntax<a name="aws-properties-ssm-association-instanceassociationoutputlocation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssm-association-instanceassociationoutputlocation-syntax.json"></a>

```
{
  "[S3Location](#cfn-ssm-association-instanceassociationoutputlocation-s3location)" : S3OutputLocation
}
```

### YAML<a name="aws-properties-ssm-association-instanceassociationoutputlocation-syntax.yaml"></a>

```
  [S3Location](#cfn-ssm-association-instanceassociationoutputlocation-s3location): 
    S3OutputLocation
```

## Properties<a name="aws-properties-ssm-association-instanceassociationoutputlocation-properties"></a>

`S3Location`  <a name="cfn-ssm-association-instanceassociationoutputlocation-s3location"></a>
 `S3OutputLocation` is a property of the [InstanceAssociationOutputLocation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ssm-association-instanceassociationoutputlocation.html) property that specifies an Amazon S3 bucket where you want to store the results of this request\.   
*Required*: No  
*Type*: [S3OutputLocation](aws-properties-ssm-association-s3outputlocation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)