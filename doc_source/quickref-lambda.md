# AWS Lambda Template<a name="quickref-lambda"></a>

## <a name="w3ab2c17c24c65b3"></a>

The following template uses an AWS Lambda \(Lambda\) function and custom resource to append a new security group to a list of existing security groups\. This function is useful when you want to build a list of security groups dynamically, so that your list includes both new and existing security groups\. For example, you can pass a list of existing security groups as a parameter value, append the new value to the list, and then associate all your values with an EC2 instance\. For more information about the Lambda function resource type, see [AWS::Lambda::Function](aws-resource-lambda-function.md)\.

In the example, when AWS CloudFormation creates the `AllSecurityGroups` custom resource, AWS CloudFormation invokes the `AppendItemToListFunction` Lambda function\. AWS CloudFormation passes the list of existing security groups and a new security group \(`NewSecurityGroup`\) to the function, which appends the new security group to the list and then returns the modified list\. AWS CloudFormation uses the modified list to associate all security groups with the `MyEC2Instance` resource\.

## JSON<a name="quickref-lambda-example-1.json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Parameters" : {
    "ExistingSecurityGroups" : {
      "Type" : "List<AWS::EC2::SecurityGroup::Id>"
    },
    "ExistingVPC" : {
      "Type" : "AWS::EC2::VPC::Id",
      "Description" : "The VPC ID that includes the security groups in the ExistingSecurityGroups parameter."
    },
    "InstanceType" : {
      "Type" : "String",
      "Default" : "t2.micro",
      "AllowedValues" : ["t2.micro", "m1.small"]
    }
  },
  "Mappings": {
    "AWSInstanceType2Arch" : {
      "t2.micro"    : { "Arch" : "HVM64"  },
      "m1.small"    : { "Arch" : "PV64"   }
    },
    "AWSRegionArch2AMI" : {
      "us-east-1"        : {"PV64" : "ami-1ccae774", "HVM64" : "ami-1ecae776"},
      "us-west-2"        : {"PV64" : "ami-ff527ecf", "HVM64" : "ami-e7527ed7"},
      "us-west-1"        : {"PV64" : "ami-d514f291", "HVM64" : "ami-d114f295"},
      "eu-west-1"        : {"PV64" : "ami-bf0897c8", "HVM64" : "ami-a10897d6"},
      "eu-central-1"     : {"PV64" : "ami-ac221fb1", "HVM64" : "ami-a8221fb5"},
      "ap-northeast-1"   : {"PV64" : "ami-27f90e27", "HVM64" : "ami-cbf90ecb"},
      "ap-southeast-1"   : {"PV64" : "ami-acd9e8fe", "HVM64" : "ami-68d8e93a"},
      "ap-southeast-2"   : {"PV64" : "ami-ff9cecc5", "HVM64" : "ami-fd9cecc7"},
      "sa-east-1"        : {"PV64" : "ami-bb2890a6", "HVM64" : "ami-b52890a8"},
      "cn-north-1"       : {"PV64" : "ami-fa39abc3", "HVM64" : "ami-f239abcb"}
    }
  },
  "Resources" : {
    "SecurityGroup" : {
      "Type" : "AWS::EC2::SecurityGroup",
      "Properties" : {
        "GroupDescription" : "Allow HTTP traffic to the host",
        "VpcId" : {"Ref" : "ExistingVPC"},
        "SecurityGroupIngress" : [{
          "IpProtocol" : "tcp",
          "FromPort" : "80",
          "ToPort" : "80",
          "CidrIp" : "0.0.0.0/0"
        }],
        "SecurityGroupEgress" : [{
          "IpProtocol" : "tcp",
          "FromPort" : "80",
          "ToPort" : "80",
          "CidrIp" : "0.0.0.0/0"
        }]
      }
    },
    "AllSecurityGroups": {
      "Type": "Custom::Split",
      "Properties": {
        "ServiceToken": { "Fn::GetAtt" : ["AppendItemToListFunction", "Arn"] },
        "List": { "Ref" : "ExistingSecurityGroups" },
        "AppendedItem": { "Ref" : "SecurityGroup" }
      }
    },
    "AppendItemToListFunction": {
      "Type": "AWS::Lambda::Function",
      "Properties": {
        "Handler": "index.handler",
        "Role": { "Fn::GetAtt" : ["LambdaExecutionRole", "Arn"] },
        "Code": {
          "ZipFile":  { "Fn::Join": ["", [
            "var response = require('cfn-response');",
            "exports.handler = function(event, context) {",
            "   var responseData = {Value: event.ResourceProperties.List};",
            "   responseData.Value.push(event.ResourceProperties.AppendedItem);",
            "   response.send(event, context, response.SUCCESS, responseData);",
            "};"
          ]]}
        },
        "Runtime": "nodejs4.3"
      }
    },
    "MyEC2Instance" : {
      "Type" : "AWS::EC2::Instance",
      "Properties" : {
        "ImageId": { "Fn::FindInMap": [ "AWSRegionArch2AMI", { "Ref": "AWS::Region" }, { "Fn::FindInMap": [
          "AWSInstanceType2Arch", { "Ref": "InstanceType" }, "Arch" ] } ]
        },
        "SecurityGroupIds" : { "Fn::GetAtt": [ "AllSecurityGroups", "Value" ] },
        "InstanceType" : { "Ref" : "InstanceType" }
      }
    },
    "LambdaExecutionRole": {
      "Type": "AWS::IAM::Role",
      "Properties": {
        "AssumeRolePolicyDocument": {
          "Version": "2012-10-17",
          "Statement": [{ "Effect": "Allow", "Principal": {"Service": ["lambda.amazonaws.com"]}, "Action": ["sts:AssumeRole"] }]
        },
        "Path": "/",
        "Policies": [{
          "PolicyName": "root",
          "PolicyDocument": {
            "Version": "2012-10-17",
            "Statement": [{ "Effect": "Allow", "Action": ["logs:*"], "Resource": "arn:aws:logs:*:*:*" }]
          }
        }]
      }
    }
  },
  "Outputs" : {
    "AllSecurityGroups" : {
      "Description" : "Security Groups that are associated with the EC2 instance",
      "Value" : { "Fn::Join" : [ ", ", { "Fn::GetAtt": [ "AllSecurityGroups", "Value" ] }]}
    }
  }
}
```

## YAML<a name="quickref-lambda-example-1.yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Parameters:
  ExistingSecurityGroups:
    Type: List<AWS::EC2::SecurityGroup::Id>
  ExistingVPC:
    Type: AWS::EC2::VPC::Id
    Description: The VPC ID that includes the security groups in the ExistingSecurityGroups
      parameter.
  InstanceType:
    Type: String
    Default: t2.micro
    AllowedValues:
    - t2.micro
    - m1.small
Mappings:
  AWSInstanceType2Arch:
    t2.micro:
      Arch: HVM64
    m1.small:
      Arch: PV64
  AWSRegionArch2AMI:
    us-east-1:
      PV64: ami-1ccae774
      HVM64: ami-1ecae776
    us-west-2:
      PV64: ami-ff527ecf
      HVM64: ami-e7527ed7
    us-west-1:
      PV64: ami-d514f291
      HVM64: ami-d114f295
    eu-west-1:
      PV64: ami-bf0897c8
      HVM64: ami-a10897d6
    eu-central-1:
      PV64: ami-ac221fb1
      HVM64: ami-a8221fb5
    ap-northeast-1:
      PV64: ami-27f90e27
      HVM64: ami-cbf90ecb
    ap-southeast-1:
      PV64: ami-acd9e8fe
      HVM64: ami-68d8e93a
    ap-southeast-2:
      PV64: ami-ff9cecc5
      HVM64: ami-fd9cecc7
    sa-east-1:
      PV64: ami-bb2890a6
      HVM64: ami-b52890a8
    cn-north-1:
      PV64: ami-fa39abc3
      HVM64: ami-f239abcb
Resources:
  SecurityGroup:
    Type: AWS::EC2::SecurityGroup
    Properties:
      GroupDescription: Allow HTTP traffic to the host
      VpcId:
        Ref: ExistingVPC
      SecurityGroupIngress:
      - IpProtocol: tcp
        FromPort: '80'
        ToPort: '80'
        CidrIp: 0.0.0.0/0
      SecurityGroupEgress:
      - IpProtocol: tcp
        FromPort: '80'
        ToPort: '80'
        CidrIp: 0.0.0.0/0
  AllSecurityGroups:
    Type: Custom::Split
    Properties:
      ServiceToken: !GetAtt AppendItemToListFunction.Arn
      List:
        Ref: ExistingSecurityGroups
      AppendedItem:
        Ref: SecurityGroup
  AppendItemToListFunction:
    Type: AWS::Lambda::Function
    Properties:
      Handler: index.handler
      Role: !GetAtt LambdaExecutionRole.Arn
      Code:
        ZipFile: !Sub |
          var response = require('cfn-response');
          exports.handler = function(event, context) {
             var responseData = {Value: event.ResourceProperties.List};
             responseData.Value.push(event.ResourceProperties.AppendedItem);
             response.send(event, context, response.SUCCESS, responseData);
          };
      Runtime: nodejs4.3
  MyEC2Instance:
    Type: AWS::EC2::Instance
    Properties:
      ImageId:
        Fn::FindInMap:
        - AWSRegionArch2AMI
        - Ref: AWS::Region
        - Fn::FindInMap:
          - AWSInstanceType2Arch
          - Ref: InstanceType
          - Arch
      SecurityGroupIds: !GetAtt AllSecurityGroups.Value
      InstanceType:
        Ref: InstanceType
  LambdaExecutionRole:
    Type: AWS::IAM::Role
    Properties:
      AssumeRolePolicyDocument:
        Version: '2012-10-17'
        Statement:
        - Effect: Allow
          Principal:
            Service:
            - lambda.amazonaws.com
          Action:
          - sts:AssumeRole
      Path: "/"
      Policies:
      - PolicyName: root
        PolicyDocument:
          Version: '2012-10-17'
          Statement:
          - Effect: Allow
            Action:
            - logs:*
            Resource: arn:aws:logs:*:*:*
Outputs:
  AllSecurityGroups:
    Description: Security Groups that are associated with the EC2 instance
    Value:
      Fn::Join:
      - ", "
      - Fn::GetAtt:
        - AllSecurityGroups
        - Value
```