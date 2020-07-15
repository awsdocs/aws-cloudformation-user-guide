# AWS::SecretsManager::RotationSchedule<a name="aws-resource-secretsmanager-rotationschedule"></a>

The `AWS::SecretsManager::RotationSchedule` resource configures rotation for a secret\. You must have already configured the secret with the details of the database or service\. If you define both the secret and the database or service in an AWS CloudFormation template, then define the [AWS::SecretsManager::SecretTargetAttachment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-secrettargetattachment.html) resource to populate the secret with the connection details of the database or service before you attempt to configure rotation\.

**Important**  
When you configure rotation for a secret, AWS CloudFormation automatically rotates the secret one time\. Be sure you configure all your clients to retrieve the secret using Secrets Manager before configuring rotation to prevent breaking them\.

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
Specifies the ARN of the Lambda function that can rotate the secret\. If you don't specify this parameter, then the secret must already have the ARN of a Lambda function configured\. To reference a Lambda function also created in this template, use the [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html) function with the function's logical ID\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RotationRules`  <a name="cfn-secretsmanager-rotationschedule-rotationrules"></a>
Specifies a structure that defines the rotation schedule for this secret\.  
*Required*: No  
*Type*: [RotationRules](aws-properties-secretsmanager-rotationschedule-rotationrules.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretId`  <a name="cfn-secretsmanager-rotationschedule-secretid"></a>
Specifies the ARN or the friendly name of the secret that you want to rotate\. To reference a secret also created in this template, use the [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html) function with the secret's logical ID\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-secretsmanager-rotationschedule-return-values"></a>

### Ref<a name="aws-resource-secretsmanager-rotationschedule-return-values-ref"></a>

When you pass the logical ID of an `AWS::SecretsManager::RotationSchedule` resource to the intrinsic `Ref` function, the function returns the ARN of the secret being configured, such as:

*arn:aws:secretsmanager: us\-west\-2*:*123456789012*:secret:*my\-path/my\-secret\-name*\-*1a2b3c* 

This enables you to reference a secret you create in one part of the stack template from within the definition of another resource later, in the same template\. You typically do this when you define the [AWS::SecretsManager::SecretTargetAttachment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-secrettargetattachment.html) resource type\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\. 

## Examples<a name="aws-resource-secretsmanager-rotationschedule--examples"></a>

The following examples display complete examples of creating a secret, creating an RDS database instance associated with the secret and configuring rotation\. The example shows how to define a Lambda rotation function, attach the required trust and permissions policies, and associate the function with the secret on a defined schedule\.

RDS Secret Rotation

### Configuring RDS DB Secret Rotation<a name="aws-resource-secretsmanager-rotationschedule--examples--Configuring_RDS_DB_Secret_Rotation"></a>

#### JSON<a name="aws-resource-secretsmanager-rotationschedule--examples--Configuring_RDS_DB_Secret_Rotation--json"></a>

```
{
      "AWSTemplateFormatVersion": "2010-09-09",
      "Transform": "AWS::Serverless-2016-10-31",
      "Resources": {
        "MyRDSInstanceRotationSecret": {
          "Type": "AWS::SecretsManager::Secret",
          "Properties": {
            "Description": "A Secrets Manager secret for my RDS DB instance",
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
            "AllocatedStorage": 20,
            "DBInstanceClass": "db.t2.micro",
            "Engine": "mysql",
            "MasterUsername": {"Fn::Sub": "{{resolve:secretsmanager:${MyRDSInstanceRotationSecret}::username}}"},
            "MasterUserPassword": {"Fn::Sub": "{{resolve:secretsmanager:${MyRDSInstanceRotationSecret}::password}}"},
            "BackupRetentionPeriod": 0
          }
        },
        "MySecretRotationSchedule": {
          "Type": "AWS::SecretsManager::RotationSchedule",
          "DependsOn": "SecretRDSInstanceAttachment",
          "Properties": {
            "SecretId": {"Ref": "MyRDSInstanceRotationSecret"},
            "RotationLambdaARN": {"Fn::GetAtt": ["MyRotationServerlessApp","Outputs.RotationLambdaARN"]},
            "RotationRules": {
              "AutomaticallyAfterDays": 30
            }
          }
        },
        "MyRotationServerlessApp": {
          "Type": "AWS::Serverless::Application",
          "Properties":{
            "Location": {
              "ApplicationId": "arn:aws:serverlessrepo:us-east-1:297356227824:applications/SecretsManagerRDSMySQLRotationSingleUser",
              "SemanticVersion": "1.1.0"
            },
            "Parameters": {
              "endpoint": {"Fn::Sub": "https://secretsmanager.${AWS::Region}.amazonaws.com"},
              "functionName": "SecretsManagerMySQLRotationLambda"
            }
          }
        }
      }
    }
```

