# AWS::Cognito::UserPoolClient AnalyticsConfiguration<a name="aws-properties-cognito-userpoolclient-analyticsconfiguration"></a>

The Amazon Pinpoint analytics configuration necessary to collect metrics for a user pool\.

**Note**  
In Regions where Amazon Pinpointisn't available, user pools only support sending events to Amazon Pinpoint projects in us\-east\-1\. In Regions where Amazon Pinpoint is available, user pools support sending events to Amazon Pinpoint projects within that same Region\.

## Syntax<a name="aws-properties-cognito-userpoolclient-analyticsconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cognito-userpoolclient-analyticsconfiguration-syntax.json"></a>

```
{
  "[ApplicationArn](#cfn-cognito-userpoolclient-analyticsconfiguration-applicationarn)" : String,
  "[ApplicationId](#cfn-cognito-userpoolclient-analyticsconfiguration-applicationid)" : String,
  "[ExternalId](#cfn-cognito-userpoolclient-analyticsconfiguration-externalid)" : String,
  "[RoleArn](#cfn-cognito-userpoolclient-analyticsconfiguration-rolearn)" : String,
  "[UserDataShared](#cfn-cognito-userpoolclient-analyticsconfiguration-userdatashared)" : Boolean
}
```

### YAML<a name="aws-properties-cognito-userpoolclient-analyticsconfiguration-syntax.yaml"></a>

```
  [ApplicationArn](#cfn-cognito-userpoolclient-analyticsconfiguration-applicationarn): String
  [ApplicationId](#cfn-cognito-userpoolclient-analyticsconfiguration-applicationid): String
  [ExternalId](#cfn-cognito-userpoolclient-analyticsconfiguration-externalid): String
  [RoleArn](#cfn-cognito-userpoolclient-analyticsconfiguration-rolearn): String
  [UserDataShared](#cfn-cognito-userpoolclient-analyticsconfiguration-userdatashared): Boolean
```

## Properties<a name="aws-properties-cognito-userpoolclient-analyticsconfiguration-properties"></a>

`ApplicationArn`  <a name="cfn-cognito-userpoolclient-analyticsconfiguration-applicationarn"></a>
The Amazon Resource Name \(ARN\) of an Amazon Pinpoint project\. You can use the Amazon Pinpoint project for integration with the chosen user pool client\. Amazon Cognito publishes events to the Amazon Pinpoint project that the app ARN declares\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ApplicationId`  <a name="cfn-cognito-userpoolclient-analyticsconfiguration-applicationid"></a>
The application ID for an Amazon Pinpoint application\.  
*Required*: No  
*Type*: String  
*Pattern*: `^[0-9a-fA-F]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExternalId`  <a name="cfn-cognito-userpoolclient-analyticsconfiguration-externalid"></a>
The external ID\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-cognito-userpoolclient-analyticsconfiguration-rolearn"></a>
The ARN of an AWS Identity and Access Management role that authorizes Amazon Cognito to publish events to Amazon Pinpoint analytics\.  
*Required*: No  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `arn:[\w+=/,.@-]+:[\w+=/,.@-]+:([\w+=/,.@-]*)?:[0-9]+:[\w+=/,.@-]+(:[\w+=/,.@-]+)?(:[\w+=/,.@-]+)?`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserDataShared`  <a name="cfn-cognito-userpoolclient-analyticsconfiguration-userdatashared"></a>
If `UserDataShared` is `true`, Amazon Cognito includes user data in the events that it publishes to Amazon Pinpoint analytics\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)