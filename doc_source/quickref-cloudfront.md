# Amazon CloudFront template snippets<a name="quickref-cloudfront"></a>

**Topics**
+ [Amazon CloudFront distribution resource with an Amazon S3 origin](#scenario-cloudfront-s3origin)
+ [Amazon CloudFront distribution resource with custom origin](#scenario-cloudfront-customorigin)
+ [Amazon CloudFront distribution with multi\-origin support\.](#scenario-cloudfront-multiorigin)

## Amazon CloudFront distribution resource with an Amazon S3 origin<a name="scenario-cloudfront-s3origin"></a>

The following example template shows an Amazon CloudFront [Distribution](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudfront-distribution.html) using an [S3Origin](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cloudfront-distribution-s3originconfig.html)\.

### JSON<a name="quickref-cloudfront-example-1.json"></a>

```
 1. {
 2.     "AWSTemplateFormatVersion" : "2010-09-09",
 3.     "Resources" : {
 4.         "myDistribution" : {
 5.             "Type" : "AWS::CloudFront::Distribution",
 6.             "Properties" : {
 7.                 "DistributionConfig" : {
 8.                     "Origins" : [ {
 9.                         "DomainName" : "mybucket.s3.amazonaws.com",
10.                         "Id" : "myS3Origin",
11.                         "S3OriginConfig" : {
12.                             "OriginAccessIdentity" : "origin-access-identity/cloudfront/E127EXAMPLE51Z"
13.                         }
14.                     }],
15.                     "Enabled" : "true",
16.                     "Comment" : "Some comment",
17.                     "DefaultRootObject" : "index.html",
18.                     "Logging" : {
19.                         "IncludeCookies" : "false",
20.                         "Bucket" : "mylogs.s3.amazonaws.com",
21.                         "Prefix" : "myprefix"
22.                     },
23.                     "Aliases" : [ "mysite.example.com", "yoursite.example.com" ],
24.                     "DefaultCacheBehavior" : {
25.                         "AllowedMethods" : [ "DELETE", "GET", "HEAD", "OPTIONS", "PATCH", "POST", "PUT" ],  
26.                         "TargetOriginId" : "myS3Origin",
27.                         "ForwardedValues" : {
28.                             "QueryString" : "false",
29.                             "Cookies" : { "Forward" : "none" }
30.                         },
31.                         "TrustedSigners" : [ "1234567890EX", "1234567891EX" ],
32.                         "ViewerProtocolPolicy" : "allow-all"
33.                     },
34.                    "PriceClass" : "PriceClass_200",
35.                    "Restrictions" : {
36.                        "GeoRestriction" : {
37.                            "RestrictionType" : "whitelist",
38.                            "Locations" : [ "AQ", "CV" ]
39.                        }
40.                    },
41.                    "ViewerCertificate" : { "CloudFrontDefaultCertificate" : "true" }  
42.                 }
43.             }
44.         }
45.     }
46. }
```

### YAML<a name="quickref-cloudfront-example-1.yaml"></a>

```
 1. AWSTemplateFormatVersion: '2010-09-09'
 2. Resources:
 3.   myDistribution:
 4.     Type: AWS::CloudFront::Distribution
 5.     Properties:
 6.       DistributionConfig:
 7.         Origins:
 8.         - DomainName: mybucket.s3.amazonaws.com
 9.           Id: myS3Origin
10.           S3OriginConfig:
11.             OriginAccessIdentity: origin-access-identity/cloudfront/E127EXAMPLE51Z
12.         Enabled: 'true'
13.         Comment: Some comment
14.         DefaultRootObject: index.html
15.         Logging:
16.           IncludeCookies: 'false'
17.           Bucket: mylogs.s3.amazonaws.com
18.           Prefix: myprefix
19.         Aliases:
20.         - mysite.example.com
21.         - yoursite.example.com
22.         DefaultCacheBehavior:
23.           AllowedMethods:
24.           - DELETE
25.           - GET
26.           - HEAD
27.           - OPTIONS
28.           - PATCH
29.           - POST
30.           - PUT
31.           TargetOriginId: myS3Origin
32.           ForwardedValues:
33.             QueryString: 'false'
34.             Cookies:
35.               Forward: none
36.           TrustedSigners:
37.           - 1234567890EX
38.           - 1234567891EX
39.           ViewerProtocolPolicy: allow-all
40.         PriceClass: PriceClass_200
41.         Restrictions:
42.           GeoRestriction:
43.             RestrictionType: whitelist
44.             Locations:
45.             - AQ
46.             - CV
47.         ViewerCertificate:
48.           CloudFrontDefaultCertificate: 'true'
```

## Amazon CloudFront distribution resource with custom origin<a name="scenario-cloudfront-customorigin"></a>

The following example template shows an Amazon CloudFront [Distribution](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudfront-distribution.html) using a [CustomOrigin](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cloudfront-distribution-customoriginconfig.html)\.

### JSON<a name="quickref-cloudfront-example-2.json"></a>

```
 1. {
 2.     "AWSTemplateFormatVersion" : "2010-09-09",
 3.     "Resources" : {
 4.         "myDistribution" : {
 5.             "Type" : "AWS::CloudFront::Distribution",
 6.             "Properties" : {
 7.                 "DistributionConfig" : {
 8.                     "Origins" : [ {
 9.                             "DomainName" : "www.example.com",
10.                             "Id" : "myCustomOrigin",
11.                             "CustomOriginConfig" : {
12.                                 "HTTPPort" : "80",
13.                                 "HTTPSPort" : "443",
14.                                 "OriginProtocolPolicy" : "http-only"
15.                             }
16.                     } ],
17.                     "Enabled" : "true",
18.                     "Comment" : "Somecomment",
19.                     "DefaultRootObject" : "index.html",
20.                     "Logging" : {
21.                         "IncludeCookies" : "true",
22.                         "Bucket" : "mylogs.s3.amazonaws.com",
23.                         "Prefix": "myprefix"
24.                     },
25.                     "Aliases" : [
26.                         "mysite.example.com",
27.                         "*.yoursite.example.com"
28.                     ],
29.                     "DefaultCacheBehavior" : {
30.                         "TargetOriginId" : "myCustomOrigin",
31.                         "SmoothStreaming" : "false",  
32.                         "ForwardedValues" : {
33.                             "QueryString" : "false",
34.                             "Cookies" : { "Forward" : "all" }
35.                         },
36.                         "TrustedSigners" : [
37.                             "1234567890EX",
38.                             "1234567891EX"
39.                         ],
40.                         "ViewerProtocolPolicy" : "allow-all"
41.                     },
42.                     "CustomErrorResponses" : [ {
43.                         "ErrorCode" : "404",
44.                         "ResponsePagePath" : "/error-pages/404.html",
45.                         "ResponseCode" : "200",
46.                         "ErrorCachingMinTTL" : "30"
47.                     } ],
48.                    "PriceClass" : "PriceClass_200",
49.                    "Restrictions" : {
50.                        "GeoRestriction" : {
51.                            "RestrictionType" : "whitelist",
52.                            "Locations" : [ "AQ", "CV" ]
53.                        }
54.                    },
55.                    "ViewerCertificate": { "CloudFrontDefaultCertificate" : "true" }
56.                 }
57.             }
58.         }
59.     }
60. }
```

### YAML<a name="quickref-cloudfront-example-2.yaml"></a>

```
 1. AWSTemplateFormatVersion: '2010-09-09'
 2. Resources:
 3.   myDistribution:
 4.     Type: 'AWS::CloudFront::Distribution'
 5.     Properties:
 6.       DistributionConfig:
 7.         Origins:
 8.         - DomainName: www.example.com
 9.           Id: myCustomOrigin
10.           CustomOriginConfig:
11.             HTTPPort: '80'
12.             HTTPSPort: '443'
13.             OriginProtocolPolicy: http-only
14.         Enabled: 'true'
15.         Comment: Somecomment
16.         DefaultRootObject: index.html
17.         Logging:
18.           IncludeCookies: 'true'
19.           Bucket: mylogs.s3.amazonaws.com
20.           Prefix: myprefix
21.         Aliases:
22.         - mysite.example.com
23.         - "*.yoursite.example.com"
24.         DefaultCacheBehavior:
25.           TargetOriginId: myCustomOrigin
26.           SmoothStreaming: 'false'
27.           ForwardedValues:
28.             QueryString: 'false'
29.             Cookies:
30.               Forward: all
31.           TrustedSigners:
32.           - 1234567890EX
33.           - 1234567891EX
34.           ViewerProtocolPolicy: allow-all
35.         CustomErrorResponses:
36.         - ErrorCode: '404'
37.           ResponsePagePath: "/error-pages/404.html"
38.           ResponseCode: '200'
39.           ErrorCachingMinTTL: '30'
40.         PriceClass: PriceClass_200
41.         Restrictions:
42.           GeoRestriction:
43.             RestrictionType: whitelist
44.             Locations:
45.             - AQ
46.             - CV
47.         ViewerCertificate:
48.           CloudFrontDefaultCertificate: 'true'
```

## Amazon CloudFront distribution with multi\-origin support\.<a name="scenario-cloudfront-multiorigin"></a>

The following example template shows how to declare a CloudFront [Distribution](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudfront-distribution.html) with multi\-origin support\. In the [DistributionConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cloudfront-distribution-distributionconfig.html), a list of origins is provided and a [DefaultCacheBehavior](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cloudfront-distribution-defaultcachebehavior.html) is set\.

### JSON<a name="quickref-cloudfront-example-3.json"></a>

```
{
    "AWSTemplateFormatVersion" : "2010-09-09",
    "Resources" : {
        "myDistribution" : {
            "Type" : "AWS::CloudFront::Distribution",
            "Properties" : {
                "DistributionConfig" : {
                    "Origins" : [ {
                        "Id" : "myS3Origin",
                        "DomainName" : "mybucket.s3.amazonaws.com",
                        "S3OriginConfig" : {
                            "OriginAccessIdentity" : "origin-access-identity/cloudfront/E127EXAMPLE51Z"
                        }
                     }, 
                     {
                         "Id" : "myCustomOrigin",
                         "DomainName" : "www.example.com",
                         "CustomOriginConfig" : {
                             "HTTPPort" : "80",
                             "HTTPSPort" : "443",
                             "OriginProtocolPolicy" : "http-only"
                         }
                     }
                   ],
                   "Enabled" : "true",
                   "Comment" : "Some comment",
                   "DefaultRootObject" : "index.html", 
                   "Logging" : {
                       "IncludeCookies" : "true",
                       "Bucket" : "mylogs.s3.amazonaws.com",
                       "Prefix" : "myprefix"
                   },            
                   "Aliases" : [ "mysite.example.com", "yoursite.example.com" ],
                   "DefaultCacheBehavior" : {
                       "TargetOriginId" : "myS3Origin",
                       "ForwardedValues" : {
                           "QueryString" : "false",
                           "Cookies" : { "Forward" : "all" }
                        },
                       "TrustedSigners" : [ "1234567890EX", "1234567891EX"  ],
                       "ViewerProtocolPolicy" : "allow-all",
                       "MinTTL" : "100",
                       "SmoothStreaming" : "true"
                   },
                   "CacheBehaviors" : [ {
                            "AllowedMethods" : [ "DELETE", "GET", "HEAD", "OPTIONS", "PATCH", "POST", "PUT" ],  
                            "TargetOriginId" : "myS3Origin",
                            "ForwardedValues" : {
                                "QueryString" : "true",
                                "Cookies" : { "Forward" : "none" }
                            },
                            "TrustedSigners" : [ "1234567890EX", "1234567891EX" ],
                            "ViewerProtocolPolicy" : "allow-all",
                            "MinTTL" : "50",
                            "PathPattern" : "images1/*.jpg"
                        }, 
                        {
                            "AllowedMethods" : [ "DELETE", "GET", "HEAD", "OPTIONS", "PATCH", "POST", "PUT" ],  
                            "TargetOriginId" : "myCustomOrigin",
                            "ForwardedValues" : {
                                "QueryString" : "true",
                                "Cookies" : { "Forward" : "none" }
                            },
                            "TrustedSigners" : [ "1234567890EX", "1234567891EX"  ],
                            "ViewerProtocolPolicy" : "allow-all",
                            "MinTTL" : "50",
                            "PathPattern" : "images2/*.jpg"
                        }
                   ],
                   "CustomErrorResponses" : [ {
                       "ErrorCode" : "404",
                       "ResponsePagePath" : "/error-pages/404.html",
                       "ResponseCode" : "200",
                       "ErrorCachingMinTTL" : "30"
                   } ],
                   "PriceClass" : "PriceClass_All",
                   "ViewerCertificate" : { "CloudFrontDefaultCertificate" : "true" }
                }
            }
        }
    }
}
```

### YAML<a name="quickref-cloudfront-example-3.yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Resources:
  myDistribution:
    Type: AWS::CloudFront::Distribution
    Properties:
      DistributionConfig:
        Origins:
        - Id: myS3Origin
          DomainName: mybucket.s3.amazonaws.com
          S3OriginConfig:
            OriginAccessIdentity: origin-access-identity/cloudfront/E127EXAMPLE51Z
        - Id: myCustomOrigin
          DomainName: www.example.com
          CustomOriginConfig:
            HTTPPort: '80'
            HTTPSPort: '443'
            OriginProtocolPolicy: http-only
        Enabled: 'true'
        Comment: Some comment
        DefaultRootObject: index.html
        Logging:
          IncludeCookies: 'true'
          Bucket: mylogs.s3.amazonaws.com
          Prefix: myprefix
        Aliases:
        - mysite.example.com
        - yoursite.example.com
        DefaultCacheBehavior:
          TargetOriginId: myS3Origin
          ForwardedValues:
            QueryString: 'false'
            Cookies:
              Forward: all
          TrustedSigners:
          - 1234567890EX
          - 1234567891EX
          ViewerProtocolPolicy: allow-all
          MinTTL: '100'
          SmoothStreaming: 'true'
        CacheBehaviors:
        - AllowedMethods:
          - DELETE
          - GET
          - HEAD
          - OPTIONS
          - PATCH
          - POST
          - PUT
          TargetOriginId: myS3Origin
          ForwardedValues:
            QueryString: 'true'
            Cookies:
              Forward: none
          TrustedSigners:
          - 1234567890EX
          - 1234567891EX
          ViewerProtocolPolicy: allow-all
          MinTTL: '50'
          PathPattern: images1/*.jpg
        - AllowedMethods:
          - DELETE
          - GET
          - HEAD
          - OPTIONS
          - PATCH
          - POST
          - PUT
          TargetOriginId: myCustomOrigin
          ForwardedValues:
            QueryString: 'true'
            Cookies:
              Forward: none
          TrustedSigners:
          - 1234567890EX
          - 1234567891EX
          ViewerProtocolPolicy: allow-all
          MinTTL: '50'
          PathPattern: images2/*.jpg
        CustomErrorResponses:
        - ErrorCode: '404'
          ResponsePagePath: "/error-pages/404.html"
          ResponseCode: '200'
          ErrorCachingMinTTL: '30'
        PriceClass: PriceClass_All
        ViewerCertificate:
          CloudFrontDefaultCertificate: 'true'
```