#### YAML<a name="aws-resource-secretsmanager-rotationschedule--examples--Configuring_RDS_DB_Secret_Rotation--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
    Transform: AWS::Serverless-2016-10-31
    Description: "This is an example template to demonstrate CloudFormation resources for Secrets Manager"
    Resources:
      #This is a Secret resource with a randomly generated password in its SecretString JSON.
      MyRDSInstanceRotationSecret:
        Type: AWS::SecretsManager::Secret
        Properties:
          Description: 'This is my rds instance secret'
          GenerateSecretString:
            SecretStringTemplate: '{"username": "admin"}'
            GenerateStringKey: 'password'
            PasswordLength: 16
            ExcludeCharacters: '"@/\'
          Tags:
            -
              Key: AppName
              Value: MyApp
     
      #This is an RDS instance resource. Its master username and password use dynamic references to resolve values from
      #SecretsManager. The dynamic reference guarantees that CloudFormation will not log or persist the resolved value
      #We sub the Secret resource's logical id in order to construct the dynamic reference, since the Secret's name is being
      #generated by CloudFormation
      MyDBInstance:
        Type: AWS::RDS::DBInstance
        Properties:
          AllocatedStorage: 20
          DBInstanceClass: db.t2.micro
          Engine: mysql
          MasterUsername: !Sub '{{resolve:secretsmanager:${MyRDSInstanceRotationSecret}::username}}'
          MasterUserPassword: !Sub '{{resolve:secretsmanager:${MyRDSInstanceRotationSecret}::password}}'
          BackupRetentionPeriod: 0
     
      #This is a SecretTargetAttachment resource which updates the referenced Secret resource with properties about
      #the referenced RDS instance
      SecretRDSInstanceAttachment:
        Type: AWS::SecretsManager::SecretTargetAttachment
        Properties:
          SecretId: !Ref MyRDSInstanceRotationSecret
          TargetId: !Ref MyDBInstance
          TargetType: AWS::RDS::DBInstance
     
      #This is a RotationSchedule resource. It configures rotation of password for the referenced secret using a rotation lambda
      #The first rotation happens at resource creation time, with subsequent rotations scheduled according to the rotation rules
      #We explicitly depend on the SecretTargetAttachment resource being created to ensure that the secret contains all the
      #information necessary for rotation to succeed
      MySecretRotationSchedule:
        Type: AWS::SecretsManager::RotationSchedule
        DependsOn: SecretRDSInstanceAttachment
        Properties:
          SecretId: !Ref MyRDSInstanceRotationSecret
          RotationLambdaARN: !GetAtt MyRotationServerlessApp.Outputs.RotationLambdaARN
          RotationRules:
            AutomaticallyAfterDays: 30
     
      # This is a AWS::Serverless::Application resource. The Location property is hardcoded to use the SecretsManager team's
      # MySQL single user rotation. The resource creates an IAM role and a Lambda function which uses the role. The Lambda function
      # is passed as the rotation lambda ref to the RotationSchedule resource
      MyRotationServerlessApp:
        Type: AWS::Serverless::Application
        Properties:
          Location:
            ApplicationId: 'arn:aws:serverlessrepo:us-east-1:297356227824:applications/SecretsManagerRDSMySQLRotationSingleUser'
            SemanticVersion: 1.1.0
          Parameters:
            endpoint: !Sub 'https://secretsmanager.${AWS::Region}.amazonaws.com'
            functionName: SecretsManagerMySQLRotationLambda
