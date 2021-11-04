# AWS::S3::Bucket RoutingRule<a name="aws-properties-s3-websiteconfiguration-routingrules"></a>

Specifies the redirect behavior and when a redirect is applied\. For more information about routing rules, see [Configuring advanced conditional redirects](https://docs.aws.amazon.com/AmazonS3/latest/dev/how-to-page-redirect.html#advanced-conditional-redirects) in the *Amazon S3 User Guide*\.

## Syntax<a name="aws-properties-s3-websiteconfiguration-routingrules-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-websiteconfiguration-routingrules-syntax.json"></a>

```
{
  "[RedirectRule](#cfn-s3-websiteconfiguration-routingrules-redirectrule)" : RedirectRule,
  "[RoutingRuleCondition](#cfn-s3-websiteconfiguration-routingrules-routingrulecondition)" : RoutingRuleCondition
}
```

### YAML<a name="aws-properties-s3-websiteconfiguration-routingrules-syntax.yaml"></a>

```
  [RedirectRule](#cfn-s3-websiteconfiguration-routingrules-redirectrule): 
    RedirectRule
  [RoutingRuleCondition](#cfn-s3-websiteconfiguration-routingrules-routingrulecondition): 
    RoutingRuleCondition
```

## Properties<a name="aws-properties-s3-websiteconfiguration-routingrules-properties"></a>

`RedirectRule`  <a name="cfn-s3-websiteconfiguration-routingrules-redirectrule"></a>
Container for redirect information\. You can redirect requests to another host, to another page, or with another protocol\. In the event of an error, you can specify a different error code to return\.  
*Required*: Yes  
*Type*: [RedirectRule](aws-properties-s3-websiteconfiguration-routingrules-redirectrule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoutingRuleCondition`  <a name="cfn-s3-websiteconfiguration-routingrules-routingrulecondition"></a>
A container for describing a condition that must be met for the specified redirect to apply\. For example, 1\. If request is for pages in the `/docs` folder, redirect to the `/documents` folder\. 2\. If request results in HTTP error 4xx, redirect request to another host where you might process the error\.  
*Required*: No  
*Type*: [RoutingRuleCondition](aws-properties-s3-websiteconfiguration-routingrules-routingrulecondition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-s3-websiteconfiguration-routingrules--examples"></a>



### Configure a static website with a routing rule<a name="aws-properties-s3-websiteconfiguration-routingrules--examples--Configure_a_static_website_with_a_routing_rule"></a>

In this example, `AWS::S3::Bucket's Fn::GetAtt` values are used to provide outputs\. If an HTTP 404 error occurs, the routing rule redirects requests to an EC2 instance and inserts the object key prefix `report-404/` in the redirect\. For example, if you request a page called `ExamplePage.html` and it results in an HTTP 404 error, the request is routed to a page called `report-404/ExamplePage.html` on the specified instance\. For all other HTTP error codes, `error.html` is returned\. 

This example also specifies a metrics configuration called `EntireBucket` that enables CloudWatch request metrics at the bucket level\.

#### JSON<a name="aws-properties-s3-websiteconfiguration-routingrules--examples--Configure_a_static_website_with_a_routing_rule--json"></a>

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

#### YAML<a name="aws-properties-s3-websiteconfiguration-routingrules--examples--Configure_a_static_website_with_a_routing_rule--yaml"></a>

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