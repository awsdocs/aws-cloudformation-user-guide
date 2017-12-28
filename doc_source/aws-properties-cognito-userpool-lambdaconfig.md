# Amazon Cognito UserPool LambdaConfig<a name="aws-properties-cognito-userpool-lambdaconfig"></a>

`LambdaConfig` is a property of the [AWS::Cognito::UserPool](aws-resource-cognito-userpool.md) resource that defines the AWS Lambda configuration of an Amazon Cognito User Pool\.

## Syntax<a name="aws-properties-cognito-userpool-lambdaconfig-syntax"></a>

### JSON<a name="aws-properties-cognito-userpool-lambdaconfig-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-lambdaconfig-createauthchallenge)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-lambdaconfig-custommessage)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-lambdaconfig-defineauthchallenge)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-lambdaconfig-postauthentication)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-lambdaconfig-postconfirmation)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-lambdaconfig-preauthentication)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-lambdaconfig-presignup)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-lambdaconfig-verifyauthchallengeresponse)" : String
}
```

### YAML<a name="aws-properties-cognito-userpool-lambdaconfig-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-lambdaconfig-createauthchallenge): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-lambdaconfig-custommessage): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-lambdaconfig-defineauthchallenge): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-lambdaconfig-postauthentication): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-lambdaconfig-postconfirmation): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-lambdaconfig-preauthentication): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-lambdaconfig-presignup): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-lambdaconfig-verifyauthchallengeresponse): String
```

## Properties<a name="aws-properties-cognito-userpool-lambdaconfig-properties"></a>

`CreateAuthChallenge`  
Creates an authentication challenge\.  
*Type*: String  
*Required: *No

`CustomMessage`  
A custom Message AWS Lambda trigger\.  
*Type*: String  
*Required: *No

`DefineAuthChallenge`  
Defines the authentication challenge\.  
*Type*: String  
*Required: *No

`PostAuthentication`  
A post\-authentication AWS Lambda trigger\.  
*Type*: String  
*Required: *No

`PostConfirmation`  
A post\-confirmation AWS Lambda trigger\.  
*Type*: String  
*Required: *No

`PreAuthentication`  
A pre\-authentication AWS Lambda trigger\.  
*Type*: String  
*Required: *No

`PreSignUp`  
A pre\-registration AWS Lambda trigger\.  
*Type*: String  
*Required: *No

`VerifyAuthChallengeResponse`  
Verifies the authentication challenge response\.  
*Type*: String  
*Required: *No