```

### Redshift Cluster Secret Rotation Example<a name="aws-resource-secretsmanager-rotationschedule--examples--Redshift_Cluster_Secret_Rotation_Example"></a>

#### JSON<a name="aws-resource-secretsmanager-rotationschedule--examples--Redshift_Cluster_Secret_Rotation_Example--json"></a>

```
{
      "AWSTemplateFormatVersion": "2010-09-09",
      "Transform": "AWS::Serverless-2016-10-31",
      "Resources": {
        "MyRedshiftSecret": {
          "Type": "AWS::SecretsManager::Secret",
          "Properties": {
            "Description": "This is a Secrets Manager secret for a Redshift cluster",
            "GenerateSecretString": {
              "SecretStringTemplate": "{\"username\": \"admin\"}",
              "GenerateStringKey": "password",
              "PasswordLength": 16,
              "ExcludeCharacters": "\"'@/\\"
            }
          }
        },
        "MyRedshiftCluster": {
          "Type": "AWS::Redshift::Cluster",
          "Properties": {
            "DBName": "myjsondb",
            "MasterUsername": {"Fn::Sub": "{{resolve:secretsmanager:${MyRedshiftSecret}::username}}"},
            "MasterUserPassword": {"Fn::Sub": "{{resolve:secretsmanager:${MyRedshiftSecret}::password}}"},
            "NodeType": "ds2.xlarge",
            "ClusterType": "single-node"
          }
        },
        "SecretRedshiftAttachment": {
          "Type": "AWS::SecretsManager::SecretTargetAttachment",
          "Properties": {
            "SecretId": {"Ref": "MyRedshiftSecret"},
            "TargetId": {"Ref": "MyRedshiftCluster"},
            "TargetType": "AWS::Redshift::Cluster"
          }
        },
        "MySecretRotationSchedule": {
          "Type": "AWS::SecretsManager::RotationSchedule",
          "DependsOn": "SecretRedshiftAttachment",
          "Properties": {
            "SecretId": {"Ref": "MyRedshiftSecret"},
            "RotationLambdaARN": {"Fn::GetAtt": ["MyRotationServerlessApp","Outputs.RotationLambdaARN"]},
            "RotationRules": {
              "AutomaticallyAfterDays": 30
            }
          }
        },
        "MyRotationServerlessApp": {
          "Type": "AWS::Serverless::Application",
          "Properties":{
            "Location": {
              "ApplicationId": "arn:aws:serverlessrepo:us-east-1:297356227824:applications/SecretsManagerRedshiftRotationSingleUser",
              "SemanticVersion": "1.1.0"
            },
            "Parameters": {
              "endpoint": {"Fn::Sub": "https://secretsmanager.${AWS::Region}.amazonaws.com"},
              "functionName": "SecretsManagerRedshiftRotationLambda"
            }
          }
        }
      }
    }
