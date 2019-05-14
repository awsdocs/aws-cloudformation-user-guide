# AWS::Cognito::UserPool LambdaConfig<a name="aws-properties-cognito-userpool-lambdaconfig"></a>

`LambdaConfig` is a property of the [AWS::Cognito::UserPool](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cognito-userpool.html) resource that defines the AWS Lambda configuration of an Amazon Cognito User Pool\.

**Note**  
In a push model, event sources \(such as Amazon S3 and custom applications\) need permission to invoke a function\. So you will need to make an extra call to add permission for these event sources to invoke your Lambda function\.  
For more information on using the Lambda API to add permission, see [ AddPermission ](https://docs.aws.amazon.com/lambda/latest/dg/API_AddPermission.html)\.   
For adding permission using the AWS CLI, see [ add\-permission ](https://docs.aws.amazon.com/cli/latest/reference/lambda/add-permission.html)\.

## Syntax<a name="aws-properties-cognito-userpool-lambdaconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cognito-userpool-lambdaconfig-syntax.json"></a>

```
{
  "[CreateAuthChallenge](#cfn-cognito-userpool-lambdaconfig-createauthchallenge)" : String,
  "[CustomMessage](#cfn-cognito-userpool-lambdaconfig-custommessage)" : String,
  "[DefineAuthChallenge](#cfn-cognito-userpool-lambdaconfig-defineauthchallenge)" : String,
  "[PostAuthentication](#cfn-cognito-userpool-lambdaconfig-postauthentication)" : String,
  "[PostConfirmation](#cfn-cognito-userpool-lambdaconfig-postconfirmation)" : String,
  "[PreAuthentication](#cfn-cognito-userpool-lambdaconfig-preauthentication)" : String,
  "[PreSignUp](#cfn-cognito-userpool-lambdaconfig-presignup)" : String,
  "[VerifyAuthChallengeResponse](#cfn-cognito-userpool-lambdaconfig-verifyauthchallengeresponse)" : String
}
```

### YAML<a name="aws-properties-cognito-userpool-lambdaconfig-syntax.yaml"></a>

```
﻿  [CreateAuthChallenge](#cfn-cognito-userpool-lambdaconfig-createauthchallenge) : String
﻿  [CustomMessage](#cfn-cognito-userpool-lambdaconfig-custommessage) : String
﻿  [DefineAuthChallenge](#cfn-cognito-userpool-lambdaconfig-defineauthchallenge) : String
﻿  [PostAuthentication](#cfn-cognito-userpool-lambdaconfig-postauthentication) : String
﻿  [PostConfirmation](#cfn-cognito-userpool-lambdaconfig-postconfirmation) : String
﻿  [PreAuthentication](#cfn-cognito-userpool-lambdaconfig-preauthentication) : String
﻿  [PreSignUp](#cfn-cognito-userpool-lambdaconfig-presignup) : String
﻿  [VerifyAuthChallengeResponse](#cfn-cognito-userpool-lambdaconfig-verifyauthchallengeresponse) : String
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

`CustomMessage`  <a name="cfn-cognito-userpool-lambdaconfig-custommessage"></a>
A custom Message AWS Lambda trigger\.  
*Required*: No  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `arn:[\w+=/,.@-]+:[\w+=/,.@-]+:([\w+=/,.@-]*)?:[0-9]+:[\w+=/,.@-]+(:[\w+=/,.@-]+)?(:[\w+=/,.@-]+)?`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefineAuthChallenge`  <a name="cfn-cognito-userpool-lambdaconfig-defineauthchallenge"></a>
Defines the authentication challenge\.  
*Required*: No  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `arn:[\w+=/,.@-]+:[\w+=/,.@-]+:([\w+=/,.@-]*)?:[0-9]+:[\w+=/,.@-]+(:[\w+=/,.@-]+)?(:[\w+=/,.@-]+)?`  
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

`VerifyAuthChallengeResponse`  <a name="cfn-cognito-userpool-lambdaconfig-verifyauthchallengeresponse"></a>
Verifies the authentication challenge response\.  
*Required*: No  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `arn:[\w+=/,.@-]+:[\w+=/,.@-]+:([\w+=/,.@-]*)?:[0-9]+:[\w+=/,.@-]+(:[\w+=/,.@-]+)?(:[\w+=/,.@-]+)?`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)