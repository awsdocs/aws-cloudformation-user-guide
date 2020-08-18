# AWS::SecretsManager::Secret GenerateSecretString<a name="aws-properties-secretsmanager-secret-generatesecretstring"></a>

Use the `GenerateSecretString` property as part of the [AWS::SecretsManager::Secret](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-secret.html) resource type to dynamically generate a random text string to use as a password\. You use this an alternative to hardcoding a password directly in the `SecretString` property\. When you generate a [AWS::SecretsManager::Secret](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-secret.html) resource type, you must include one or the other, but not both\.

`SecretString` enables you to place a literal value directly into the secret, an action not recommended\. Instead, we recommend that you use the `GenerateSecretString` property to dynamically generate a random password\. The operation returns a complete JSON structure to use as the secret value\. The structure begins with the string you supply using the `SecretStringTemplate`\. This template string must be a properly formatted JSON string that contains all of the secret value information except the password\. The operation then generates a random password using the rules specified by the other parameters\. Finally, the operations inserts the generated password into the secret value structure along with the JSON key name specified by the `GenerateStringKey` parameter\.

For examples, see [AWS::SecretsManager::Secret](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-secret.html)\. 

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
A string that excludes characters in the generated password\. By default, all characters from the included sets can be used\. The string can be a minimum length of 0 characters and a maximum length of 7168 characters\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `4096`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExcludeLowercase`  <a name="cfn-secretsmanager-secret-generatesecretstring-excludelowercase"></a>
Specifies the generated password should not include lowercase letters\. By default, SEcrets Manager disables this parameter, and the generated password can include lowercase `False`, and the generated password can include lowercase letters\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExcludeNumbers`  <a name="cfn-secretsmanager-secret-generatesecretstring-excludenumbers"></a>
Specifies that the generated password should exclude digits\. By default, Secrets Manager does not enable the parameter, `False`, and the generated password can include digits\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExcludePunctuation`  <a name="cfn-secretsmanager-secret-generatesecretstring-excludepunctuation"></a>
Specifies that the generated password should not include punctuation characters\. The default if you do not include this switch parameter is that punctuation characters can be included\.  
The following are the punctuation characters that *can* be included in the generated password if you don't explicitly exclude them with `ExcludeCharacters` or `ExcludePunctuation`:  
 `! " # $ % & ' ( ) * + , - . / : ; < = > ? @ [ \ ] ^ _ ` { | } ~`   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExcludeUppercase`  <a name="cfn-secretsmanager-secret-generatesecretstring-excludeuppercase"></a>
Specifies that the generated password should not include uppercase letters\. The default behavior is `False`, and the generated password can include uppercase letters\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GenerateStringKey`  <a name="cfn-secretsmanager-secret-generatesecretstring-generatestringkey"></a>
The JSON key name used to add the generated password to the JSON structure specified by the `SecretStringTemplate` parameter\. If you specify this parameter, then you must also specify `SecretStringTemplate`\.   
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `65536`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludeSpace`  <a name="cfn-secretsmanager-secret-generatesecretstring-includespace"></a>
Specifies that the generated password can include the space character\. By default, Secrets Manager disables this parameter, and the generated password doesn't include space   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PasswordLength`  <a name="cfn-secretsmanager-secret-generatesecretstring-passwordlength"></a>
The desired length of the generated password\. The default value if you do not include this parameter is 32 characters\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RequireEachIncludedType`  <a name="cfn-secretsmanager-secret-generatesecretstring-requireeachincludedtype"></a>
Specifies whether the generated password must include at least one of every allowed character type\. By default, Secrets Manager enables this parameter, and the generated password includes at least one of every character type\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretStringTemplate`  <a name="cfn-secretsmanager-secret-generatesecretstring-secretstringtemplate"></a>
A properly structured JSON string that the generated password can be added to\. If you specify this parameter, then you must also specify `GenerateStringKey`\. Secrets Manager combines this with the generated random string and inserts into the JSON structure specified by this parameter\. The merged JSON string returns as the completed `SecretString` of the secret\. By default, Secrets Manager does not return the generated random password string, and doesn't embed it in a JSON structure\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `65536`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-secretsmanager-secret-generatesecretstring--seealso"></a>
+  [GetRandomPassword](https://docs.aws.amazon.com/secretsmanager/latest/apireference/API_GetRandomPassword.html) API in the AWS Secrets Manager API Reference