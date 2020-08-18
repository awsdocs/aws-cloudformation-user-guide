# AWS::RDS::DBProxy AuthFormat<a name="aws-properties-rds-dbproxy-authformat"></a>

Specifies the details of authentication used by a proxy to log in as a specific database user\.

## Syntax<a name="aws-properties-rds-dbproxy-authformat-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-rds-dbproxy-authformat-syntax.json"></a>

```
{
  "[AuthScheme](#cfn-rds-dbproxy-authformat-authscheme)" : String,
  "[Description](#cfn-rds-dbproxy-authformat-description)" : String,
  "[IAMAuth](#cfn-rds-dbproxy-authformat-iamauth)" : String,
  "[SecretArn](#cfn-rds-dbproxy-authformat-secretarn)" : String,
  "[UserName](#cfn-rds-dbproxy-authformat-username)" : String
}
```

### YAML<a name="aws-properties-rds-dbproxy-authformat-syntax.yaml"></a>

```
  [AuthScheme](#cfn-rds-dbproxy-authformat-authscheme): String
  [Description](#cfn-rds-dbproxy-authformat-description): String
  [IAMAuth](#cfn-rds-dbproxy-authformat-iamauth): String
  [SecretArn](#cfn-rds-dbproxy-authformat-secretarn): String
  [UserName](#cfn-rds-dbproxy-authformat-username): String
```

## Properties<a name="aws-properties-rds-dbproxy-authformat-properties"></a>

`AuthScheme`  <a name="cfn-rds-dbproxy-authformat-authscheme"></a>
The type of authentication that the proxy uses for connections from the proxy to the underlying database\.  
Valid Values: `SECRETS`  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-rds-dbproxy-authformat-description"></a>
A user\-specified description about the authentication used by a proxy to log in as a specific database user\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IAMAuth`  <a name="cfn-rds-dbproxy-authformat-iamauth"></a>
Whether to require or disallow AWS Identity and Access Management \(IAM\) authentication for connections to the proxy\.  
Valid Values: `DISABLED | REQUIRED`  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretArn`  <a name="cfn-rds-dbproxy-authformat-secretarn"></a>
The Amazon Resource Name \(ARN\) representing the secret that the proxy uses to authenticate to the RDS DB instance or Aurora DB cluster\. These secrets are stored within Amazon Secrets Manager\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserName`  <a name="cfn-rds-dbproxy-authformat-username"></a>
The name of the database user to which the proxy connects\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)