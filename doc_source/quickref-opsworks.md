# AWS OpsWorks template snippets<a name="quickref-opsworks"></a>

AWS OpsWorks is an application management service that simplifies a wide range of tasks such as software configuration, application deployment, scaling, and monitoring\. AWS CloudFormation is a resource management service that you can use to manage AWS OpsWorks resources, such as AWS OpsWorks stacks, layers, apps, and instances\.

## AWS OpsWorks sample PHP app<a name="quickref-opsworks-sample-php-app"></a>

The following sample template deploys a sample AWS OpsWorks PHP web application that is stored in public Git repository\. The AWS OpsWorks stack includes two application servers with a load balancer that distributes incoming traffic evenly across the servers\. The AWS OpsWorks stack also includes a back\-end MySQL database server to store data\. For more information about the sample AWS OpsWorks application, see [Walkthrough: Learn AWS AWS OpsWorks basics by creating an application server stack](https://docs.aws.amazon.com/opsworks/latest/userguide/gettingstarted.html) in the *AWS OpsWorks User Guide*\.

**Note**  
The `ServiceRoleArn` and `DefaultInstanceProfileArn` properties reference IAM roles that are created after you use AWS OpsWorks for the first time\.

The example defines the `MysqlRootPassword` parameter with its `NoEcho` property set to `true`\. If you set the `NoEcho` attribute to `true`, CloudFormation returns the parameter value masked as asterisks \(\*\*\*\*\*\) for any calls that describe the stack or stack events\.

**Important**  
Rather than embedding sensitive information directly in your AWS CloudFormation templates, we recommend you use dynamic parameters in the stack template to reference sensitive information that is stored and managed outside of CloudFormation, such as in the AWS Systems Manager Parameter Store or AWS Secrets Manager\.  
For more information, see the [Do not embed credentials in your templates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/best-practices.html#creds) best practice\.

### JSON<a name="quickref-opsworks-example-1.json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Parameters": {
    "ServiceRole": {
      "Default": "aws-opsworks-service-role",
      "Description": "The OpsWorks service role",
      "Type": "String",
      "MinLength": "1",
      "MaxLength": "64",
      "AllowedPattern": "[a-zA-Z][a-zA-Z0-9-]*",
      "ConstraintDescription": "must begin with a letter and contain only alphanumeric characters."
    },
    "InstanceRole": {
      "Default": "aws-opsworks-ec2-role",
      "Description": "The OpsWorks instance role",
      "Type": "String",
      "MinLength": "1",
      "MaxLength": "64",
      "AllowedPattern": "[a-zA-Z][a-zA-Z0-9-]*",
      "ConstraintDescription": "must begin with a letter and contain only alphanumeric characters."
    },
    "AppName": {
      "Default": "myapp",
      "Description": "The app name",
      "Type": "String",
      "MinLength": "1",
      "MaxLength": "64",
      "AllowedPattern": "[a-zA-Z][a-zA-Z0-9]*",
      "ConstraintDescription": "must begin with a letter and contain only alphanumeric characters."
    },
    "MysqlRootPassword" : {
      "Description" : "MysqlRootPassword",
      "NoEcho" : "true",
      "Type" : "String"
    }
  },
  "Resources": {
    "myStack": {
      "Type": "AWS::OpsWorks::Stack",
      "Properties": {
        "Name": {
          "Ref": "AWS::StackName"
        },
        "ServiceRoleArn": {
          "Fn::Join": [
            "", ["arn:aws:iam::", {"Ref": "AWS::AccountId"},
                  ":role/", {"Ref": "ServiceRole"}]
          ]
        },
        "DefaultInstanceProfileArn": {
          "Fn::Join": [
            "", ["arn:aws:iam::", {"Ref": "AWS::AccountId"},
              ":instance-profile/", {"Ref": "InstanceRole"}]
          ]
        },
        "UseCustomCookbooks": "true",
        "CustomCookbooksSource": {
          "Type": "git",
          "Url": "git://github.com/amazonwebservices/opsworks-example-cookbooks.git"
        }
      }
    },    
    "myLayer": {
      "Type": "AWS::OpsWorks::Layer",
      "DependsOn": "myApp",
      "Properties": {
        "StackId": {"Ref": "myStack"},
        "Type": "php-app",
	    "Shortname" : "php-app",
        "EnableAutoHealing" : "true",
        "AutoAssignElasticIps" : "false",
        "AutoAssignPublicIps" : "true",
        "Name": "MyPHPApp",
        "CustomRecipes" : {
          "Configure" : ["phpapp::appsetup"]
        }
      }
    },
    "DBLayer" : {
      "Type" : "AWS::OpsWorks::Layer",
      "DependsOn": "myApp",
      "Properties" : {
        "StackId" : {"Ref":"myStack"},
        "Type" : "db-master",
	    "Shortname" : "db-layer",
        "EnableAutoHealing" : "true",
        "AutoAssignElasticIps" : "false",
        "AutoAssignPublicIps" : "true",
        "Name" : "MyMySQL",
        "CustomRecipes" : {
          "Setup" : ["phpapp::dbsetup"]
        },
        "Attributes" : {
          "MysqlRootPassword" : {"Ref":"MysqlRootPassword"},
          "MysqlRootPasswordUbiquitous": "true"
        },
        "VolumeConfigurations":[{"MountPoint":"/vol/mysql","NumberOfDisks":1,"Size":10}]
      }
    },    
    "ELBAttachment" : {
      "Type" : "AWS::OpsWorks::ElasticLoadBalancerAttachment",
      "Properties" : {
        "ElasticLoadBalancerName" : { "Ref" : "ELB" },
        "LayerId" : { "Ref" : "myLayer" }
      }
    },	
    "ELB" : {
      "Type": "AWS::ElasticLoadBalancing::LoadBalancer",
      "Properties": {
        "AvailabilityZones": { "Fn::GetAZs" : "" } ,
        "Listeners": [{
          "LoadBalancerPort": "80",
          "InstancePort": "80",
          "Protocol": "HTTP",
          "InstanceProtocol": "HTTP"
        }],
        "HealthCheck": {
          "Target": "HTTP:80/",
          "HealthyThreshold": "2",
          "UnhealthyThreshold": "10",
          "Interval": "30",
          "Timeout": "5"
        }
      }
    },
    "myAppInstance1": {
      "Type": "AWS::OpsWorks::Instance",
      "Properties": {
        "StackId": {"Ref": "myStack"},
        "LayerIds": [{"Ref": "myLayer"}],
        "InstanceType": "m1.small"
      }
    },    
    "myAppInstance2": {
      "Type": "AWS::OpsWorks::Instance",
      "Properties": {
        "StackId": {"Ref": "myStack"},
        "LayerIds": [{"Ref": "myLayer"}],
        "InstanceType": "m1.small"
      }
    },
    "myDBInstance": {
      "Type": "AWS::OpsWorks::Instance",
      "Properties": {
        "StackId": {"Ref": "myStack"},
        "LayerIds": [{"Ref": "DBLayer"}],
        "InstanceType": "m1.small"
      }
    },
    "myApp" : {
      "Type" : "AWS::OpsWorks::App",
      "Properties" : {
        "StackId" : {"Ref":"myStack"},
        "Type" : "php",
        "Name" : {"Ref": "AppName"},
        "AppSource" : {
          "Type" : "git",
          "Url" : "git://github.com/amazonwebservices/opsworks-demo-php-simple-app.git",
          "Revision" : "version2"
        },
        "Attributes" : {
          "DocumentRoot" : "web"
        }
      }
    }
  }
}
```

### YAML<a name="quickref-opsworks-example-1.yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Parameters:
  ServiceRole:
    Default: aws-opsworks-service-role
    Description: The OpsWorks service role
    Type: String
    MinLength: '1'
    MaxLength: '64'
    AllowedPattern: "[a-zA-Z][a-zA-Z0-9-]*"
    ConstraintDescription: must begin with a letter and contain only alphanumeric
      characters.
  InstanceRole:
    Default: aws-opsworks-ec2-role
    Description: The OpsWorks instance role
    Type: String
    MinLength: '1'
    MaxLength: '64'
    AllowedPattern: "[a-zA-Z][a-zA-Z0-9-]*"
    ConstraintDescription: must begin with a letter and contain only alphanumeric
      characters.
  AppName:
    Default: myapp
    Description: The app name
    Type: String
    MinLength: '1'
    MaxLength: '64'
    AllowedPattern: "[a-zA-Z][a-zA-Z0-9]*"
    ConstraintDescription: must begin with a letter and contain only alphanumeric
      characters.
  MysqlRootPassword:
    Description: MysqlRootPassword
    NoEcho: 'true'
    Type: String
Resources:
  myStack:
    Type: AWS::OpsWorks::Stack
    Properties:
      Name:
        Ref: AWS::StackName
      ServiceRoleArn: !Sub "arn:aws:iam::${AWS::AccountId}:role/${ServiceRole}"
      DefaultInstanceProfileArn: !Sub "arn:aws:iam::${AWS::AccountId}:instance-profile/${InstanceRole}"
      UseCustomCookbooks: 'true'
      CustomCookbooksSource:
        Type: git
        Url: git://github.com/amazonwebservices/opsworks-example-cookbooks.git
  myLayer:
    Type: AWS::OpsWorks::Layer
    DependsOn: myApp
    Properties:
      StackId:
        Ref: myStack
      Type: php-app
      Shortname: php-app
      EnableAutoHealing: 'true'
      AutoAssignElasticIps: 'false'
      AutoAssignPublicIps: 'true'
      Name: MyPHPApp
      CustomRecipes:
        Configure:
        - phpapp::appsetup
  DBLayer:
    Type: AWS::OpsWorks::Layer
    DependsOn: myApp
    Properties:
      StackId:
        Ref: myStack
      Type: db-master
      Shortname: db-layer
      EnableAutoHealing: 'true'
      AutoAssignElasticIps: 'false'
      AutoAssignPublicIps: 'true'
      Name: MyMySQL
      CustomRecipes:
        Setup:
        - phpapp::dbsetup
      Attributes:
        MysqlRootPassword:
          Ref: MysqlRootPassword
        MysqlRootPasswordUbiquitous: 'true'
      VolumeConfigurations:
      - MountPoint: "/vol/mysql"
        NumberOfDisks: 1
        Size: 10
  ELBAttachment:
    Type: AWS::OpsWorks::ElasticLoadBalancerAttachment
    Properties:
      ElasticLoadBalancerName:
        Ref: ELB
      LayerId:
        Ref: myLayer
  ELB:
    Type: AWS::ElasticLoadBalancing::LoadBalancer
    Properties:
      AvailabilityZones:
        Fn::GetAZs: ''
      Listeners:
      - LoadBalancerPort: '80'
        InstancePort: '80'
        Protocol: HTTP
        InstanceProtocol: HTTP
      HealthCheck:
        Target: HTTP:80/
        HealthyThreshold: '2'
        UnhealthyThreshold: '10'
        Interval: '30'
        Timeout: '5'
  myAppInstance1:
    Type: AWS::OpsWorks::Instance
    Properties:
      StackId:
        Ref: myStack
      LayerIds:
      - Ref: myLayer
      InstanceType: m1.small
  myAppInstance2:
    Type: AWS::OpsWorks::Instance
    Properties:
      StackId:
        Ref: myStack
      LayerIds:
      - Ref: myLayer
      InstanceType: m1.small
  myDBInstance:
    Type: AWS::OpsWorks::Instance
    Properties:
      StackId:
        Ref: myStack
      LayerIds:
      - Ref: DBLayer
      InstanceType: m1.small
  myApp:
    Type: AWS::OpsWorks::App
    Properties:
      StackId:
        Ref: myStack
      Type: php
      Name:
        Ref: AppName
      AppSource:
        Type: git
        Url: git://github.com/amazonwebservices/opsworks-demo-php-simple-app.git
        Revision: version2
      Attributes:
        DocumentRoot: web
```