# AWS::SecretsManager::RotationSchedule<a name="aws-resource-secretsmanager-rotationschedule"></a>

The `AWS::SecretsManager::RotationSchedule` resource configures rotation for a secret\. The secret must already be configured with the details of the database or service\. If you define both the secret and the database or service in an AWS CloudFormation template, then define the [AWS::SecretsManager::SecretTargetAttachment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-secrettargetattachment.html) resource to populate the secret with the connection details of the database or service before you attempt to configure rotation\.

**Important**  
When you configure rotation for a secret, AWS CloudFormation automatically rotates the secret one time\. Ensure that you configure all your clients to retrieve the secret using Secrets Manager before configuring rotation to prevent breaking them\.

## Syntax<a name="aws-resource-secretsmanager-rotationschedule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-secretsmanager-rotationschedule-syntax.json"></a>

```
{
  "Type" : "AWS::SecretsManager::RotationSchedule",
  "Properties" : {
      "[RotationLambdaARN](#cfn-secretsmanager-rotationschedule-rotationlambdaarn)" : String,
      "[RotationRules](#cfn-secretsmanager-rotationschedule-rotationrules)" : [RotationRules](aws-properties-secretsmanager-rotationschedule-rotationrules.md),
      "[SecretId](#cfn-secretsmanager-rotationschedule-secretid)" : String
    }
}
```

### YAML<a name="aws-resource-secretsmanager-rotationschedule-syntax.yaml"></a>

```
Type: AWS::SecretsManager::RotationSchedule
Properties: 
  [RotationLambdaARN](#cfn-secretsmanager-rotationschedule-rotationlambdaarn): String
  [RotationRules](#cfn-secretsmanager-rotationschedule-rotationrules): 
    [RotationRules](aws-properties-secretsmanager-rotationschedule-rotationrules.md)
  [SecretId](#cfn-secretsmanager-rotationschedule-secretid): String
```

## Properties<a name="aws-resource-secretsmanager-rotationschedule-properties"></a>

