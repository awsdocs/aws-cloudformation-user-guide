# AWS::SecretsManager::Secret GenerateSecretString<a name="aws-properties-secretsmanager-secret-generatesecretstring"></a>

Generates a random password\. We recommend that you specify the maximum length and include every character type that the system you are generating a password for can support\.

 **Required permissions: ** `secretsmanager:GetRandomPassword`\. For more information, see [ IAM policy actions for Secrets Manager](https://docs.aws.amazon.com/service-authorization/latest/reference/list_awssecretsmanager.html#awssecretsmanager-actions-as-permissions) and [Authentication and access control in Secrets Manager](https://docs.aws.amazon.com/secretsmanager/latest/userguide/auth-and-access.html)\. 

## Syntax<a name="aws-properties-secretsmanager-secret-generatesecretstring-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-secretsmanager-secret-generatesecretstring-syntax.json"></a>

```
{
  "[ExcludeCharacters](#cfn-secretsmanager-secret-generatesecretstring-excludecharacters)" : String,
  "[ExcludeLowercase](#cfn-secretsmanager-secret-generatesecretstring-excludelowercase)" : Boolean,
  "[ExcludeNumbers](#cfn-secretsmanager-secret-generatesecretstring-excludenumbers)" : Boolean,
  "[ExcludePunctuation](#cfn-secretsmanager-secret-generatesecretstring-excludepunctuation)" : Boolean,
  "[ExcludeUppercase](#cfn-secretsmanager-secret-generatesecretstring-excludeuppercase)" : Boolean,
  "[GenerateStringKey](#cfn-secretsmanager-secret-generatesecretstring-generatestringkey)" : String,
  "[IncludeSpace](#cfn-secretsmanager-secret-generatesecretstring-includespace)" : Boolean,
  "[PasswordLength](#cfn-secretsmanager-secret-generatesecretstring-passwordlength)" : Integer,
  "[RequireEachIncludedType](#cfn-secretsmanager-secret-generatesecretstring-requireeachincludedtype)" : Boolean,
  "[SecretStringTemplate](#cfn-secretsmanager-secret-generatesecretstring-secretstringtemplate)" : String
}
```

### YAML<a name="aws-properties-secretsmanager-secret-generatesecretstring-syntax.yaml"></a>

```
  [ExcludeCharacters](#cfn-secretsmanager-secret-generatesecretstring-excludecharacters): String
  [ExcludeLowercase](#cfn-secretsmanager-secret-generatesecretstring-excludelowercase): Boolean
  [ExcludeNumbers](#cfn-secretsmanager-secret-generatesecretstring-excludenumbers): Boolean
  [ExcludePunctuation](#cfn-secretsmanager-secret-generatesecretstring-excludepunctuation): Boolean
  [ExcludeUppercase](#cfn-secretsmanager-secret-generatesecretstring-excludeuppercase): Boolean
  [GenerateStringKey](#cfn-secretsmanager-secret-generatesecretstring-generatestringkey): 
    String
  [IncludeSpace](#cfn-secretsmanager-secret-generatesecretstring-includespace): Boolean
  [PasswordLength](#cfn-secretsmanager-secret-generatesecretstring-passwordlength): Integer
  [RequireEachIncludedType](#cfn-secretsmanager-secret-generatesecretstring-requireeachincludedtype): Boolean
  [SecretStringTemplate](#cfn-secretsmanager-secret-generatesecretstring-secretstringtemplate): 
    String
```

## Properties<a name="aws-properties-secretsmanager-secret-generatesecretstring-properties"></a>

`ExcludeCharacters`  <a name="cfn-secretsmanager-secret-generatesecretstring-excludecharacters"></a>
A string of the characters that you don't want in the password\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExcludeLowercase`  <a name="cfn-secretsmanager-secret-generatesecretstring-excludelowercase"></a>
Specifies whether to exclude lowercase letters from the password\. If you don't include this switch, the password can contain lowercase letters\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExcludeNumbers`  <a name="cfn-secretsmanager-secret-generatesecretstring-excludenumbers"></a>
Specifies whether to exclude numbers from the password\. If you don't include this switch, the password can contain numbers\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExcludePunctuation`  <a name="cfn-secretsmanager-secret-generatesecretstring-excludepunctuation"></a>
Specifies whether to exclude the following punctuation characters from the password: `! " # $ % & ' ( ) * + , - . / : ; < = > ? @ [ \ ] ^ _ ` { | } ~`\. If you don't include this switch, the password can contain punctuation\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExcludeUppercase`  <a name="cfn-secretsmanager-secret-generatesecretstring-excludeuppercase"></a>
Specifies whether to exclude uppercase letters from the password\. If you don't include this switch, the password can contain uppercase letters\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GenerateStringKey`  <a name="cfn-secretsmanager-secret-generatesecretstring-generatestringkey"></a>
The JSON key name for the key/value pair, where the value is the generated password\. This pair is added to the JSON structure specified by the `SecretStringTemplate` parameter\. If you specify this parameter, then you must also specify `SecretStringTemplate`\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludeSpace`  <a name="cfn-secretsmanager-secret-generatesecretstring-includespace"></a>
Specifies whether to include the space character\. If you include this switch, the password can contain space characters\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PasswordLength`  <a name="cfn-secretsmanager-secret-generatesecretstring-passwordlength"></a>
The length of the password\. If you don't include this parameter, the default length is 32 characters\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RequireEachIncludedType`  <a name="cfn-secretsmanager-secret-generatesecretstring-requireeachincludedtype"></a>
Specifies whether to include at least one upper and lowercase letter, one number, and one punctuation\. If you don't include this switch, the password contains at least one of every character type\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretStringTemplate`  <a name="cfn-secretsmanager-secret-generatesecretstring-secretstringtemplate"></a>
A template that the generated string must match\. When you make a change to this property, a new secret version is created\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-secretsmanager-secret-generatesecretstring--seealso"></a>
+  [GetRandomPassword](https://docs.aws.amazon.com/secretsmanager/latest/apireference/API_GetRandomPassword.html) in the AWS Secrets Manager API Reference