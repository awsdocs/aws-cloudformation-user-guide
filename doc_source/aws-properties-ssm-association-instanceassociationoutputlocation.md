# AWS Systems Manager Association InstanceAssociationOutputLocation<a name="aws-properties-ssm-association-instanceassociationoutputlocation"></a>

`InstanceAssociationOutputLocation` is a property of the [AWS::SSM::Association](aws-resource-ssm-association.md) resource that specifies an Amazon S3 bucket where you want to store the results of this association request\.

## Syntax<a name="w3ab2c21c14e1926b5"></a>

### JSON<a name="aws-properties-ssm-association-instanceassociationoutputlocation-syntax.json"></a>

```
{
  "[S3Location](#cfn-ssm-association-instanceassociationoutputlocation-s3location)" : [*S3OutputLocation*](aws-properties-ssm-association-s3outputlocation.md)
}
```

### YAML<a name="aws-properties-ssm-association-instanceassociationoutputlocation-syntax.yaml"></a>

```
[S3Location](#cfn-ssm-association-instanceassociationoutputlocation-s3location): [*S3OutputLocation*](aws-properties-ssm-association-s3outputlocation.md)
```

## Properties<a name="w3ab2c21c14e1926b7"></a>

`S3Location`  <a name="cfn-ssm-association-instanceassociationoutputlocation-s3location"></a>
An Amazon S3 bucket where you want to store the results of this request\.  
*Required*: No  
*Type*: [Systems Manager Association S3OutputLocation](aws-properties-ssm-association-s3outputlocation.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)