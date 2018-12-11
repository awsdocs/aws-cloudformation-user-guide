# Secrets Manager Secret GenerateSecretString<a name="aws-properties-secretsmanager-secret-generatesecretstring"></a>

<a name="aws-properties-secretsmanager-secret-generatesecretstring-description"></a>You can use the `GenerateSecretString` property as part of the [AWS::SecretsManager::Secret](aws-resource-secretsmanager-secret.md) resource type to dynamically generate a random text string to use as a password\. It is an alternative to 'hardcoding' a password directly in the `SecretString` property\. When you generate a [AWS::SecretsManager::Secret](aws-resource-secretsmanager-secret.md) resource type, you must include one or the other, but not both\. 

`SecretString` enables you to place a *literal* value directly into the secret \(a technique that we recommend that you avoid\)\. Instead, we recommend that you use the `GenerateSecretString` property to dynamically generate a random password\. The operation returns a complete JSON structure to use as the secret value\. The structure begins with the string that you supply using `SecretStringTemplate`\. This template string must be a properly formatted JSON string that contains all of the secret value information *except* the password\. The operation then generates a random password using the rules specified by the other parameters\. Finally, the operation inserts the generated password into the secret value structure along with the JSON key name that's specified by the `GenerateStringKey` parameter\.

For examples, see [AWS::SecretsManager::Secret](aws-resource-secretsmanager-secret.md)\.

<a name="aws-properties-secretsmanager-secret-generatesecretstring-inheritance"></a> `GenerateSecretString` is a property of the [AWS::SecretsManager::Secret](aws-resource-secretsmanager-secret.md) resource\.

## Syntax<a name="aws-properties-secretsmanager-secret-generatesecretstring-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-secretsmanager-secret-generatesecretstring-syntax.json"></a>

```
{
  "[ExcludeUppercase](#cfn-secretsmanager-secret-generatesecretstring-excludeuppercase)" : Boolean,
  "[RequireEachIncludedType](#cfn-secretsmanager-secret-generatesecretstring-requireeachincludedtype)" : Boolean,
  "[IncludeSpace](#cfn-secretsmanager-secret-generatesecretstring-includespace)" : Boolean,
  "[ExcludeCharacters](#cfn-secretsmanager-secret-generatesecretstring-excludecharacters)" : String,
  "[GenerateStringKey](#cfn-secretsmanager-secret-generatesecretstring-generatestringkey)" : String,
  "[PasswordLength](#cfn-secretsmanager-secret-generatesecretstring-passwordlength)" : Integer,
  "[ExcludePunctuation](#cfn-secretsmanager-secret-generatesecretstring-excludepunctuation)" : Boolean,
  "[ExcludeLowercase](#cfn-secretsmanager-secret-generatesecretstring-excludelowercase)" : Boolean,
  "[SecretStringTemplate](#cfn-secretsmanager-secret-generatesecretstring-secretstringtemplate)" : String,
  "[ExcludeNumbers](#cfn-secretsmanager-secret-generatesecretstring-excludenumbers)" : Boolean
}
```

### YAML<a name="aws-properties-secretsmanager-secret-generatesecretstring-syntax.yaml"></a>

```
[ExcludeUppercase](#cfn-secretsmanager-secret-generatesecretstring-excludeuppercase): Boolean
[RequireEachIncludedType](#cfn-secretsmanager-secret-generatesecretstring-requireeachincludedtype): Boolean
[IncludeSpace](#cfn-secretsmanager-secret-generatesecretstring-includespace): Boolean
[ExcludeCharacters](#cfn-secretsmanager-secret-generatesecretstring-excludecharacters): String
[GenerateStringKey](#cfn-secretsmanager-secret-generatesecretstring-generatestringkey): String
[PasswordLength](#cfn-secretsmanager-secret-generatesecretstring-passwordlength): Integer
[ExcludePunctuation](#cfn-secretsmanager-secret-generatesecretstring-excludepunctuation): Boolean
[ExcludeLowercase](#cfn-secretsmanager-secret-generatesecretstring-excludelowercase): Boolean
[SecretStringTemplate](#cfn-secretsmanager-secret-generatesecretstring-secretstringtemplate): String
[ExcludeNumbers](#cfn-secretsmanager-secret-generatesecretstring-excludenumbers): Boolean
```

