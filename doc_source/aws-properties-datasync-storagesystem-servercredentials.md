# AWS::DataSync::StorageSystem ServerCredentials<a name="aws-properties-datasync-storagesystem-servercredentials"></a>

The credentials that provide DataSync Discovery read access to your on\-premises storage system's management interface\.

DataSync Discovery stores these credentials in [AWS Secrets Manager](https://docs.aws.amazon.com/secretsmanager/latest/userguide/intro.html)\. For more information, see [Accessing your on\-premises storage system](https://docs.aws.amazon.com/datasync/latest/userguide/discovery-configure-storage.html)\.

## Syntax<a name="aws-properties-datasync-storagesystem-servercredentials-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-datasync-storagesystem-servercredentials-syntax.json"></a>

```
{
  "[Password](#cfn-datasync-storagesystem-servercredentials-password)" : String,
  "[Username](#cfn-datasync-storagesystem-servercredentials-username)" : String
}
```

### YAML<a name="aws-properties-datasync-storagesystem-servercredentials-syntax.yaml"></a>

```
  [Password](#cfn-datasync-storagesystem-servercredentials-password): String
  [Username](#cfn-datasync-storagesystem-servercredentials-username): String
```

## Properties<a name="aws-properties-datasync-storagesystem-servercredentials-properties"></a>

`Password`  <a name="cfn-datasync-storagesystem-servercredentials-password"></a>
Specifies the password for your storage system's management interface\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `1024`  
*Pattern*: `^(?!.*[:\"][^:"]*$).+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Username`  <a name="cfn-datasync-storagesystem-servercredentials-username"></a>
Specifies the user name for your storage system's management interface\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `1024`  
*Pattern*: `^(?!.*[:\"][^:"]*$).+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)