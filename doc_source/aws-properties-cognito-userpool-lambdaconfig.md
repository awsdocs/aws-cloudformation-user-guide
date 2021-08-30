# AWS::Cognito::UserPool LambdaConfig<a name="aws-properties-cognito-userpool-lambdaconfig"></a>

Specifies the configuration for AWS Lambda triggers\.

## Syntax<a name="aws-properties-cognito-userpool-lambdaconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cognito-userpool-lambdaconfig-syntax.json"></a>

```
{
  "[CreateAuthChallenge](#cfn-cognito-userpool-lambdaconfig-createauthchallenge)" : String,
  "[CustomEmailSender](#cfn-cognito-userpool-lambdaconfig-customemailsender)" : CustomEmailSender,
  "[CustomMessage](#cfn-cognito-userpool-lambdaconfig-custommessage)" : String,
  "[CustomSMSSender](#cfn-cognito-userpool-lambdaconfig-customsmssender)" : CustomSMSSender,
  "[DefineAuthChallenge](#cfn-cognito-userpool-lambdaconfig-defineauthchallenge)" : String,
  "[KMSKeyID](#cfn-cognito-userpool-lambdaconfig-kmskeyid)" : String,
  "[PostAuthentication](#cfn-cognito-userpool-lambdaconfig-postauthentication)" : String,
  "[PostConfirmation](#cfn-cognito-userpool-lambdaconfig-postconfirmation)" : String,
  "[PreAuthentication](#cfn-cognito-userpool-lambdaconfig-preauthentication)" : String,
  "[PreSignUp](#cfn-cognito-userpool-lambdaconfig-presignup)" : String,
  "[PreTokenGeneration](#cfn-cognito-userpool-lambdaconfig-pretokengeneration)" : String,
  "[UserMigration](#cfn-cognito-userpool-lambdaconfig-usermigration)" : String,
  "[VerifyAuthChallengeResponse](#cfn-cognito-userpool-lambdaconfig-verifyauthchallengeresponse)" : String
}
```

### YAML<a name="aws-properties-cognito-userpool-lambdaconfig-syntax.yaml"></a>

```
  [CreateAuthChallenge](#cfn-cognito-userpool-lambdaconfig-createauthchallenge): String
  [CustomEmailSender](#cfn-cognito-userpool-lambdaconfig-customemailsender): 
    CustomEmailSender
  [CustomMessage](#cfn-cognito-userpool-lambdaconfig-custommessage): String
  [CustomSMSSender](#cfn-cognito-userpool-lambdaconfig-customsmssender): 
    CustomSMSSender
  [DefineAuthChallenge](#cfn-cognito-userpool-lambdaconfig-defineauthchallenge): String
  [KMSKeyID](#cfn-cognito-userpool-lambdaconfig-kmskeyid): String
  [PostAuthentication](#cfn-cognito-userpool-lambdaconfig-postauthentication): String
  [PostConfirmation](#cfn-cognito-userpool-lambdaconfig-postconfirmation): String
  [PreAuthentication](#cfn-cognito-userpool-lambdaconfig-preauthentication): String
  [PreSignUp](#cfn-cognito-userpool-lambdaconfig-presignup): String
  [PreTokenGeneration](#cfn-cognito-userpool-lambdaconfig-pretokengeneration): String
  [UserMigration](#cfn-cognito-userpool-lambdaconfig-usermigration): String
  [VerifyAuthChallengeResponse](#cfn-cognito-userpool-lambdaconfig-verifyauthchallengeresponse): String
```

## Properties<a name="aws-properties-cognito-userpool-lambdaconfig-properties"></a>

