# AWS::S3::Bucket RedirectRule<a name="aws-properties-s3-bucket-redirectrule"></a>

Specifies how requests are redirected\. In the event of an error, you can specify a different error code to return\.

## Syntax<a name="aws-properties-s3-bucket-redirectrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-redirectrule-syntax.json"></a>

```
{
  "[HostName](#cfn-s3-bucket-redirectrule-hostname)" : String,
  "[HttpRedirectCode](#cfn-s3-bucket-redirectrule-httpredirectcode)" : String,
  "[Protocol](#cfn-s3-bucket-redirectrule-protocol)" : String,
  "[ReplaceKeyPrefixWith](#cfn-s3-bucket-redirectrule-replacekeyprefixwith)" : String,
  "[ReplaceKeyWith](#cfn-s3-bucket-redirectrule-replacekeywith)" : String
}
```

### YAML<a name="aws-properties-s3-bucket-redirectrule-syntax.yaml"></a>

```
  [HostName](#cfn-s3-bucket-redirectrule-hostname): String
  [HttpRedirectCode](#cfn-s3-bucket-redirectrule-httpredirectcode): String
  [Protocol](#cfn-s3-bucket-redirectrule-protocol): String
  [ReplaceKeyPrefixWith](#cfn-s3-bucket-redirectrule-replacekeyprefixwith): String
  [ReplaceKeyWith](#cfn-s3-bucket-redirectrule-replacekeywith): String
```

## Properties<a name="aws-properties-s3-bucket-redirectrule-properties"></a>

`HostName`  <a name="cfn-s3-bucket-redirectrule-hostname"></a>
The host name to use in the redirect request\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HttpRedirectCode`  <a name="cfn-s3-bucket-redirectrule-httpredirectcode"></a>
The HTTP redirect code to use on the response\. Not required if one of the siblings is present\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Protocol`  <a name="cfn-s3-bucket-redirectrule-protocol"></a>
Protocol to use when redirecting requests\. The default is the protocol that is used in the original request\.  
*Required*: No  
*Type*: String  
*Allowed values*: `http | https`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReplaceKeyPrefixWith`  <a name="cfn-s3-bucket-redirectrule-replacekeyprefixwith"></a>
The object key prefix to use in the redirect request\. For example, to redirect requests for all pages with prefix `docs/` \(objects in the `docs/` folder\) to `documents/`, you can set a condition block with `KeyPrefixEquals` set to `docs/` and in the Redirect set `ReplaceKeyPrefixWith` to `/documents`\. Not required if one of the siblings is present\. Can be present only if `ReplaceKeyWith` is not provided\.  
Replacement must be made for object keys containing special characters \(such as carriage returns\) when using XML requests\. For more information, see [ XML related object key constraints](https://docs.aws.amazon.com/AmazonS3/latest/userguide/object-keys.html#object-key-xml-related-constraints)\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReplaceKeyWith`  <a name="cfn-s3-bucket-redirectrule-replacekeywith"></a>
The specific object key to use in the redirect request\. For example, redirect request to `error.html`\. Not required if one of the siblings is present\. Can be present only if `ReplaceKeyPrefixWith` is not provided\.  
Replacement must be made for object keys containing special characters \(such as carriage returns\) when using XML requests\. For more information, see [ XML related object key constraints](https://docs.aws.amazon.com/AmazonS3/latest/userguide/object-keys.html#object-key-xml-related-constraints)\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-s3-bucket-redirectrule--examples"></a>



### Configure a static website with a routing rule<a name="aws-properties-s3-bucket-redirectrule--examples--Configure_a_static_website_with_a_routing_rule"></a>

In this example, `AWS::S3::Bucket's Fn::GetAtt` values are used to provide outputs\. If an HTTP 404 error occurs, the routing rule redirects requests to an EC2 instance and inserts the object key prefix `report-404/` in the redirect\. For example, if you request a page called `ExamplePage.html` and it results in an HTTP 404 error, the request is routed to a page called `report-404/ExamplePage.html` on the specified instance\. For all other HTTP error codes, `error.html` is returned\. 

This example also specifies a metrics configuration called `EntireBucket` that enables CloudWatch request metrics at the bucket level\.

#### JSON<a name="aws-properties-s3-bucket-redirectrule--examples--Configure_a_static_website_with_a_routing_rule--json"></a>

```
{
    "Resources": {
        "S3Bucket": {
            "Type": "AWS::S3::Bucket",
            "Properties": {
                "AccessControl": "PublicRead",
                "BucketName": "public-bucket",
                "MetricsConfigurations": [
                    {
                        "Id": "EntireBucket"
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
            "DeletionPolicy": "Retain"
        }
    },
    "Outputs": {
        "WebsiteURL": {
            "Value": {
                "Fn::GetAtt": [
                    "S3Bucket",
                    "WebsiteURL"
                ]
            },
            "Description": "URL for website hosted on S3"
        },
        "S3BucketSecureURL": {
            "Value": {
                "Fn::Join": [
                    "",
                    [
                        "https://",
                        {
                            "Fn::GetAtt": [
                                "S3Bucket",
                                "DomainName"
                            ]
                        }
                    ]
                ]
            },
            "Description": "Name of S3 bucket to hold website content"
        }
    }
}
```

#### YAML<a name="aws-properties-s3-bucket-redirectrule--examples--Configure_a_static_website_with_a_routing_rule--yaml"></a>

```
Resources:
  S3Bucket:
    Type: 'AWS::S3::Bucket'
    Properties:
      AccessControl: PublicRead
      BucketName: public-bucket
      MetricsConfigurations:
        - Id: EntireBucket
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
Outputs:
  WebsiteURL:
    Value: !GetAtt
      - S3Bucket
      - WebsiteURL
    Description: URL for website hosted on S3
  S3BucketSecureURL:
    Value: !Join
      - ''
      - - 'https://'
        - !GetAtt
          - S3Bucket
          - DomainName
    Description: Name of S3 bucket to hold website content
```