`RotationLambdaARN`  <a name="cfn-secretsmanager-rotationschedule-rotationlambdaarn"></a>
Specifies the ARN of the Lambda function that can rotate the secret\. If you don't specify this parameter, then the secret must already have the ARN of a Lambda function configured\. To reference a Lambda function that's also created in this template, use the [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html) function with the function's logical ID\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RotationRules`  <a name="cfn-secretsmanager-rotationschedule-rotationrules"></a>
Specifies a structure that defines the rotation schedule for this secret\.  
*Required*: No  
*Type*: [RotationRules](aws-properties-secretsmanager-rotationschedule-rotationrules.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretId`  <a name="cfn-secretsmanager-rotationschedule-secretid"></a>
Specifies the Amazon Resource Name \(ARN\) or the friendly name of the secret that you want to rotate\. To reference a secret also that's created in this template, use the [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html) function with the secret's logical ID\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return Values<a name="aws-resource-secretsmanager-rotationschedule-return-values"></a>

### Ref<a name="aws-resource-secretsmanager-rotationschedule-return-values-ref"></a>

When you pass the logical ID of an `AWS::SecretsManager::RotationSchedule` resource to the intrinsic `Ref` function, the function returns the ARN of the secret that's being configured, such as:

*arn:aws:secretsmanager: us\-west\-2*:*123456789012*:secret:*my\-path/my\-secret\-name*\-*1a2b3c* 

This enables you to reference a secret that you create in one part of the stack template from within the definition of another resource later, in the same template\. You typically do this when you define the [AWS::SecretsManager::SecretTargetAttachment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-secrettargetattachment.html) resource type\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\. 

## Examples<a name="aws-resource-secretsmanager-rotationschedule--examples"></a>

### Configuring a Secret to Rotate<a name="aws-resource-secretsmanager-rotationschedule--examples--Configuring_a_Secret_to_Rotate"></a>

The following example shows a complete example of creating a secret, creating an RDS database instance that's associated with the secret and configuring it to rotate\. The example shows how to define a Lambda rotation function, attach the required trust and permissions policies, and associate the function with the secret on a defined schedule\.

#### JSON<a name="aws-resource-secretsmanager-rotationschedule--examples--Configuring_a_Secret_to_Rotate--json"></a>

```
{
  "MyRDSInstanceRotationSecret": {
    "Type": "AWS::SecretsManager::Secret",
    "Properties": {
      "Description": "This is my rds instance secret",
      "GenerateSecretString": {
        "SecretStringTemplate": "{\"username\": \"admin\"}",
        "GenerateStringKey": "password",
        "PasswordLength": 16,
        "ExcludeCharacters": "\"@/\\"
      }
    }
  },
  "SecretRDSInstanceAttachment": {
    "Type": "AWS::SecretsManager::SecretTargetAttachment",
    "Properties": {
      "SecretId": {"Ref": "MyRDSInstanceRotationSecret"},
      "TargetId": {"Ref": "MyDBInstance"},
      "TargetType": "AWS::RDS::DBInstance"
    }
  },
  "MyDBInstance": {
    "Type": "AWS::RDS::DBInstance",
    "Properties": {
      "AllocatedStorage": "’20’",
      "DBInstanceClass": "db.t2.micro",
      "Engine": "mysql",
      "MasterUsername": {"Fn::Join": [
        "",
        ["{{resolve:secretsmanager:",{"Ref": "MyRDSInstanceRotationSecret"},"::username}}"]
      ]},
      "MasterUserPassword": {"Fn::Join": [
        "",
        ["{{resolve:secretsmanager:",{"Ref": "MyRDSInstanceRotationSecret"},"::password}}"]
      ]},
      "BackupRetentionPeriod": 0,
      "DBInstanceIdentifier": "rotation-instance"
    }
  },
  "MySecretRotationSchedule": {
    "Type": "“AWS::SecretsManager::RotationSchedule\"",
    "DependsOn": "SecretRDSInstanceAttachment",
    "Properties": {
      "SecretId": {"Ref": "MyRDSInstanceRotationSecret"},
      "RotationLambdaARN": {"Fn::GetAtt": ["MyRotationLambda", "Arn"]},
      "RotationRules": {
        "AutomaticallyAfterDays": 5
      }
    }
  },
  "LambdaInvokePermission": {
    "Type": "AWS::Lambda::Permission",
    "DependsOn": "MyRotationLambda",
    "Properties": {
      "FunctionName": "cfn-rotation-lambda",
      "Action": "lambda:InvokeFunction",
      "Principal": "secretsmanager.amazonaws.com"
    }
  },
  "MyLambdaExecutionRole": {
    "Type": "AWS::IAM::Role",
    "Properties": {
      "RoleName": "cfn-rotation-lambda-role",
      "AssumeRolePolicyDocument": {
        "Version": "2012-10-17",
        "Statement": [
          {
            "Effect": "Allow",
            "Principal": {
              "Service": [
                "lambda.amazonaws.com"
              ]
            },
            "Action": [
              "sts:AssumeRole"
            ]
          }
        ]
      },
      "Policies": [
        {
          "PolicyName": "AWSSecretsManagerRotationPolicy",
          "PolicyDocument": {
            "Version": "2012-10-17",
            "Statement": [
              {
                "Effect": "Allow",
                "Action": [
                  "secretsmanager:DescribeSecret",
                  "secretsmanager:GetSecretValue",
                  "secretsmanager:PutSecretValue",
                  "secretsmanager:UpdateSecretVersionStage"
                ],
                "Resource": {"Fn::Sub": "arn:${AWS::Partition}:secretsmanager:${AWS::Region}:${AWS::AccountId}:secret:*"},
                "Condition": {
                  "StringEquals": {
                    "secretsmanager:resource/AllowRotationLambdaArn": {
                      "Fn::Sub": "arn:${AWS::Partition}:lambda:${AWS::Region}:${AWS::AccountId}:function:cfn-rotation-lambda"
                    }
                  }
                }
              },
              {
                "Effect": "Allow",
                "Action": [
                  "secretsmanager:GetRandomPassword"
                ],
                "Resource": "*"
              },
              {
                "Effect": "Allow",
                "Action": [
                  "logs:CreateLogGroup",
                  "logs:CreateLogStream",
                  "logs:PutLogEvents"
                ],
                "Resource": "arn:aws:logs:*:*:*"
              },
              {
                "Effect": "Allow",
                "Action": [
                  "kms:Decrypt",
                  "kms:DescribeKey",
                  "kms:GenerateDataKey"
                ],
                "Resource": "*"
              }
            ]
          }
        }
      ]
    }
  },
  "MyRotationLambda": {
    "Type": "AWS::Lambda::Function",
    "Properties": {
      "Runtime": "python2.7",
      "Role": {"Fn::GetAtt": ["MyLambdaExecutionRole","Arn"]},
      "Handler": "lambda_function.lambda_handler",
      "Description": "This is a lambda to rotate MySql user passwd",
      "FunctionName": "cfn-rotation-lambda",
      "Environment": {
        "Variables": {
          "SECRETS_MANAGER_ENDPOINT": {"Fn::Sub": "https://secretsmanager.${AWS::Region}.amazonaws.com"}
        }
      },
      "Code": {
        "S3Bucket": "<% replace-this-with-name-of-s3-bucket-that-contains-lambda-function-code %>",
        "S3Key": "<% replace-this-with-path-and-filename-of-zip-file-that-contains-lambda-function-code %>",
        "S3ObjectVersion": "<% replace-this-with-lambda-zip-file-version-if-s3-bucket-versioning-is-enabled %>"
      }
    }
  }
}
```

#### YAML<a name="aws-resource-secretsmanager-rotationschedule--examples--Configuring_a_Secret_to_Rotate--yaml"></a>

```
#This is a Secret resource with a randomly generated password in its SecretString JSON.
  MyRDSInstanceRotationSecret:
    Type: AWS::SecretsManager::Secret
    Properties:
      Description: "This is my rds instance secret"
      GenerateSecretString:
        SecretStringTemplate: '{"username": "admin"}'
        GenerateStringKey: "password"
        PasswordLength: 16
        ExcludeCharacters: '"@/\'

  # This is an RDS instance resource. The master username and password use dynamic references
  # to resolve values from Secrets Manager. The dynamic reference guarantees that CloudFormation
  # will not log or persist the resolved value. We use a Ref to the secret resource's logical id
  # to construct the dynamic reference, since the secret name is generated by CloudFormation.
  MyDBInstance:
    Type: AWS::RDS::DBInstance
    Properties:
      AllocatedStorage: 20
      DBInstanceClass: db.t2.micro
      Engine: mysql
      MasterUsername: !Join ['', ['{{resolve:secretsmanager:', !Ref MyRDSInstanceRotationSecret, '::username}}' ]]
      MasterUserPassword: !Join ['', ['{{resolve:secretsmanager:', !Ref MyRDSInstanceRotationSecret, '::password}}' ]]
      BackupRetentionPeriod: 0
      DBInstanceIdentifier: 'rotation-instance'

  #This is a SecretTargetAttachment resource which updates the referenced Secret resource with properties about
  #the referenced RDS instance
  SecretRDSInstanceAttachment:
    Type: AWS::SecretsManager::SecretTargetAttachment
    Properties:
      SecretId: !Ref MyRDSInstanceRotationSecret
      TargetId: !Ref MyDBInstance
      TargetType: AWS::RDS::DBInstance

  # This is a RotationSchedule resource. It configures rotation of the password for the referenced
  # secret using a Lambda rotation function. The first rotation happens immediately when
  # CloudFormation processes this resource type. All subsequent rotations are scheduled according to
  # the configured rotation rules. We explicitly depend on the SecretTargetAttachment resource to
  # ensure that the secret contains all the information necessary for rotation to succeed.
  MySecretRotationSchedule:
    Type: AWS::SecretsManager::RotationSchedule
    DependsOn: SecretRDSInstanceAttachment
    Properties:
      SecretId: !Ref MyRDSInstanceRotationSecret
      RotationLambdaARN: !GetAtt MyRotationLambda.Arn
      RotationRules:
        AutomaticallyAfterDays: 5

  #This is a Lambda Permission resource that grants Secrets Manager permission to invoke the function
  LambdaInvokePermission:
    Type: AWS::Lambda::Permission
    DependsOn: MyRotationLambda
    Properties:
      FunctionName: 'cfn-rotation-lambda'
      Action: 'lambda:InvokeFunction'
      Principal: secretsmanager.amazonaws.com

  # This is an IAM Role resource. It gets attached to the Lambda rotation function and grants
  # permissions to the function to retrieve and update the secret as part of the rotation process.
  # It also includes the required KMS permissions and CloudWatch logging permissions.
  MyLambdaExecutionRole:
    Type: AWS::IAM::Role
    Properties:
      RoleName: 'cfn-rotation-lambda-role'
      AssumeRolePolicyDocument:
        Version: "2012-10-17"
        Statement:
          -
            Effect: "Allow"
            Principal:
              Service:
                - "lambda.amazonaws.com"
            Action:
              - "sts:AssumeRole"
      Policies:
        -
          PolicyName: "AWSSecretsManagerRotationPolicy"
          PolicyDocument:
            Version: "2012-10-17"
            Statement:
              -
                Effect: "Allow"
                Action:
                  - "secretsmanager:DescribeSecret"
                  - "secretsmanager:GetSecretValue"
                  - "secretsmanager:PutSecretValue"
                  - "secretsmanager:UpdateSecretVersionStage"
                Resource: !Sub 'arn:${AWS::Partition}:secretsmanager:${AWS::Region}:${AWS::AccountId}:secret:*'
                Condition:
                  StringEquals:
                    secretsmanager:resource/AllowRotationLambdaArn: !Sub 'arn:${AWS::Partition}:lambda:${AWS::Region}:${AWS::AccountId}:function:cfn-rotation-lambda'
              -
                Effect: "Allow"
                Action:
                  - "secretsmanager:GetRandomPassword"
                Resource: "*"
              -
                Effect: "Allow"
                Action:
                  - "logs:CreateLogGroup"
                  - "logs:CreateLogStream"
                  - "logs:PutLogEvents"
                Resource: "arn:aws:logs:*:*:*"
              -
                Effect: "Allow"
                Action:
                  - "kms:Decrypt"
                  - "kms:DescribeKey"
                  - "kms:GenerateDataKey"
                Resource: "*"

  # This is a Lambda Function resource. We use this to create the rotation function that rotate
  # our secret. For details about rotation Lambdas, see:
  # https://docs.aws.amazon.com/secretsmanager/latest/userguide/rotating-secrets.html
  # This example assumes that the Lambda code is already present in an S3 bucket, and that it
  # is coded to rotate a MySQL database password
  MyRotationLambda:
    Type: AWS::Lambda::Function
    Properties:
      Runtime: python2.7
      Role: !GetAtt MyLambdaExecutionRole.Arn
      Handler: lambda_function.lambda_handler
      Description: 'This is a lambda to rotate MySql user passwd'
      FunctionName: 'cfn-rotation-lambda'
      Environment:
        Variables:
          SECRETS_MANAGER_ENDPOINT: !Sub 'https://secretsmanager.${AWS::Region}.amazonaws.com'
      Code:
        S3Bucket: <% replace-this-with-name-of-s3-bucket-that-contains-lambda-function-code %>
        S3Key: <% replace-this-with-path-and-filename-of-zip-file-that-contains-lambda-function-code %>
        S3ObjectVersion: <% replace-this-with-lambda-zip-file-version-if-s3-bucket-versioning-is-enabled %>
```

## See Also<a name="aws-resource-secretsmanager-rotationschedule--seealso"></a>
+  [RotateSecret](https://docs.aws.amazon.com/secretsmanager/latest/apireference/API_RotateSecret.html) in the AWS Secrets Manager API Reference
+  [Rotating Your AWS Secrets Manager Secrets](https://docs.aws.amazon.com/secretsmanager/latest/userguide/rotating-secrets.html) in the AWS Secrets Manager User Guide

## Supported Regions

This ResourceType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `ca-central-1`
- `eu-central-1`
- `eu-west-1`
- `eu-west-2`
- `eu-west-3`
- `sa-east-1`
- `us-east-1`
- `us-east-2`
- `us-gov-west-1`
- `us-west-1`
- `us-west-2`
