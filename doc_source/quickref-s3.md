# Amazon S3 template snippets<a name="quickref-s3"></a>

**Topics**
+ [Creating an Amazon S3 bucket with defaults](#scenario-s3-bucket)
+ [Creating an Amazon S3 bucket for website hosting and with a DeletionPolicy](#scenario-s3-bucket-website)
+ [Creating a static website using a custom domain](#scenario-s3-bucket-website-customdomain)

## Creating an Amazon S3 bucket with defaults<a name="scenario-s3-bucket"></a>

This example uses a [AWS::S3::Bucket](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.html) to create a bucket with default settings\.

### JSON<a name="quickref-s3-example-1.json"></a>

```
1. "myS3Bucket" : {
2.       "Type" : "AWS::S3::Bucket"
3.       }
```

### YAML<a name="quickref-s3-example-1.yaml"></a>

```
1. MyS3Bucket:
2.     Type: AWS::S3::Bucket
```

## Creating an Amazon S3 bucket for website hosting and with a DeletionPolicy<a name="scenario-s3-bucket-website"></a>

This example creates a bucket as a website\. The AccessControl property is set to Private, otherwise the BucketPolicy will fail to be created\. Because this bucket resource has a [DeletionPolicy attribute](aws-attribute-deletionpolicy.md) set to `Retain`, AWS CloudFormation will not delete this bucket when it deletes the stack\. The Output section uses `Fn::GetAtt` to retrieve the WebsiteURL attribute and DomainName attribute of the S3Bucket resource\.

### JSON<a name="quickref-s3-example-2.json"></a>

```
 1. {
 2.     "AWSTemplateFormatVersion": "2010-09-09",
 3.     "Resources": {
 4.         "S3Bucket": {
 5.             "Type": "AWS::S3::Bucket",
 6.             "Properties": {
 7.                 "AccessControl": "Private",
 8.                 "PublicAccessBlockConfiguration": {
 9.                     "BlockPublicPolicy": false
10.                 },
11.                 "WebsiteConfiguration": {
12.                     "IndexDocument": "index.html",
13.                     "ErrorDocument": "error.html"
14.                 }
15.             },
16.             "DeletionPolicy": "Retain"
17.         },
18.         "BucketPolicy": {
19.             "Type": "AWS::S3::BucketPolicy",
20.             "Properties": {
21.                 "PolicyDocument": {
22.                     "Id": "MyPolicy",
23.                     "Version": "2012-10-17",
24.                     "Statement": [
25.                         {
26.                             "Sid": "PublicReadForGetBucketObjects",
27.                             "Effect": "Allow",
28.                             "Principal": "*",
29.                             "Action": "s3:GetObject",
30.                             "Resource": {
31.                                 "Fn::Join": [
32.                                     "",
33.                                     [
34.                                         "arn:aws:s3:::",
35.                                         {
36.                                             "Ref": "S3Bucket"
37.                                         },
38.                                         "/*"
39.                                     ]
40.                                 ]
41.                             }
42.                         }
43.                     ]
44.                 },
45.                 "Bucket": {
46.                     "Ref": "S3Bucket"
47.                 }
48.             }
49.         }
50.     },
51.     "Outputs": {
52.         "WebsiteURL": {
53.             "Value": {
54.                 "Fn::GetAtt": [
55.                     "S3Bucket",
56.                     "WebsiteURL"
57.                 ]
58.             },
59.             "Description": "URL for website hosted on S3"
60.         },
61.         "S3BucketSecureURL": {
62.             "Value": {
63.                 "Fn::Join": [
64.                     "",
65.                     [
66.                         "https://",
67.                         {
68.                             "Fn::GetAtt": [
69.                                 "S3Bucket",
70.                                 "DomainName"
71.                             ]
72.                         }
73.                     ]
74.                 ]
75.             },
76.             "Description": "Name of S3 bucket to hold website content"
77.         }
78.     }
79. }
```

### YAML<a name="quickref-s3-example-2.yaml"></a>

```
 1. AWSTemplateFormatVersion: 2010-09-09
 2. Resources:
 3.   S3Bucket:
 4.     Type: 'AWS::S3::Bucket'
 5.     Properties:
 6.       AccessControl: Private
 7.       PublicAccessBlockConfiguration:
 8.         BlockPublicPolicy: false
 9.       WebsiteConfiguration:
10.         IndexDocument: index.html
11.         ErrorDocument: error.html
12.     DeletionPolicy: Retain
13.   BucketPolicy:
14.     Type: 'AWS::S3::BucketPolicy'
15.     Properties:
16.       PolicyDocument:
17.         Id: MyPolicy
18.         Version: 2012-10-17
19.         Statement:
20.           - Sid: PublicReadForGetBucketObjects
21.             Effect: Allow
22.             Principal: '*'
23.             Action: 's3:GetObject'
24.             Resource: !Join 
25.               - ''
26.               - - 'arn:aws:s3:::'
27.                 - !Ref S3Bucket
28.                 - /*
29.       Bucket: !Ref S3Bucket
30. Outputs:
31.   WebsiteURL:
32.     Value: !GetAtt 
33.       - S3Bucket
34.       - WebsiteURL
35.     Description: URL for website hosted on S3
36.   S3BucketSecureURL:
37.     Value: !Join 
38.       - ''
39.       - - 'https://'
40.         - !GetAtt 
41.           - S3Bucket
42.           - DomainName
43.     Description: Name of S3 bucket to hold website content
```

## Creating a static website using a custom domain<a name="scenario-s3-bucket-website-customdomain"></a>

You can use Route 53 with a registered domain\. The following sample assumes that you have already created a hosted zone in Route 53 for your domain\. The example creates two buckets for website hosting\. The root bucket hosts the content, and the other bucket redirects `www.domainname.com` requests to the root bucket\. The record sets map your domain name to Amazon S3 endpoints\. You will also need to add a bucket policy, as shown in the examples above\.

For more information about using a custom domain, see [Setting up a static website using a custom domain](https://docs.aws.amazon.com/AmazonS3/latest/dev/website-hosting-custom-domain-walkthrough.html) in the *Amazon Simple Storage Service User Guide*\.

### JSON<a name="quickref-s3-example-3.json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Mappings" : {
        "RegionMap" : {
            "us-east-1" : { "S3hostedzoneID" : "Z3AQBSTGFYJSTF", "websiteendpoint" : "s3-website-us-east-1.amazonaws.com" },
            "us-west-1" : { "S3hostedzoneID" : "Z2F56UZL2M1ACD", "websiteendpoint" : "s3-website-us-west-1.amazonaws.com" },
            "us-west-2" : { "S3hostedzoneID" : "Z3BJ6K6RIION7M", "websiteendpoint" : "s3-website-us-west-2.amazonaws.com" },            
            "eu-west-1" : { "S3hostedzoneID" : "Z1BKCTXD74EZPE", "websiteendpoint" : "s3-website-eu-west-1.amazonaws.com" },
            "ap-southeast-1" : { "S3hostedzoneID" : "Z3O0J2DXBE1FTB", "websiteendpoint" : "s3-website-ap-southeast-1.amazonaws.com" },
            "ap-southeast-2" : { "S3hostedzoneID" : "Z1WCIGYICN2BYD", "websiteendpoint" : "s3-website-ap-southeast-2.amazonaws.com" },
            "ap-northeast-1" : { "S3hostedzoneID" : "Z2M4EHUR26P7ZW", "websiteendpoint" : "s3-website-ap-northeast-1.amazonaws.com" },
            "sa-east-1" : { "S3hostedzoneID" : "Z31GFT0UA1I2HV", "websiteendpoint" : "s3-website-sa-east-1.amazonaws.com" }
        }
    },
    "Parameters": {
        "RootDomainName": {
            "Description": "Domain name for your website (example.com)",
            "Type": "String"
        }
    },
    "Resources": {
        "RootBucket": {
            "Type": "AWS::S3::Bucket",
            "Properties": {
                "BucketName" : {"Ref":"RootDomainName"},                
                "AccessControl": "Private",
                "PublicAccessBlockConfiguration": {
                     "BlockPublicPolicy": false
                },
                "WebsiteConfiguration": {
                    "IndexDocument":"index.html",
                    "ErrorDocument":"404.html"
                }
            }
        },
        "WWWBucket": {
            "Type": "AWS::S3::Bucket",
            "Properties": {
                "BucketName": {
                    "Fn::Join": ["", ["www.", {"Ref":"RootDomainName"}]]
                },
                "AccessControl": "BucketOwnerFullControl",
                "WebsiteConfiguration": {
                    "RedirectAllRequestsTo": {
                        "HostName": {"Ref": "RootBucket"}
                    }
                }
            }
        },
        "myDNS": {
            "Type": "AWS::Route53::RecordSetGroup",
            "Properties": {
                "HostedZoneName": {
                    "Fn::Join": ["", [{"Ref": "RootDomainName"}, "."]]
                },
                "Comment": "Zone apex alias.",
                "RecordSets": [
                    {
                        "Name": {"Ref": "RootDomainName"},
                        "Type": "A",
                        "AliasTarget": {
                            "HostedZoneId": {"Fn::FindInMap" : [ "RegionMap", { "Ref" : "AWS::Region" }, "S3hostedzoneID"]},
                            "DNSName": {"Fn::FindInMap" : [ "RegionMap", { "Ref" : "AWS::Region" }, "websiteendpoint"]}
                        }
                    },
                    {
                        "Name": {
                            "Fn::Join": ["", ["www.", {"Ref":"RootDomainName"}]]
                        },
                        "Type": "CNAME",
                        "TTL" : "900",
                        "ResourceRecords" : [
                            {"Fn::GetAtt":["WWWBucket", "DomainName"]}
                        ]
                    }
                ]
            }
        }
    },
    "Outputs": {
        "WebsiteURL": {
            "Value": {"Fn::GetAtt": ["RootBucket", "WebsiteURL"]},
            "Description": "URL for website hosted on S3"
        }
    }
}
```

### YAML<a name="quickref-s3-example-3.yaml"></a>

```
Parameters:
  RootDomainName:
    Description: Domain name for your website (example.com)
    Type: String
Mappings:
  RegionMap:
    us-east-1:
      S3hostedzoneID: Z3AQBSTGFYJSTF
      websiteendpoint: s3-website-us-east-1.amazonaws.com
    us-west-1:
      S3hostedzoneID: Z2F56UZL2M1ACD
      websiteendpoint: s3-website-us-west-1.amazonaws.com
    us-west-2:
      S3hostedzoneID: Z3BJ6K6RIION7M
      websiteendpoint: s3-website-us-west-2.amazonaws.com
    eu-west-1:
      S3hostedzoneID: Z1BKCTXD74EZPE
      websiteendpoint: s3-website-eu-west-1.amazonaws.com
    ap-southeast-1:
      S3hostedzoneID: Z3O0J2DXBE1FTB
      websiteendpoint: s3-website-ap-southeast-1.amazonaws.com
    ap-southeast-2:
      S3hostedzoneID: Z1WCIGYICN2BYD
      websiteendpoint: s3-website-ap-southeast-2.amazonaws.com
    ap-northeast-1:
      S3hostedzoneID: Z2M4EHUR26P7ZW
      websiteendpoint: s3-website-ap-northeast-1.amazonaws.com
    sa-east-1:
      S3hostedzoneID: Z31GFT0UA1I2HV
      websiteendpoint: s3-website-sa-east-1.amazonaws.com
Resources:
  RootBucket:
    Type: AWS::S3::Bucket
    Properties:
      BucketName: !Ref RootDomainName
      AccessControl: Private
      PublicAccessBlockConfiguration:
        BlockPublicPolicy: false
      WebsiteConfiguration:
        IndexDocument: index.html
        ErrorDocument: 404.html
  WWWBucket:
    Type: AWS::S3::Bucket
    Properties:
      BucketName: !Sub
          - www.${Domain}
          - Domain: !Ref RootDomainName
      AccessControl: BucketOwnerFullControl
      WebsiteConfiguration:
        RedirectAllRequestsTo:
          HostName: !Ref RootBucket
  myDNS:
    Type: AWS::Route53::RecordSetGroup
    Properties:
      HostedZoneName: !Sub 
          - ${Domain}.
          - Domain: !Ref RootDomainName
      Comment: Zone apex alias.
      RecordSets:
      - 
        Name: !Ref RootDomainName
        Type: A
        AliasTarget:
          HostedZoneId: !FindInMap [ RegionMap, !Ref 'AWS::Region', S3hostedzoneID]
          DNSName: !FindInMap [ RegionMap, !Ref 'AWS::Region', websiteendpoint]
      -
        Name: !Sub
            - www.${Domain}
            - Domain: !Ref RootDomainName
        Type: CNAME
        TTL: 900
        ResourceRecords:
        - !GetAtt WWWBucket.DomainName
Outputs:
  WebsiteURL:
    Value: !GetAtt RootBucket.WebsiteURL
    Description: URL for website hosted on S3
```