`CreateAuthChallenge`  <a name="cfn-cognito-userpool-lambdaconfig-createauthchallenge"></a>
Creates an authentication challenge\.  
*Required*: No  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `arn:[\w+=/,.@-]+:[\w+=/,.@-]+:([\w+=/,.@-]*)?:[0-9]+:[\w+=/,.@-]+(:[\w+=/,.@-]+)?(:[\w+=/,.@-]+)?`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CustomEmailSender`  <a name="cfn-cognito-userpool-lambdaconfig-customemailsender"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: [CustomEmailSender](aws-properties-cognito-userpool-customemailsender.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CustomMessage`  <a name="cfn-cognito-userpool-lambdaconfig-custommessage"></a>
A custom Message AWS Lambda trigger\.  
*Required*: No  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `arn:[\w+=/,.@-]+:[\w+=/,.@-]+:([\w+=/,.@-]*)?:[0-9]+:[\w+=/,.@-]+(:[\w+=/,.@-]+)?(:[\w+=/,.@-]+)?`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CustomSMSSender`  <a name="cfn-cognito-userpool-lambdaconfig-customsmssender"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: [CustomSMSSender](aws-properties-cognito-userpool-customsmssender.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefineAuthChallenge`  <a name="cfn-cognito-userpool-lambdaconfig-defineauthchallenge"></a>
Defines the authentication challenge\.  
*Required*: No  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `arn:[\w+=/,.@-]+:[\w+=/,.@-]+:([\w+=/,.@-]*)?:[0-9]+:[\w+=/,.@-]+(:[\w+=/,.@-]+)?(:[\w+=/,.@-]+)?`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KMSKeyID`  <a name="cfn-cognito-userpool-lambdaconfig-kmskeyid"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PostAuthentication`  <a name="cfn-cognito-userpool-lambdaconfig-postauthentication"></a>
A post\-authentication AWS Lambda trigger\.  
*Required*: No  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `arn:[\w+=/,.@-]+:[\w+=/,.@-]+:([\w+=/,.@-]*)?:[0-9]+:[\w+=/,.@-]+(:[\w+=/,.@-]+)?(:[\w+=/,.@-]+)?`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PostConfirmation`  <a name="cfn-cognito-userpool-lambdaconfig-postconfirmation"></a>
A post\-confirmation AWS Lambda trigger\.  
*Required*: No  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `arn:[\w+=/,.@-]+:[\w+=/,.@-]+:([\w+=/,.@-]*)?:[0-9]+:[\w+=/,.@-]+(:[\w+=/,.@-]+)?(:[\w+=/,.@-]+)?`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PreAuthentication`  <a name="cfn-cognito-userpool-lambdaconfig-preauthentication"></a>
A pre\-authentication AWS Lambda trigger\.  
*Required*: No  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `arn:[\w+=/,.@-]+:[\w+=/,.@-]+:([\w+=/,.@-]*)?:[0-9]+:[\w+=/,.@-]+(:[\w+=/,.@-]+)?(:[\w+=/,.@-]+)?`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PreSignUp`  <a name="cfn-cognito-userpool-lambdaconfig-presignup"></a>
A pre\-registration AWS Lambda trigger\.  
*Required*: No  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `arn:[\w+=/,.@-]+:[\w+=/,.@-]+:([\w+=/,.@-]*)?:[0-9]+:[\w+=/,.@-]+(:[\w+=/,.@-]+)?(:[\w+=/,.@-]+)?`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PreTokenGeneration`  <a name="cfn-cognito-userpool-lambdaconfig-pretokengeneration"></a>
A Lambda trigger that is invoked before token generation\.  
*Required*: No  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `arn:[\w+=/,.@-]+:[\w+=/,.@-]+:([\w+=/,.@-]*)?:[0-9]+:[\w+=/,.@-]+(:[\w+=/,.@-]+)?(:[\w+=/,.@-]+)?`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserMigration`  <a name="cfn-cognito-userpool-lambdaconfig-usermigration"></a>
The user migration Lambda config type\.  
*Required*: No  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `arn:[\w+=/,.@-]+:[\w+=/,.@-]+:([\w+=/,.@-]*)?:[0-9]+:[\w+=/,.@-]+(:[\w+=/,.@-]+)?(:[\w+=/,.@-]+)?`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VerifyAuthChallengeResponse`  <a name="cfn-cognito-userpool-lambdaconfig-verifyauthchallengeresponse"></a>
Verifies the authentication challenge response\.  
*Required*: No  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `arn:[\w+=/,.@-]+:[\w+=/,.@-]+:([\w+=/,.@-]*)?:[0-9]+:[\w+=/,.@-]+(:[\w+=/,.@-]+)?(:[\w+=/,.@-]+)?`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)