```

#### YAML<a name="aws-resource-secretsmanager-rotationschedule--examples--Redshift_Cluster_Secret_Rotation_Example--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
    Transform: AWS::Serverless-2016-10-31
    Description: "This is an example template to demonstrate CloudFormation resources for Secrets Manager"
    Resources:
      #This is a Secret resource with a randomly generated password in its SecretString JSON.
      MyRedshiftSecret:
        Type: "AWS::SecretsManager::Secret"
        Properties:
          Description: "This is a Secrets Manager secret for an Redshift cluster"
          GenerateSecretString:
            SecretStringTemplate: '{"username": "admin"}'
            GenerateStringKey: "password"
            PasswordLength: 16
            ExcludeCharacters: "\"@'/\\"
     
      # This is a Redshift cluster resource. The master username and password use dynamic references
      # to resolve values from Secrets Manager. The dynamic reference guarantees that CloudFormation
      # will not log or persist the resolved value. We use a Ref to the secret resource's logical id
      # to construct the dynamic reference, since the secret name is generated by CloudFormation.
      MyRedshiftCluster:
        Type: AWS::Redshift::Cluster
        Properties:
          DBName: "myyamldb"
          MasterUsername: !Sub '{{resolve:secretsmanager:${MyRedshiftSecret}::username}}'
          MasterUserPassword: !Sub '{{resolve:secretsmanager:${MyRedshiftSecret}::password}}'
          NodeType: "ds2.xlarge"
          ClusterType: "single-node"
     
      # This is a SecretTargetAttachment resource which updates the referenced Secret resource with properties about
      # the referenced Redshift cluster
      SecretRedshiftAttachment:
        Type: "AWS::SecretsManager::SecretTargetAttachment"
        Properties:
          SecretId: !Ref MyRedshiftSecret
          TargetId: !Ref MyRedshiftCluster
          TargetType: AWS::Redshift::Cluster
     
      #This is a RotationSchedule resource. It configures rotation of password for the referenced secret using a rotation lambda
      #The first rotation happens at resource creation time, with subsequent rotations scheduled according to the rotation rules
      #We explicitly depend on the SecretTargetAttachment resource being created to ensure that the secret contains all the
      #information necessary for rotation to succeed
      MySecretRotationSchedule:
        Type: AWS::SecretsManager::RotationSchedule
        DependsOn: SecretRedshiftAttachment
        Properties:
          SecretId: !Ref MyRedshiftSecret
          RotationLambdaARN: !GetAtt MyRotationServerlessApp.Outputs.RotationLambdaARN
          RotationRules:
            AutomaticallyAfterDays: 30
     
      # This is a AWS::Serverless::Application resource. The Location property is hardcoded to use the SecretsManager team's
      # MySQL single user rotation. The resource creates an IAM role and a Lambda function which uses the role. The Lambda function
      # is passed as the rotation lambda ref to the RotationSchedule resource
      MyRotationServerlessApp:
        Type: AWS::Serverless::Application
        Properties:
          Location:
            ApplicationId: 'arn:aws:serverlessrepo:us-east-1:297356227824:applications/SecretsManagerRedshiftRotationSingleUser'
            SemanticVersion: 1.1.0
          Parameters:
            endpoint: !Sub 'https://secretsmanager.${AWS::Region}.amazonaws.com'
            functionName: SecretsManagerRedshiftRotationLambda
```

### DocumentDB Cluster Secret Rotation Example<a name="aws-resource-secretsmanager-rotationschedule--examples--DocumentDB_Cluster_Secret_Rotation_Example"></a>

#### JSON<a name="aws-resource-secretsmanager-rotationschedule--examples--DocumentDB_Cluster_Secret_Rotation_Example--json"></a>

```
    {
      "AWSTemplateFormatVersion": "2010-09-09",
      "Transform": "AWS::Serverless-2016-10-31",
      "Resources": {
        "MyDocDBClusterRotationSecret": {
          "Type": "AWS::SecretsManager::Secret",
          "Properties": {
            "Description": "A Secrets Manager secret for my DocDB Cluster",
            "GenerateSecretString": {
              "SecretStringTemplate": "{\"username\": \"someadmin\"}",
              "GenerateStringKey": "password",
              "PasswordLength": 16,
              "ExcludeCharacters": "\"@/"
            }
          }
        },
        "SecretDocDBClusterAttachment": {
          "Type": "AWS::SecretsManager::SecretTargetAttachment",
          "Properties": {
            "SecretId": {"Ref": "MyDocDBClusterRotationSecret"},
            "TargetId": {"Ref": "MyDocDBCluster"},
            "TargetType": "AWS::DocDB::DBCluster"
          }
        },
        "MyDocDBCluster": {
          "Type": "AWS::DocDB::DBCluster",
          "Properties": {
            "MasterUsername": {"Fn::Sub": "{{resolve:secretsmanager:${MyDocDBClusterRotationSecret}::username}}"},
            "MasterUserPassword": {"Fn::Sub": "{{resolve:secretsmanager:${MyDocDBClusterRotationSecret}::password}}"},
          }
        },
        "MySecretRotationSchedule": {
          "Type": "AWS::SecretsManager::RotationSchedule",
          "DependsOn": "SecretDocDBClusterAttachment",
          "Properties": {
            "SecretId": {"Ref": "MyDocDBClusterRotationSecret"},
            "RotationLambdaARN": {"Fn::GetAtt": ["MyRotationServerlessApp","Outputs.RotationLambdaARN"]},
            "RotationRules": {
              "AutomaticallyAfterDays": 30
            }
          }
        },
        "MyRotationServerlessApp": {
          "Type": "AWS::Serverless::Application",
          "Properties":{
            "Location": {
              "ApplicationId": "arn:aws:serverlessrepo:us-east-1:297356227824:applications/SecretsManagerMongoDBRotationSingleUser",
              "SemanticVersion": "1.1.0"
            },
            "Parameters": {
              "endpoint": {"Fn::Sub": "https://secretsmanager.${AWS::Region}.amazonaws.com"},
              "functionName": "SecretsManagerDocDBRotationLambda"
            }
          }
        }
      }
    }
```

