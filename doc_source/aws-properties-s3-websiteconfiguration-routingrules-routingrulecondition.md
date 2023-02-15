# AWS::S3::Bucket RoutingRuleCondition<a name="aws-properties-s3-websiteconfiguration-routingrules-routingrulecondition"></a>

A container for describing a condition that must be met for the specified redirect to apply\. For example, 1\. If request is for pages in the `/docs` folder, redirect to the `/documents` folder\. 2\. If request results in HTTP error 4xx, redirect request to another host where you might process the error\.

## Syntax<a name="aws-properties-s3-websiteconfiguration-routingrules-routingrulecondition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-websiteconfiguration-routingrules-routingrulecondition-syntax.json"></a>

```
{
  "[HttpErrorCodeReturnedEquals](#cfn-s3-websiteconfiguration-routingrules-routingrulecondition-httperrorcodereturnedequals)" : String,
  "[KeyPrefixEquals](#cfn-s3-websiteconfiguration-routingrules-routingrulecondition-keyprefixequals)" : String
}
```

### YAML<a name="aws-properties-s3-websiteconfiguration-routingrules-routingrulecondition-syntax.yaml"></a>

```
  [HttpErrorCodeReturnedEquals](#cfn-s3-websiteconfiguration-routingrules-routingrulecondition-httperrorcodereturnedequals): String
  [KeyPrefixEquals](#cfn-s3-websiteconfiguration-routingrules-routingrulecondition-keyprefixequals): String
```

## Properties<a name="aws-properties-s3-websiteconfiguration-routingrules-routingrulecondition-properties"></a>

`HttpErrorCodeReturnedEquals`  <a name="cfn-s3-websiteconfiguration-routingrules-routingrulecondition-httperrorcodereturnedequals"></a>
The HTTP error code when the redirect is applied\. In the event of an error, if the error code equals this value, then the specified redirect is applied\.  
Required when parent element `Condition` is specified and sibling `KeyPrefixEquals` is not specified\. If both are specified, then both must be true for the redirect to be applied\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KeyPrefixEquals`  <a name="cfn-s3-websiteconfiguration-routingrules-routingrulecondition-keyprefixequals"></a>
The object key name prefix when the redirect is applied\. For example, to redirect requests for `ExamplePage.html`, the key prefix will be `ExamplePage.html`\. To redirect request for all pages with the prefix `docs/`, the key prefix will be `/docs`, which identifies all objects in the docs/ folder\.  
Required when the parent element `Condition` is specified and sibling `HttpErrorCodeReturnedEquals` is not specified\. If both conditions are specified, both must be true for the redirect to be applied\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-s3-websiteconfiguration-routingrules-routingrulecondition--examples"></a>



### Configure a static website with a routing rule<a name="aws-properties-s3-websiteconfiguration-routingrules-routingrulecondition--examples--Configure_a_static_website_with_a_routing_rule"></a>

In this example, `AWS::S3::Bucket's Fn::GetAtt` values are used to provide outputs\. If an HTTP 404 error occurs, the routing rule redirects requests to an EC2 instance and inserts the object key prefix `report-404/` in the redirect\. For example, if you request a page called `ExamplePage.html` and it results in an HTTP 404 error, the request is routed to a page called `report-404/ExamplePage.html` on the specified instance\. For all other HTTP error codes, `error.html` is returned\. 

This example also specifies a metrics configuration called `EntireBucket` that enables CloudWatch request metrics at the bucket level\.

#### JSON<a name="aws-properties-s3-websiteconfiguration-routingrules-routingrulecondition--examples--Configure_a_static_website_with_a_routing_rule--json"></a>

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

#### YAML<a name="aws-properties-s3-websiteconfiguration-routingrules-routingrulecondition--examples--Configure_a_static_website_with_a_routing_rule--yaml"></a>

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