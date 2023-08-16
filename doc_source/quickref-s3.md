# Amazon S3 template snippets<a name="quickref-s3"></a>

**Topics**
+ [Creating an Amazon S3 bucket with defaults](#scenario-s3-bucket)
+ [Creating an Amazon S3 bucket for website hosting and with a `DeletionPolicy`](#scenario-s3-bucket-website)
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

## Creating an Amazon S3 bucket for website hosting and with a `DeletionPolicy`<a name="scenario-s3-bucket-website"></a>

This example creates a bucket as a website\. The `AccessControl` property is set to the canned ACL PublicRead \(public read permissions are required for buckets set up for website hosting\)\. Because this bucket resource has a [DeletionPolicy attribute](aws-attribute-deletionpolicy.md) set to `Retain`, AWS CloudFormation will not delete this bucket when it deletes the stack\. The Output section uses `Fn::GetAtt` to retrieve the `WebsiteURL` attribute and `DomainName` attribute of the `S3Bucket` resource\.

### JSON<a name="quickref-s3-example-2.json"></a>

```
 1. {
 2.     "AWSTemplateFormatVersion": "2010-09-09",
 3.     "Resources": {
 4.         "S3Bucket": {
 5.             "Type": "AWS::S3::Bucket",
 6.             "Properties": {
 7.                 "AccessControl": "PublicRead",
 8.                 "WebsiteConfiguration": {
 9.                     "IndexDocument": "index.html",
10.                     "ErrorDocument": "error.html"
11.                 }
12.             },
13.             "DeletionPolicy": "Retain",
14.             "UpdateReplacePolicy": "Retain"
15.         },
16.         "BucketPolicy": {
17.             "Type": "AWS::S3::BucketPolicy",
18.             "Properties": {
19.                 "PolicyDocument": {
20.                     "Id": "MyPolicy",
21.                     "Version": "2012-10-17",
22.                     "Statement": [
23.                         {
24.                             "Sid": "PublicReadForGetBucketObjects",
25.                             "Effect": "Allow",
26.                             "Principal": "*",
27.                             "Action": "s3:GetObject",
28.                             "Resource": {
29.                                 "Fn::Join": [
30.                                     "",
31.                                     [
32.                                         "arn:aws:s3:::",
33.                                         {
34.                                             "Ref": "S3Bucket"
35.                                         },
36.                                         "/*"
37.                                     ]
38.                                 ]
39.                             }
40.                         }
41.                     ]
42.                 },
43.                 "Bucket": {
44.                     "Ref": "S3Bucket"
45.                 }
46.             }
47.         }
48.     },
49.     "Outputs": {
50.         "WebsiteURL": {
51.             "Value": {
52.                 "Fn::GetAtt": [
53.                     "S3Bucket",
54.                     "WebsiteURL"
55.                 ]
56.             },
57.             "Description": "URL for website hosted on S3"
58.         },
59.         "S3BucketSecureURL": {
60.             "Value": {
61.                 "Fn::Join": [
62.                     "",
63.                     [
64.                         "https://",
65.                         {
66.                             "Fn::GetAtt": [
67.                                 "S3Bucket",
68.                                 "DomainName"
69.                             ]
70.                         }
71.                     ]
72.                 ]
73.             },
74.             "Description": "Name of S3 bucket to hold website content"
75.         }
76.     }
77. }
```

### YAML<a name="quickref-s3-example-2.yaml"></a>

```
 1. AWSTemplateFormatVersion: 2010-09-09
 2. Resources:
 3.   S3Bucket:
 4.     Type: 'AWS::S3::Bucket'
 5.     Properties:
 6.       AccessControl: PublicRead
 7.       WebsiteConfiguration:
 8.         IndexDocument: index.html
 9.         ErrorDocument: error.html
10.     DeletionPolicy: Retain
11.     UpdateReplacePolicy: Retain
12.   BucketPolicy:
13.     Type: 'AWS::S3::BucketPolicy'
14.     Properties:
15.       PolicyDocument:
16.         Id: MyPolicy
17.         Version: 2012-10-17
18.         Statement:
19.           - Sid: PublicReadForGetBucketObjects
20.             Effect: Allow
21.             Principal: '*'
22.             Action: 's3:GetObject'
23.             Resource: !Join 
24.               - ''
25.               - - 'arn:aws:s3:::'
26.                 - !Ref S3Bucket
27.                 - /*
28.       Bucket: !Ref S3Bucket
29. Outputs:
30.   WebsiteURL:
31.     Value: !GetAtt 
32.       - S3Bucket
33.       - WebsiteURL
34.     Description: URL for website hosted on S3
35.   S3BucketSecureURL:
36.     Value: !Join 
37.       - ''
38.       - - 'https://'
39.         - !GetAtt 
40.           - S3Bucket
41.           - DomainName
42.     Description: Name of S3 bucket to hold website content
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
                "AccessControl": "PublicRead",
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
      AccessControl: PublicRead
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