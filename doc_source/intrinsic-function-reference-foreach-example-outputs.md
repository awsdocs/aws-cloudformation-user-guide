# `Fn::ForEach` in the `Outputs` section<a name="intrinsic-function-reference-foreach-example-outputs"></a>

These examples demonstrate using the `Fn::ForEach` intrinsic function in the [Outputs](outputs-section-structure.md) section\.

**Topics**
+ [Reference replicated [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.htmlAWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.htmlAWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.html) resources](#intrinsic-function-reference-foreach-example-replicate-outputs)
+ [Reference replicated [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html) resources](#intrinsic-function-reference-foreach-example-replicate-conditions)

## Reference replicated [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.htmlAWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.htmlAWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.html) resources<a name="intrinsic-function-reference-foreach-example-replicate-outputs"></a>

This example uses nested `Fn::ForEach` loops in the [Outputs](outputs-section-structure.md) section to reduce the template length\.

### JSON<a name="intrinsic-function-reference-foreach-example-replicate-outputs.json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Transform": "AWS::LanguageExtensions",
  "Resources": {
    "Fn::ForEach::Buckets": [
      "Identifier",
      [ "A", "B", "C" ],
      {
        "S3Bucket${Identifier}": {
          "Type": "AWS::S3::Bucket",
          "Properties": {
            "AccessControl": "PublicRead",
            "MetricsConfigurations": [
              {
                "Id": {"Fn::Sub": "EntireBucket${Identifier}"}
              }
            ],
            "WebsiteConfiguration": {
              "IndexDocument": "index.html",
              "ErrorDocument": "error.html",
              "RoutingRules": [
                {
                  "RoutingRuleCondition": {
                    "HttpErrorCodeReturnedEquals": "404",
                    "KeyPrefixEquals": "out1/"
                  },
                  "RedirectRule": {
                    "HostName": "ec2-11-22-333-44.compute-1.amazonaws.com",
                    "ReplaceKeyPrefixWith": "report-404/"
                  }
                }
              ]
            }
          },
          "DeletionPolicy": "Retain",
          "UpdateReplacePolicy": "Retain"
        }
      }
    ]
  },
  "Outputs": {
    "Fn::ForEach::BucketOutputs": [
      "Identifier",
      [ "A", "B", "C" ],
      {
        "Fn::ForEach::GetAttLoop": [
          "Property",
          [ "Arn", "DomainName", "WebsiteURL" ],
          {
            "S3Bucket${Identifier}${Property}": {
              "Value": {
                "Fn::GetAtt": [
                  {"Fn::Sub": "S3Bucket${Identifier}"},
                  {"Ref": "Property"}
                ]
              }
            }
          }
        ]
      }
    ]
  }
}
```

### YAML<a name="intrinsic-function-reference-foreach-example-outputs.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Transform: 'AWS::LanguageExtensions'
Resources:
  'Fn::ForEach::Buckets':
    - Identifier
    - [A, B, C]
    - 'S3Bucket${Identifier}':
        Type: 'AWS::S3::Bucket'
        Properties:
          AccessControl: PublicRead
          MetricsConfigurations:
            - Id: !Sub 'EntireBucket${Identifier}'
          WebsiteConfiguration:
            IndexDocument: index.html
            ErrorDocument: error.html
            RoutingRules:
              - RoutingRuleCondition:
                  HttpErrorCodeReturnedEquals: '404'
                  KeyPrefixEquals: out1/
                RedirectRule:
                  HostName: ec2-11-22-333-44.compute-1.amazonaws.com
                  ReplaceKeyPrefixWith: report-404/
        DeletionPolicy: Retain
        UpdateReplacePolicy: Retain
Outputs:
  'Fn::ForEach::BucketOutputs':
    - Identifier
    - [A, B, C]
    - 'Fn::ForEach::GetAttLoop':
        - Property
        - [Arn, DomainName, WebsiteURL]
        - 'S3Bucket${Identifier}${Property}':
            Value: !GetAtt [!Sub 'S3Bucket${Identifier}', !Ref Property]
```

The transformed template will be equivalent to the following template:

```
AWSTemplateFormatVersion: 2010-09-09
Transform: 'AWS::LanguageExtensions'
Resources:
  S3BucketA:
    Type: 'AWS::S3::Bucket'
    Properties:
      AccessControl: PublicRead
      MetricsConfigurations:
        - Id: EntireBucketA
      WebsiteConfiguration:
        IndexDocument: index.html
        ErrorDocument: error.html
        RoutingRules:
          - RoutingRuleCondition:
              HttpErrorCodeReturnedEquals: '404'
              KeyPrefixEquals: out1/
            RedirectRule:
              HostName: ec2-11-22-333-44.compute-1.amazonaws.com
              ReplaceKeyPrefixWith: report-404/
    DeletionPolicy: Retain
    UpdateReplacePolicy: Retain
  S3BucketB:
    Type: 'AWS::S3::Bucket'
    Properties:
      AccessControl: PublicRead
      MetricsConfigurations:
        - Id: EntireBucketB
      WebsiteConfiguration:
        IndexDocument: index.html
        ErrorDocument: error.html
        RoutingRules:
          - RoutingRuleCondition:
              HttpErrorCodeReturnedEquals: '404'
              KeyPrefixEquals: out1/
            RedirectRule:
              HostName: ec2-11-22-333-44.compute-1.amazonaws.com
              ReplaceKeyPrefixWith: report-404/
    DeletionPolicy: Retain
    UpdateReplacePolicy: Retain
  S3BucketC:
    Type: 'AWS::S3::Bucket'
    Properties:
      AccessControl: PublicRead
      MetricsConfigurations:
        - Id: EntireBucketC
      WebsiteConfiguration:
        IndexDocument: index.html
        ErrorDocument: error.html
        RoutingRules:
          - RoutingRuleCondition:
              HttpErrorCodeReturnedEquals: '404'
              KeyPrefixEquals: out1/
            RedirectRule:
              HostName: ec2-11-22-333-44.compute-1.amazonaws.com
              ReplaceKeyPrefixWith: report-404/
    DeletionPolicy: Retain
    UpdateReplacePolicy: Retain
Outputs:
  S3BucketAArn:
    Value: !GetAtt [S3BucketA, Arn]
  S3BucketADomainName:
    Value: !GetAtt [S3BucketA, DomainName]
  S3BucketAWebsiteURL:
    Value: !GetAtt [S3BucketA, WebsiteURL]
  S3BucketBArn:
    Value: !GetAtt [S3BucketB, Arn]
  S3BucketBDomainName:
    Value: !GetAtt [S3BucketB, DomainName]
  S3BucketBWebsiteURL:
    Value: !GetAtt [S3BucketB, WebsiteURL]
  S3BucketCArn:
    Value: !GetAtt [S3BucketC, Arn]
  S3BucketCDomainName:
    Value: !GetAtt [S3BucketC, DomainName]
  S3BucketCWebsiteURL:
    Value: !GetAtt [S3BucketC, WebsiteURL]
```

## Reference replicated [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html) resources<a name="intrinsic-function-reference-foreach-example-replicate-conditions"></a>

This example references replicated resources in the [Conditions](outputs-section-structure.md) using the generated Logical IDs\.

### JSON<a name="intrinsic-function-reference-foreach-example-replicate-conditions.json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Transform": "AWS::LanguageExtensions",
  "Mappings": {
    "Instances": {
      "InstanceType": {
        "B": "m5.4xlarge",
        "C": "c5.2xlarge"
      },
      "ImageId": {"A": "ami-id1"}
    }
  },
  "Resources": {
    "Fn::ForEach::Instances": [
      "Identifier",
      [ "A", "B", "C" ],
      {
        "Instance${Identifier}": {
          "Type": "AWS::EC2::Instance",
          "Properties": {
            "InstanceType": {
              "Fn::FindInMap": [
                "Instances",
                "InstanceType",
                {"Ref": "Identifier"},
                {"DefaultValue": "m5.xlarge"}
              ]
            },
            "ImageId": {
              "Fn::FindInMap": [
                "Instances",
                "ImageId",
                {"Ref": "Identifier"},
                {"DefaultValue": "ami-id-default"}
              ]
            }
          }
        }
      }
    ]
  },
  "Outputs": {
    "SecondInstanceId": {
      "Description": "Instance Id for InstanceB",
      "Value": {"Ref": "InstanceB"}
    },
    "SecondPrivateIp": {
      "Description": "Private IP for InstanceB",
      "Value": {
        "Fn::GetAtt": [
          "InstanceB",
          "PrivateIp"
        ]
      }
    }
  }
}
```

### YAML<a name="intrinsic-function-reference-foreach-example-replicate-conditions.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Transform: 'AWS::LanguageExtensions'
Mappings:
  Instances:
    InstanceType:
      B: m5.4xlarge
      C: c5.2xlarge
    ImageId:
      A: ami-id1
Resources:
  'Fn::ForEach::Instances':
    - Identifier
    - [A, B, C]
    - 'Instance${Identifier}':
        Type: 'AWS::EC2::Instance'
        Properties:
          InstanceType: !FindInMap [Instances, InstanceType, !Ref Identifier, DefaultValue: m5.xlarge]
          ImageId: !FindInMap [Instances, ImageId, !Ref Identifier, DefaultValue: ami-id-default]
Outputs:
  SecondInstanceId:
    Description: Instance Id for InstanceB
    Value: !Ref InstanceB
  SecondPrivateIp:
    Description: Private IP for InstanceB
    Value: !GetAtt [InstanceB, PrivateIp]
```

The transformed template will be equivalent to the following template:

```
AWSTemplateFormatVersion: 2010-09-09
Transform: 'AWS::LanguageExtensions'
Resources:
  InstanceA:
    Type: 'AWS::EC2::Instance'
    Properties:
      InstanceType: m5.xlarge
      ImageId: ami-id1
  InstanceB:
    Type: 'AWS::EC2::Instance'
    Properties:
      InstanceType: m5.4xlarge
      ImageId: ami-id-default
  InstanceC:
    Type: 'AWS::EC2::Instance'
    Properties:
      InstanceType: c5.2xlarge
      ImageId: ami-id-default
Outputs:
  SecondInstanceId:
    Description: Instance Id for InstanceB
    Value: !Ref InstanceB
  SecondPrivateIp:
    Description: Private IP for InstanceB
    Value: !GetAtt [InstanceB, PrivateIp]
```