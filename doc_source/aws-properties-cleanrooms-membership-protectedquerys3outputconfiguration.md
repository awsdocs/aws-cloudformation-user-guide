# AWS::CleanRooms::Membership ProtectedQueryS3OutputConfiguration<a name="aws-properties-cleanrooms-membership-protectedquerys3outputconfiguration"></a>

Contains the configuration to write the query results to S3\.

## Syntax<a name="aws-properties-cleanrooms-membership-protectedquerys3outputconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cleanrooms-membership-protectedquerys3outputconfiguration-syntax.json"></a>

```
{
  "[Bucket](#cfn-cleanrooms-membership-protectedquerys3outputconfiguration-bucket)" : String,
  "[KeyPrefix](#cfn-cleanrooms-membership-protectedquerys3outputconfiguration-keyprefix)" : String,
  "[ResultFormat](#cfn-cleanrooms-membership-protectedquerys3outputconfiguration-resultformat)" : String
}
```

### YAML<a name="aws-properties-cleanrooms-membership-protectedquerys3outputconfiguration-syntax.yaml"></a>

```
  [Bucket](#cfn-cleanrooms-membership-protectedquerys3outputconfiguration-bucket): String
  [KeyPrefix](#cfn-cleanrooms-membership-protectedquerys3outputconfiguration-keyprefix): String
  [ResultFormat](#cfn-cleanrooms-membership-protectedquerys3outputconfiguration-resultformat): String
```

## Properties<a name="aws-properties-cleanrooms-membership-protectedquerys3outputconfiguration-properties"></a>

`Bucket`  <a name="cfn-cleanrooms-membership-protectedquerys3outputconfiguration-bucket"></a>
The S3 bucket to unload the protected query results\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `63`  
*Pattern*: `.*(?!^(\d+\.)+\d+$)(^(([a-z0-9]|[a-z0-9][a-z0-9\-]*[a-z0-9])\.)*([a-z0-9]|[a-z0-9][a-z0-9\-]*[a-z0-9])$).*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KeyPrefix`  <a name="cfn-cleanrooms-membership-protectedquerys3outputconfiguration-keyprefix"></a>
The S3 prefix to unload the protected query results\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `512`  
*Pattern*: `[\w!.=*/-]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResultFormat`  <a name="cfn-cleanrooms-membership-protectedquerys3outputconfiguration-resultformat"></a>
Intended file format of the result\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `CSV | PARQUET`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)