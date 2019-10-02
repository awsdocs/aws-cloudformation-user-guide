# AWS::LakeFormation::DataLakeSettings<a name="aws-resource-lakeformation-datalakesettings"></a>

The AWS::LakeFormation::DataLakeSettings resource is an AWS Lake Formation resource type that manages data lake settings\.

## Syntax<a name="aws-resource-lakeformation-datalakesettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-lakeformation-datalakesettings-syntax.json"></a>

```
{
  "Type" : "AWS::LakeFormation::DataLakeSettings",
  "Properties" : {
      "[Admins](#cfn-lakeformation-datalakesettings-admins)" : [Admins](aws-properties-lakeformation-datalakesettings-admins.md)
    }
}
```

### YAML<a name="aws-resource-lakeformation-datalakesettings-syntax.yaml"></a>

```
Type: AWS::LakeFormation::DataLakeSettings
Properties: 
  [Admins](#cfn-lakeformation-datalakesettings-admins): 
    [Admins](aws-properties-lakeformation-datalakesettings-admins.md)
```

## Properties<a name="aws-resource-lakeformation-datalakesettings-properties"></a>

`Admins`  <a name="cfn-lakeformation-datalakesettings-admins"></a>
A list of AWS Lake Formation principals\.  
*Required*: No  
*Type*: [Admins](aws-properties-lakeformation-datalakesettings-admins.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-lakeformation-datalakesettings-return-values"></a>

### Ref<a name="aws-resource-lakeformation-datalakesettings-return-values-ref"></a>

## Supported Regions

This ResourceType is supported by the following regions:

- `ap-northeast-1`
- `eu-west-1`
- `us-east-1`
- `us-east-2`
- `us-west-2`
