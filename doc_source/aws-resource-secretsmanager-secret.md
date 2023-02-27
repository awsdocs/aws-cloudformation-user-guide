# AWS::SecretsManager::Secret<a name="aws-resource-secretsmanager-secret"></a>

Creates a new secret\. A *secret* can be a password, a set of credentials such as a user name and password, an OAuth token, or other secret information that you store in an encrypted form in Secrets Manager\.

For Amazon RDS master user credentials, see [AWS::RDS::DBCluster MasterUserSecret](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-dbcluster-masterusersecret.html)\.

To retrieve a secret in a CloudFormation template, use a *dynamic reference*\. For more information, see [ Retrieve a secret in an AWS CloudFormation resource](https://docs.aws.amazon.com/secretsmanager/latest/userguide/cfn-example_reference-secret.html)\.

A common scenario is to first create a secret with `GenerateSecretString`, which generates a password, and then use a dynamic reference to retrieve the username and password from the secret to use as credentials for a new database\. Follow these steps, as shown in the examples below:

1. Define the secret without referencing the service or database\. You can't reference the service or database because it doesn't exist yet\. The secret must contain a username and password\.

1. Next, define the service or database\. Include the reference to the secret to use stored credentials to define the database admin user and password\.

1. Finally, define a `SecretTargetAttachment` resource type to finish configuring the secret with the required database engine type and the connection details of the service or database\. The rotation function requires the details, if you attach one later by defining a [AWS::SecretsManager::RotationSchedule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-rotationschedule.html) resource type\.

For information about creating a secret in the console, see [Create a secret](https://docs.aws.amazon.com/secretsmanager/latest/userguide/manage_create-basic-secret.html)\. For information about creating a secret using the CLI or SDK, see [CreateSecret](https://docs.aws.amazon.com/secretsmanager/latest/apireference/API_CreateSecret.html)\.

For information about retrieving a secret in code, see [Retrieve secrets from Secrets Manager](https://docs.aws.amazon.com/secretsmanager/latest/userguide/retrieving-secrets.html)\.

**Note**  
Do not create a dynamic reference using a backslash `(\)` as the final value\. AWS CloudFormation cannot resolve those references, which causes a resource failure\. 

## Syntax<a name="aws-resource-secretsmanager-secret-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-secretsmanager-secret-syntax.json"></a>

```
{
  "Type" : "AWS::SecretsManager::Secret",
  "Properties" : {
      "[Description](#cfn-secretsmanager-secret-description)" : String,
      "[GenerateSecretString](#cfn-secretsmanager-secret-generatesecretstring)" : GenerateSecretString,
      "[KmsKeyId](#cfn-secretsmanager-secret-kmskeyid)" : String,
      "[Name](#cfn-secretsmanager-secret-name)" : String,
      "[ReplicaRegions](#cfn-secretsmanager-secret-replicaregions)" : [ ReplicaRegion, ... ],
      "[SecretString](#cfn-secretsmanager-secret-secretstring)" : String,
      "[Tags](#cfn-secretsmanager-secret-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-secretsmanager-secret-syntax.yaml"></a>

```
Type: AWS::SecretsManager::Secret
Properties: 
  [Description](#cfn-secretsmanager-secret-description): String
  [GenerateSecretString](#cfn-secretsmanager-secret-generatesecretstring): 
    GenerateSecretString
  [KmsKeyId](#cfn-secretsmanager-secret-kmskeyid): String
  [Name](#cfn-secretsmanager-secret-name): String
  [ReplicaRegions](#cfn-secretsmanager-secret-replicaregions): 
    - ReplicaRegion
  [SecretString](#cfn-secretsmanager-secret-secretstring): 
    String
  [Tags](#cfn-secretsmanager-secret-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-secretsmanager-secret-properties"></a>

`Description`  <a name="cfn-secretsmanager-secret-description"></a>
The description of the secret\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GenerateSecretString`  <a name="cfn-secretsmanager-secret-generatesecretstring"></a>
A structure that specifies how to generate a password to encrypt and store in the secret\. To include a specific string in the secret, use `SecretString` instead\. If you omit both `GenerateSecretString` and `SecretString`, you create an empty secret\. When you make a change to this property, a new secret version is created\.  
We recommend that you specify the maximum length and include every character type that the system you are generating a password for can support\.  
*Required*: No  
*Type*: [GenerateSecretString](aws-properties-secretsmanager-secret-generatesecretstring.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KmsKeyId`  <a name="cfn-secretsmanager-secret-kmskeyid"></a>
The ARN, key ID, or alias of the AWS KMS key that Secrets Manager uses to encrypt the secret value in the secret\. An alias is always prefixed by `alias/`, for example `alias/aws/secretsmanager`\. For more information, see [About aliases](https://docs.aws.amazon.com/kms/latest/developerguide/alias-about.html)\.  
To use a AWS KMS key in a different account, use the key ARN or the alias ARN\.  
If you don't specify this value, then Secrets Manager uses the key `aws/secretsmanager`\. If that key doesn't yet exist, then Secrets Manager creates it for you automatically the first time it encrypts the secret value\.  
If the secret is in a different AWS account from the credentials calling the API, then you can't use `aws/secretsmanager` to encrypt the secret, and you must create and use a customer managed AWS KMS key\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-secretsmanager-secret-name"></a>
The name of the new secret\.  
The secret name can contain ASCII letters, numbers, and the following characters: /\_\+=\.@\-  
Do not end your secret name with a hyphen followed by six characters\. If you do so, you risk confusion and unexpected results when searching for a secret by partial ARN\. Secrets Manager automatically adds a hyphen and six random characters after the secret name at the end of the ARN\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ReplicaRegions`  <a name="cfn-secretsmanager-secret-replicaregions"></a>
A custom type that specifies a `Region` and the `KmsKeyId` for a replica secret\.  
*Required*: No  
*Type*: List of [ReplicaRegion](aws-properties-secretsmanager-secret-replicaregion.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretString`  <a name="cfn-secretsmanager-secret-secretstring"></a>
The text to encrypt and store in the secret\. We recommend you use a JSON structure of key/value pairs for your secret value\. To generate a random password, use `GenerateSecretString` instead\. If you omit both `GenerateSecretString` and `SecretString`, you create an empty secret\. When you make a change to this property, a new secret version is created\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-secretsmanager-secret-tags"></a>
A list of tags to attach to the secret\. Each tag is a key and value pair of strings in a JSON text string, for example:  
 `[{"Key":"CostCenter","Value":"12345"},{"Key":"environment","Value":"production"}]`   
Secrets Manager tag key names are case sensitive\. A tag with the key "ABC" is a different tag from one with key "abc"\.  
If you check tags in permissions policies as part of your security strategy, then adding or removing a tag can change permissions\. If the completion of this operation would result in you losing your permissions for this secret, then Secrets Manager blocks the operation and returns an `Access Denied` error\. For more information, see [Control access to secrets using tags](https://docs.aws.amazon.com/secretsmanager/latest/userguide/auth-and-access_examples.html#tag-secrets-abac) and [Limit access to identities with tags that match secrets' tags](https://docs.aws.amazon.com/secretsmanager/latest/userguide/auth-and-access_examples.html#auth-and-access_tags2)\.  
For information about how to format a JSON parameter for the various command line tool environments, see [Using JSON for Parameters](https://docs.aws.amazon.com/cli/latest/userguide/cli-using-param.html#cli-using-param-json)\. If your command\-line tool or SDK requires quotation marks around the parameter, you should use single quotes to avoid confusion with the double quotes required in the JSON text\.  
The following restrictions apply to tags:  
+ Maximum number of tags per secret: 50
+ Maximum key length: 127 Unicode characters in UTF\-8
+ Maximum value length: 255 Unicode characters in UTF\-8
+ Tag keys and values are case sensitive\.
+ Do not use the `aws:` prefix in your tag names or values because AWS reserves it for AWS use\. You can't edit or delete tag names or values with this prefix\. Tags with this prefix do not count against your tags per secret limit\.
+ If you use your tagging schema across multiple services and resources, other services might have restrictions on allowed characters\. Generally allowed characters: letters, spaces, and numbers representable in UTF\-8, plus the following special characters: \+ \- = \. \_ : / @\.
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-secretsmanager-secret-return-values"></a>

### Ref<a name="aws-resource-secretsmanager-secret-return-values-ref"></a>

When you pass the logical ID of an `AWS::SecretsManager::Secret` resource to the intrinsic `Ref` function, the function returns the ARN of the secret configured such as:

`arn:aws:secretsmanager:us-west-2:123456789012:secret:my-path/my-secret-name-1a2b3c`

If you know the ARN of a secret, you can reference a secret you created in one part of the stack template from within the definition of another resource in the same template\. You typically use the `Ref` function with the [AWS::SecretsManager::SecretTargetAttachment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-secrettargetattachment.html) resource type to get references to both the secret and its associated database\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\. 

## Examples<a name="aws-resource-secretsmanager-secret--examples"></a>



### Creating a secret with a dynamically generated password<a name="aws-resource-secretsmanager-secret--examples--Creating_a_secret_with_a_dynamically_generated_password"></a>

The following example creates a secret, constructing the secret value from a string template combined with a dynamically generated random password\. The result of this example is a `SecretString` value that looks like the following:

`{"username": "test-user", "password": "rzDtILsQNfmmHwkJBPsTVhkRvWRtSn" }`

#### JSON<a name="aws-resource-secretsmanager-secret--examples--Creating_a_secret_with_a_dynamically_generated_password--json"></a>

```
{
  "MySecretA": {
    "Type": "AWS::SecretsManager::Secret",
    "Properties": {
      "Name": "MySecretForAppA",
      "Description": "This secret has a dynamically generated secret password.",
      "GenerateSecretString": {
        "SecretStringTemplate": "{\"username\":\"test-user\"}",
        "GenerateStringKey": "password",
        "PasswordLength": 30,
        "ExcludeCharacters": "\"@/\\"
      },
      "Tags": [
        {
          "Key": "AppName",
          "Value": "AppA"
        }
      ]
    }
  }
}
```

#### YAML<a name="aws-resource-secretsmanager-secret--examples--Creating_a_secret_with_a_dynamically_generated_password--yaml"></a>

```
#This is a Secret resource with a randomly generated password in its SecretString JSON.
MySecretA:
  Type: 'AWS::SecretsManager::Secret'
  Properties:
    Name: MySecretForAppA
    Description: "This secret has a dynamically generated secret password."
    GenerateSecretString:
      SecretStringTemplate: '{"username": "test-user"}'
      GenerateStringKey: "password"
      PasswordLength: 30
      ExcludeCharacters: '"@/\'
    Tags:
      -
        Key: AppName
        Value: AppA
```

### Creating a secret with a hardcoded password<a name="aws-resource-secretsmanager-secret--examples--Creating_a_secret_with_a_hardcoded_password"></a>

The following example creates a secret and provides the secret value as a literal string stored in the secret\. We recommend that you don't hardcode your password this way\. Instead use the [SecretsManager Secret GenerateSecretString](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-secretsmanager-secret-generatesecretstring.html) property\. See the previous example for the recommended option\.

#### JSON<a name="aws-resource-secretsmanager-secret--examples--Creating_a_secret_with_a_hardcoded_password--json"></a>

```
{
  "MySecretB": {
    "Type": "AWS::SecretsManager::Secret",
    "Properties": {
      "Name": "MySecretForAppB",
      "Description": "This secret has a hardcoded password in SecretString (use GenerateSecretString instead)",
      "SecretString": "{\"username\":\"MasterUsername\",\"password\":\"secret-password\"}",
      "Tags": [
        {
          "Key": "AppName",
          "Value": "AppB"
        }
      ]
    }
  }
}
```

#### YAML<a name="aws-resource-secretsmanager-secret--examples--Creating_a_secret_with_a_hardcoded_password--yaml"></a>

```
  # This is another secret that has its password hardcoded into the template (NOT RECOMMENDED)
  MySecretB:
    Type: 'AWS::SecretsManager::Secret'
    Properties:
      Name: MySecretForAppB
      Description: This secret has a hardcoded password in SecretString (use GenerateSecretString instead)
      SecretString: '{"username":"MasterUsername","password":"secret-password"}'
      Tags:
        -
          Key: AppName
          Value: AppB
```

### Replicating a secret<a name="aws-resource-secretsmanager-secret--examples--Replicating_a_secret"></a>

The following example replicates a primary secret to `us-east-1` and `us-east-2`\.

#### JSON<a name="aws-resource-secretsmanager-secret--examples--Replicating_a_secret--json"></a>

```
{
   "MyReplicatedSecret":{
      "Type":"AWS::SecretsManager::Secret",
      "Properties":{
         "Name":"MyReplicatedSecret",
         "Description":"This secret is replicated to
        two regions. One with a customer managed key, and one with the AWS managed key for Secrets Manager aws/secretsmanager.",
         "ReplicaRegions":[
            {
               "Region":"us-east-1",
               "KmsKeyId":"alias/exampleAlias"
            },
            {
               "Region":"us-east-2"
            }
         ]
      }
   }
}
```

#### YAML<a name="aws-resource-secretsmanager-secret--examples--Replicating_a_secret--yaml"></a>

```
#This is a Secret resource which is replicated to two other regions.
MyReplicatedSecret:
  Type: AWS::SecretsManager::Secret
  Properties:
    Name: MyReplicatedSecret
    Description: 'This secret is replicated to
    two regions. One with a customer managed key, and one with the AWS managed key for Secrets Manager aws/secretsmanager.'
    ReplicaRegions:
    - Region: us-east-1
      KmsKeyId: alias/exampleAlias
    - Region: us-east-2
```

## See also<a name="aws-resource-secretsmanager-secret--seealso"></a>
+  [CreateSecret](https://docs.aws.amazon.com/secretsmanager/latest/apireference/API_CreateSecret.html) in the AWS Secrets Manager API Reference
+  [Create and manage secrets](https://docs.aws.amazon.com/secretsmanager/latest/userguide/managing-secrets.html) in the AWS Secrets Manager User Guide 
+  [AWS::SecretsManager::ResourcePolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-resourcepolicy.html)
+  [AWS::SecretsManager::RotationSchedule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-rotationschedule.html)
+  [AWS::SecretsManager::SecretReplicaRegion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-secretsmanager-secret-replicaregion.html) 
+  [AWS::SecretsManager::SecretTargetAttachment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-secrettargetattachment.html)