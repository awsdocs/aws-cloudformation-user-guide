# AWS::S3::Bucket WebsiteConfiguration<a name="aws-properties-s3-websiteconfiguration"></a>

Specifies website configuration parameters for an Amazon S3 bucket\.

## Syntax<a name="aws-properties-s3-websiteconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-websiteconfiguration-syntax.json"></a>

```
{
  "[ErrorDocument](#cfn-s3-websiteconfiguration-errordocument)" : String,
  "[IndexDocument](#cfn-s3-websiteconfiguration-indexdocument)" : String,
  "[RedirectAllRequestsTo](#cfn-s3-websiteconfiguration-redirectallrequeststo)" : RedirectAllRequestsTo,
  "[RoutingRules](#cfn-s3-websiteconfiguration-routingrules)" : [ RoutingRule, ... ]
}
```

### YAML<a name="aws-properties-s3-websiteconfiguration-syntax.yaml"></a>

```
  [ErrorDocument](#cfn-s3-websiteconfiguration-errordocument): String
  [IndexDocument](#cfn-s3-websiteconfiguration-indexdocument): String
  [RedirectAllRequestsTo](#cfn-s3-websiteconfiguration-redirectallrequeststo): 
    RedirectAllRequestsTo
  [RoutingRules](#cfn-s3-websiteconfiguration-routingrules): 
    - RoutingRule
```

## Properties<a name="aws-properties-s3-websiteconfiguration-properties"></a>

`ErrorDocument`  <a name="cfn-s3-websiteconfiguration-errordocument"></a>
The name of the error document for the website\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IndexDocument`  <a name="cfn-s3-websiteconfiguration-indexdocument"></a>
The name of the index document for the website\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RedirectAllRequestsTo`  <a name="cfn-s3-websiteconfiguration-redirectallrequeststo"></a>
The redirect behavior for every request to this bucket's website endpoint\.  
If you specify this property, you can't specify any other property\.
*Required*: No  
*Type*: [RedirectAllRequestsTo](aws-properties-s3-websiteconfiguration-redirectallrequeststo.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoutingRules`  <a name="cfn-s3-websiteconfiguration-routingrules"></a>
Rules that define when a redirect is applied and the redirect behavior\.  
*Required*: No  
*Type*: List of [RoutingRule](aws-properties-s3-websiteconfiguration-routingrules.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-s3-websiteconfiguration--examples"></a>



### Configure a static website with a routing rule<a name="aws-properties-s3-websiteconfiguration--examples--Configure_a_static_website_with_a_routing_rule"></a>

In this example, `AWS::S3::Bucket's Fn::GetAtt` values are used to provide outputs\. If an HTTP 404 error occurs, the routing rule redirects requests to an EC2 instance and inserts the object key prefix `report-404/` in the redirect\. For example, if you request a page called `ExamplePage.html` and it results in an HTTP 404 error, the request is routed to a page called `report-404/ExamplePage.html` on the specified instance\. For all other HTTP error codes, `error.html` is returned\. 

This example also specifies a metrics configuration called `EntireBucket` that enables CloudWatch request metrics at the bucket level\.

#### JSON<a name="aws-properties-s3-websiteconfiguration--examples--Configure_a_static_website_with_a_routing_rule--json"></a>

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

#### YAML<a name="aws-properties-s3-websiteconfiguration--examples--Configure_a_static_website_with_a_routing_rule--yaml"></a>

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