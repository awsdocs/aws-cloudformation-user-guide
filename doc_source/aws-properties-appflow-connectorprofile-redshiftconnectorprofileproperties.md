# AWS::AppFlow::ConnectorProfile RedshiftConnectorProfileProperties<a name="aws-properties-appflow-connectorprofile-redshiftconnectorprofileproperties"></a>

 The `RedshiftConnectorProfileProperties` property type specifies the connector\-specific profile properties when using Amazon Redshift\. 

## Syntax<a name="aws-properties-appflow-connectorprofile-redshiftconnectorprofileproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-connectorprofile-redshiftconnectorprofileproperties-syntax.json"></a>

```
{
  "[BucketName](#cfn-appflow-connectorprofile-redshiftconnectorprofileproperties-bucketname)" : String,
  "[BucketPrefix](#cfn-appflow-connectorprofile-redshiftconnectorprofileproperties-bucketprefix)" : String,
  "[DatabaseUrl](#cfn-appflow-connectorprofile-redshiftconnectorprofileproperties-databaseurl)" : String,
  "[RoleArn](#cfn-appflow-connectorprofile-redshiftconnectorprofileproperties-rolearn)" : String
}
```

### YAML<a name="aws-properties-appflow-connectorprofile-redshiftconnectorprofileproperties-syntax.yaml"></a>

```
  [BucketName](#cfn-appflow-connectorprofile-redshiftconnectorprofileproperties-bucketname): String
  [BucketPrefix](#cfn-appflow-connectorprofile-redshiftconnectorprofileproperties-bucketprefix): String
  [DatabaseUrl](#cfn-appflow-connectorprofile-redshiftconnectorprofileproperties-databaseurl): String
  [RoleArn](#cfn-appflow-connectorprofile-redshiftconnectorprofileproperties-rolearn): String
```

## Properties<a name="aws-properties-appflow-connectorprofile-redshiftconnectorprofileproperties-properties"></a>

`BucketName`  <a name="cfn-appflow-connectorprofile-redshiftconnectorprofileproperties-bucketname"></a>
 A name for the associated Amazon S3 bucket\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `63`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BucketPrefix`  <a name="cfn-appflow-connectorprofile-redshiftconnectorprofileproperties-bucketprefix"></a>
 The object key for the destination bucket in which Amazon AppFlow places the files\.   
*Required*: No  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DatabaseUrl`  <a name="cfn-appflow-connectorprofile-redshiftconnectorprofileproperties-databaseurl"></a>
 The JDBC URL of the Amazon Redshift cluster\.   
*Required*: Yes  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-appflow-connectorprofile-redshiftconnectorprofileproperties-rolearn"></a>
 The Amazon Resource Name \(ARN\) of the IAM role\.   
*Required*: Yes  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `arn:aws:iam:.*:[0-9]+:.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-appflow-connectorprofile-redshiftconnectorprofileproperties--seealso"></a>
+ [RedshiftConnectorProfileProperties](https://docs.aws.amazon.com/appflow/1.0/APIReference/API_RedshiftConnectorProfileProperties.html) in the *Amazon AppFlow API Reference*\.