## Properties<a name="aws-properties-secretsmanager-secret-generatesecretstring-properties"></a>

`ExcludeUppercase`  <a name="cfn-secretsmanager-secret-generatesecretstring-excludeuppercase"></a>
Specifies that the generated password shouldn't include uppercase letters\. The default if you don't include this switch parameter is `False`, and the generated password can include uppercase letters\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`RequireEachIncludedType`  <a name="cfn-secretsmanager-secret-generatesecretstring-requireeachincludedtype"></a>
Specifies whether the generated password must include at least one of every allowed character type\. The default if you don't include this switch is True, and the generated password includes at least one of every character type\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`IncludeSpace`  <a name="cfn-secretsmanager-secret-generatesecretstring-includespace"></a>
Specifies that the generated password can include the space character\. The default if you don't include this switch parameter is False, and the generated password doesn't include any space characters\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ExcludeCharacters`  <a name="cfn-secretsmanager-secret-generatesecretstring-excludecharacters"></a>
A string that includes characters that shouldn't be included in the generated password\. The default if you don't include this parameter is that all characters from the included sets are candidates for inclusion in the generated password\. The string can be a minimum length of 0 characters and a maximum length of 4096 characters\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`GenerateStringKey`  <a name="cfn-secretsmanager-secret-generatesecretstring-generatestringkey"></a>
The JSON key name that's used to add the generated password to the JSON structure specified by the `SecretStringTemplate` parameter\. If you specify this parameter, then you must also specify `SecretStringTemplate`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`PasswordLength`  <a name="cfn-secretsmanager-secret-generatesecretstring-passwordlength"></a>
The desired length of the generated password\. The default value if you don't include this parameter is 32 characters\.  
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ExcludePunctuation`  <a name="cfn-secretsmanager-secret-generatesecretstring-excludepunctuation"></a>
Specifies that the generated password shouldn't include punctuation characters\. The default if you don't include this switch parameter is `False`, and the generated password can include punctuation characters\.  
The following are the punctuation characters that can be included in the generated password if you don't explicitly exclude them with `ExcludeCharacters` or `ExcludePunctuation`:  
` ! " # $ % & ' ( ) * + , - . / : ; < = > ? @ [ \ ] ^ _ ` { | } ~`  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ExcludeLowercase`  <a name="cfn-secretsmanager-secret-generatesecretstring-excludelowercase"></a>
Specifies that the generated password shouldn't include lowercase letters\. The default if you don't include this switch parameter is `False`, and the generated password can include lowercase letters\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`SecretStringTemplate`  <a name="cfn-secretsmanager-secret-generatesecretstring-secretstringtemplate"></a>
A properly structured JSON string that the generated password can be added to\. If you specify this parameter, then you must also specify `GenerateStringKey`\. That key is combined with the generated random string and inserted into the JSON structure that's specified by this parameter\. The merged JSON string is returned as the completed `SecretString` of the secret\. The default if you don't include this parameter is that the generated random password string is returned by itself, and isn't embedded in a JSON structure\.   
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ExcludeNumbers`  <a name="cfn-secretsmanager-secret-generatesecretstring-excludenumbers"></a>
Specifies that the generated password shouldn't include digits\. The default if you don't include this switch parameter is `False`, and the generated password can include digits\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-secretsmanager-secret-generatesecretstring-seealso"></a>
+ [GetRandomPassword](https://docs.aws.amazon.com/secretsmanager/latest/apireference/API_GetRandomPassword.html) in the *AWS Secrets Manager API Reference*