# AWS::SystemsManagerSAP::Application Credential<a name="aws-properties-systemsmanagersap-application-credential"></a>

The credentials of your SAP application\.

## Syntax<a name="aws-properties-systemsmanagersap-application-credential-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-systemsmanagersap-application-credential-syntax.json"></a>

```
{
  "[CredentialType](#cfn-systemsmanagersap-application-credential-credentialtype)" : String,
  "[DatabaseName](#cfn-systemsmanagersap-application-credential-databasename)" : String,
  "[SecretId](#cfn-systemsmanagersap-application-credential-secretid)" : String
}
```

### YAML<a name="aws-properties-systemsmanagersap-application-credential-syntax.yaml"></a>

```
  [CredentialType](#cfn-systemsmanagersap-application-credential-credentialtype): String
  [DatabaseName](#cfn-systemsmanagersap-application-credential-databasename): String
  [SecretId](#cfn-systemsmanagersap-application-credential-secretid): String
```

## Properties<a name="aws-properties-systemsmanagersap-application-credential-properties"></a>

`CredentialType`  <a name="cfn-systemsmanagersap-application-credential-credentialtype"></a>
The type of the application credentials\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DatabaseName`  <a name="cfn-systemsmanagersap-application-credential-databasename"></a>
The name of the SAP HANA database\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SecretId`  <a name="cfn-systemsmanagersap-application-credential-secretid"></a>
The secret ID created in AWS Secrets Manager to store the credentials of the SAP application\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)