#### YAML<a name="aws-resource-secretsmanager-rotationschedule--examples--DocumentDB_Cluster_Secret_Rotation_Example--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
    Transform: AWS::Serverless-2016-10-31
    Description: "This is an example template to demonstrate CloudFormation resources for Secrets Manager"
    Resources:
      #This is a Secret resource with a randomly generated password in its SecretString JSON.
      MyDocDBClusterRotationSecret:
        Type: AWS::SecretsManager::Secret
        Properties:
          Description: 'This is my DocDB cluster secret'
          GenerateSecretString:
            SecretStringTemplate: '{"username": "someadmin"}'
            GenerateStringKey: 'password'
            PasswordLength: 16
            ExcludeCharacters: '"@/'
          Tags:
            -
              Key: AppName
              Value: MyApp
     
      #This is an DocDB cluster resource. Its master username and password use dynamic references to resolve values from
      #SecretsManager. The dynamic reference guarantees that CloudFormation will not log or persist the resolved value
      #We sub the Secret resource's logical id in order to construct the dynamic reference, since the Secret's name is being
      #generated by CloudFormation
      MyDocDBCluster:
        Type: AWS::DocDB::DBCluster
        Properties:
          MasterUsername: !Sub '{{resolve:secretsmanager:${MyDocDBClusterRotationSecret}::username}}'
          MasterUserPassword: !Sub '{{resolve:secretsmanager:${MyDocDBClusterRotationSecret}::password}}'
     
      #This is a SecretTargetAttachment resource which updates the referenced Secret resource with properties about
      #the referenced DocDB cluster
      SecretDocDBClusterAttachment:
        Type: AWS::SecretsManager::SecretTargetAttachment
        Properties:
          SecretId: !Ref MyDocDBClusterRotationSecret
          TargetId: !Ref MyDocDBCluster
          TargetType: AWS::DocDB::DBCluster
     
      #This is a RotationSchedule resource. It configures rotation of password for the referenced secret using a rotation lambda
      #The first rotation happens at resource creation time, with subsequent rotations scheduled according to the rotation rules
      #We explicitly depend on the SecretTargetAttachment resource being created to ensure that the secret contains all the
      #information necessary for rotation to succeed
      MySecretRotationSchedule:
        Type: AWS::SecretsManager::RotationSchedule
        DependsOn: SecretDocDBClusterAttachment
        Properties:
          SecretId: !Ref MyDocDBClusterRotationSecret
          RotationLambdaARN: !GetAtt MyRotationServerlessApp.Outputs.RotationLambdaARN
          RotationRules:
            AutomaticallyAfterDays: 30
     
      # This is a AWS::Serverless::Application resource. The Location property is hardcoded to use the SecretsManager team's
      # MongoDB single user rotation. The resource creates an IAM role and a Lambda function which uses the role. The Lambda function
      # is passed as the rotation lambda ref to the RotationSchedule resource
      MyRotationServerlessApp:
        Type: AWS::Serverless::Application
        Properties:
          Location:
            ApplicationId: 'arn:aws:serverlessrepo:us-east-1:297356227824:applications/SecretsManagerMongoDBRotationSingleUser'
            SemanticVersion: 1.1.0
          Parameters:
            endpoint: !Sub 'https://secretsmanager.${AWS::Region}.amazonaws.com'
            functionName: SecretsManagerDocDBRotationLambda
```

## See also<a name="aws-resource-secretsmanager-rotationschedule--seealso"></a>
+  [RotateSecret](https://docs.aws.amazon.com/secretsmanager/latest/apireference/API_RotateSecret.html) in the AWS Secrets Manager API Reference
+  [Rotating Your AWS Secrets Manager Secrets](https://docs.aws.amazon.com/secretsmanager/latest/userguide/rotating-secrets.html) in the AWS Secrets Manager User Guide
