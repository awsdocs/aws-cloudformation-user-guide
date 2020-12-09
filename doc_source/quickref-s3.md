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

This example creates a bucket as a website\. The AccessControl property is set to the canned ACL PublicRead \(public read permissions are required for buckets set up for website hosting\)\. Because this bucket resource has a [DeletionPolicy attribute](aws-attribute-deletionpolicy.md) set to `Retain`, AWS CloudFormation will not delete this bucket when it deletes the stack\. The Output section uses `Fn::GetAtt` to retrieve the WebsiteURL attribute and DomainName attribute of the S3Bucket resource\.

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
13.             "DeletionPolicy": "Retain"
14.         },
15.         "BucketPolicy": {
16.             "Type": "AWS::S3::BucketPolicy",
17.             "Properties": {
18.                 "PolicyDocument": {
19.                     "Id": "MyPolicy",
20.                     "Version": "2012-10-17",
21.                     "Statement": [
22.                         {
23.                             "Sid": "PublicReadForGetBucketObjects",
24.                             "Effect": "Allow",
25.                             "Principal": "*",
26.                             "Action": "s3:GetObject",
27.                             "Resource": {
28.                                 "Fn::Join": [
29.                                     "",
30.                                     [
31.                                         "arn:aws:s3:::",
32.                                         {
33.                                             "Ref": "S3Bucket"
34.                                         },
35.                                         "/*"
36.                                     ]
37.                                 ]
38.                             }
39.                         }
40.                     ]
41.                 },
42.                 "Bucket": {
43.                     "Ref": "S3Bucket"
44.                 }
45.             }
46.         }
47.     },
48.     "Outputs": {
49.         "WebsiteURL": {
50.             "Value": {
51.                 "Fn::GetAtt": [
52.                     "S3Bucket",
53.                     "WebsiteURL"
54.                 ]
55.             },
56.             "Description": "URL for website hosted on S3"
57.         },
58.         "S3BucketSecureURL": {
59.             "Value": {
60.                 "Fn::Join": [
61.                     "",
62.                     [
63.                         "https://",
64.                         {
65.                             "Fn::GetAtt": [
66.                                 "S3Bucket",
67.                                 "DomainName"
68.                             ]
69.                         }
70.                     ]
71.                 ]
72.             },
73.             "Description": "Name of S3 bucket to hold website content"
74.         }
75.     }
76. }
```

### YAML<a name="quickref-s3-example-2.yaml"></a>

```
 1. AWSTemplateFormatVersion: 2010-09-09
 2. Resources:
 3.   S3Bucket:
 4.     Type: AWS::S3::Bucket
 5.     Properties:
 6.       AccessControl: PublicRead
 7.       WebsiteConfiguration:
 8.         IndexDocument: index.html
 9.         ErrorDocument: error.html
10.     DeletionPolicy: Retain
11.   BucketPolicy:
12.     Type: AWS::S3::BucketPolicy
13.     Properties:
14.       PolicyDocument:
15.         Id: MyPolicy
16.         Version: 2012-10-17
17.         Statement:
18.           - Sid: PublicReadForGetBucketObjects
19.             Effect: Allow
20.             Principal: '*'
21.             Action: 's3:GetObject'
22.             Resource: !Join 
23.               - ''
24.               - - 'arn:aws:s3:::'
25.                 - !Ref S3Bucket
26.                 - /*
27.       Bucket: !Ref S3Bucket
28. Outputs:
29.   WebsiteURL:
30.     Value: !GetAtt 
31.       - S3Bucket
32.       - WebsiteURL
33.     Description: URL for website hosted on S3
34.   S3BucketSecureURL:
35.     Value: !Join 
36.       - ''
37.       - - 'https://'
38.         - !GetAtt 
39.           - S3Bucket
40.           - DomainName
41.     Description: Name of S3 bucket to hold website content
```

## Creating a static website using a custom domain<a name="scenario-s3-bucket-website-customdomain"></a>

You can use Route 53 with a registered domain\. The following sample assumes that you have already created a hosted zone in Route 53 for your domain\. The example creates two buckets for website hosting\. The root bucket hosts the content, and the other bucket redirects `www.domainname.com` requests to the root bucket\. The record sets map your domain name to Amazon S3 endpoints\. Note that you will also need to add a bucket policy, as shown in the examples above\.

For more information about using a custom domain, see [Setting up a static website using a custom domain](https://docs.aws.amazon.com/AmazonS3/latest/dev/website-hosting-custom-domain-walkthrough.html) in the *Amazon Simple Storage Service Developer Guide*\.

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