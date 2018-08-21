# AWS::SES::ConfigurationSetEventDestination<a name="aws-resource-ses-configurationseteventdestination"></a>

The `AWS::SES::ConfigurationSetEventDestination` resource specifies a configuration set event destination for Amazon SES\. For more information, see [CreateConfigurationSetEventDestination](http://docs.aws.amazon.com/ses/latest/APIReference/API_CreateConfigurationSetEventDestination.html) in the *Amazon Simple Email Service API Reference*\. 

**Note**  
When you create or update an event destination, you must provide one, and only one, destination\. The destination can be Amazon CloudWatch or Amazon Kinesis Firehose\.

An event destination is the AWS service to which Amazon SES publishes the email sending events associated with a configuration set\. For information, see [Using Amazon SES Configuration Sets](url-ses-dev;using-configuration-sets.html) in the *Amazon Simple Email Service Developer Guide*\.

**Topics**
+ [Syntax](#aws-resource-ses-configurationseteventdestination-syntax)
+ [Properties](#aws-resource-ses-configurationseteventdestination-properties)
+ [Example](#aws-resource-ses-configurationseteventdestination-examples)
+ [See Also](#aws-resource-ses-configurationseteventdestination-seealso)

## Syntax<a name="aws-resource-ses-configurationseteventdestination-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ses-configurationseteventdestination-syntax.json"></a>

```
{
  "Type" : "AWS::SES::ConfigurationSetEventDestination",
  "Properties" : {
    "[ConfigurationSetName](#cfn-ses-configurationseteventdestination-configurationsetname)" : String,
    "[EventDestination](#cfn-ses-configurationseteventdestination-eventdestination)" : [*EventDestination*](aws-properties-ses-configurationseteventdestination-eventdestination.md)
  }
}
```

### YAML<a name="aws-resource-ses-configurationseteventdestination-syntax.yaml"></a>

```
Type: "AWS::SES::ConfigurationSetEventDestination"
Properties:
  [ConfigurationSetName](#cfn-ses-configurationseteventdestination-configurationsetname): String
  [EventDestination](#cfn-ses-configurationseteventdestination-eventdestination): [*EventDestination*](aws-properties-ses-configurationseteventdestination-eventdestination.md)
```

## Properties<a name="aws-resource-ses-configurationseteventdestination-properties"></a>

`ConfigurationSetName`  <a name="cfn-ses-configurationseteventdestination-configurationsetname"></a>
The name of the configuration set that the event destination should be associated with\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`EventDestination`  <a name="cfn-ses-configurationseteventdestination-eventdestination"></a>
The AWS service that email sending event information will be published to\.  
 *Required*: Yes  
 *Type*: [Amazon SES ConfigurationSetEventDestination EventDestination](aws-properties-ses-configurationseteventdestination-eventdestination.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Example<a name="aws-resource-ses-configurationseteventdestination-examples"></a>

### <a name="aws-resource-ses-configurationseteventdestination-example1"></a>

#### JSON<a name="aws-resource-ses-configurationseteventdestination-example1.json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "AWS SES ConfigurationSetEventDestination Sample Template",
    "Parameters": {
        "ConfigSetName": {
            "Type": "String"
        },
        "EventDestinationName": {
            "Type": "String"
        },
        "EventType1": {
            "Type": "String"
        },
        "EventType2": {
            "Type": "String"
        },
        "EventType3": {
            "Type": "String"
        },
        "DimensionName1": {
            "Type": "String"
        },
        "DimensionValueSource1": {
            "Type": "String"
        },
        "DefaultDimensionValue1": {
            "Type": "String"
        },
        "DimensionName2": {
            "Type": "String"
        },
        "DimensionValueSource2": {
            "Type": "String"
        },
        "DefaultDimensionValue2": {
            "Type": "String"
        }
    },
    "Resources": {
        "ConfigSet": {
            "Type": "AWS::SES::ConfigurationSet",
            "Properties": {
                "Name": {
                    "Ref": "ConfigSetName"
                }
            }
        },
        "CWEventDestination": {
            "Type": "AWS::SES::ConfigurationSetEventDestination",
            "Properties": {
                "ConfigurationSetName": {
                    "Ref": "ConfigSet"
                },
                "EventDestination": {
                    "Name": {
                        "Ref": "EventDestinationName"
                    },
                    "Enabled": true,
                    "MatchingEventTypes": [
                        {
                            "Ref": "EventType1"
                        },
                        {
                            "Ref": "EventType2"
                        },
                        {
                            "Ref": "EventType3"
                        }
                    ],
                    "CloudWatchDestination": {
                        "DimensionConfigurations": [
                            {
                                "DimensionName": {
                                    "Ref": "DimensionName1"
                                },
                                "DimensionValueSource": {
                                    "Ref": "DimensionValueSource1"
                                },
                                "DefaultDimensionValue": {
                                    "Ref": "DefaultDimensionValue1"
                                }
                            },
                            {
                                "DimensionName": {
                                    "Ref": "DimensionName2"
                                },
                                "DimensionValueSource": {
                                    "Ref": "DimensionValueSource2"
                                },
                                "DefaultDimensionValue": {
                                    "Ref": "DefaultDimensionValue2"
                                }
                            }
                        ]
                    }
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-ses-configurationseteventdestination-example1.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: 'AWS SES ConfigurationSetEventDestination Sample Template'
Parameters:
  ConfigSetName:
    Type: String
  EventDestinationName:
    Type: String
  EventType1:
    Type: String
  EventType2:
    Type: String
  EventType3:
    Type: String
  DimensionName1:
    Type: String
  DimensionValueSource1:
    Type: String
  DefaultDimensionValue1:
    Type: String
  DimensionName2:
    Type: String
  DimensionValueSource2:
    Type: String
  DefaultDimensionValue2:
    Type: String

Resources:
  ConfigSet:
    Type: 'AWS::SES::ConfigurationSet'
    Properties:
      Name: !Ref ConfigSetName

  CWEventDestination:
    Type: 'AWS::SES::ConfigurationSetEventDestination'
    Properties:
      ConfigurationSetName: !Ref ConfigSet
      EventDestination:
        Name: !Ref EventDestinationName
        Enabled: true
        MatchingEventTypes:
          - !Ref EventType1
          - !Ref EventType2
          - !Ref EventType3
        CloudWatchDestination:
          DimensionConfigurations:
            - DimensionName: !Ref DimensionName1
              DimensionValueSource: !Ref DimensionValueSource1
              DefaultDimensionValue: !Ref DefaultDimensionValue1
            - DimensionName: !Ref DimensionName2
              DimensionValueSource: !Ref DimensionValueSource2
              DefaultDimensionValue: !Ref DefaultDimensionValue2
```

## See Also<a name="aws-resource-ses-configurationseteventdestination-seealso"></a>
+ [Using Amazon SES Configuration Sets](url-ses-dev;using-configuration-sets.html) in the *Amazon Simple Email Service Developer Guide*
+ [CreateConfigurationSetEventDestination](http://docs.aws.amazon.com/ses/latest/APIReference/API_CreateConfigurationSetEventDestination.html) in the *Amazon Simple Email Service API Reference*