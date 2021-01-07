# Specification format<a name="cfn-resource-specification-format"></a>

AWS CloudFormation creates a specification for each [resource type](aws-template-resource-type-ref.md), such as `AWS::S3::Bucket` or `AWS::EC2::Instance`\. The following sections describe the format and each field within the specification\.

**Topics**
+ [Specification sections](#w7739ab1c33c14c21b7)
+ [Property specification](#cfn-resource-specification-format-propertytypes)
+ [Resource specification](#cfn-resource-specification-format-resourcetype)
+ [Example resource specification](#w7739ab1c33c14c21c13)

## Specification sections<a name="w7739ab1c33c14c21b7"></a>

The formal definition for each resource type is organized into three main sections: `PropertyTypes`, `ResourceSpecificationVersion`, and `ResourceTypes`, as shown in the following example:

```
{
  "PropertyTypes": {
    *Property specifications*
  },
  "ResourceSpecificationVersion": "Specification version number",
  "ResourceTypes": {
    *Resource specification*
  }
}
```

`PropertyTypes`  
For resources that have properties within a property \(also known as subproperties\), a list of subproperty specifications, such as which properties are required, the type of allowed value for each property, and their update behavior\. For more information, see [Property specification](#cfn-resource-specification-format-propertytypes)\.  
If a resource doesn't have subproperties, this section is omitted\.

`ResourceSpecificationVersion`  
The version of the resource specification\. The version format is `majorVersion.minorVersion.patch`, where each release increments the version number\. All resources have the same version number regardless of whether the resource was updated\.  
AWS CloudFormation increments the patch number when the service makes a backwards\-compatible bug fix, such as fixing a broken documentation link\. When AWS CloudFormation adds resources or properties that are backwards compatible, it increments the minor version number\. For example, later versions of a specification might add additional resource properties to support new features of an AWS service\.  
Backwards incompatible changes increment the major version number\. A backwards incompatible change can result from a change in the resource specification, such as a name change to a field, or a change to a resource, such as the making an optional resource property required\.

`ResourceTypes`  
The list of resources and information about each resource's properties, such as its property names, which properties are required, and their update behavior\. For more information, see [Resource specification](#cfn-resource-specification-format-resourcetype)\.  
If you view a file that contains the definition of one resource type, this property name is `ResourceType` \(singular\)\. 

## Property specification<a name="cfn-resource-specification-format-propertytypes"></a>

The specification for each property includes the following fields\. For subproperties, the property name uses the `resourceType.subpropertyName` format\.

```
"Property name": {
  "Documentation": "Link to the relevant documentation"
  "DuplicatesAllowed": "true or false",
  "ItemType": "Type of list or map (non-primitive)",
  "PrimitiveItemType": "Type of list or map (primitive)",
  "PrimitiveType": "Type of value (primitive)",
  "Required": "true or false",
  "Type": "Type of value (non-primitive)",
  "UpdateType": "Mutable, Immutable, or Conditional",
}
```

`Documentation`  
A link to the *AWS CloudFormation User Guide* that provides information about the property\.

`DuplicatesAllowed`  
If the value of the `Type` field is `List`, indicates whether AWS CloudFormation allows duplicate values\. If the value is `true`, AWS CloudFormation ignores duplicate values\. If the value is `false`, AWS CloudFormation returns an error if you submit duplicate values\.

`ItemType`  
If the value of the `Type` field is `List` or `Map`, indicates the type of list or map if they contain non\-primitive types\. Otherwise, this field is omitted\. For lists or maps that contain primitive types, the `PrimitiveItemType` property indicates the valid value type\.  
A subproperty name is a valid item type\. For example, if the type value is `List` and the item type value is `PortMapping`, you can specify a list of port mapping properties\.

`PrimitiveItemType`  
If the value of the `Type` field is `List` or `Map`, indicates the type of list or map if they contain primitive types\. Otherwise, this field is omitted\. For lists or maps that contain non\-primitive types, the `ItemType` property indicates the valid value type\.  
The valid primitive types for lists and maps are `String`, `Long`, `Integer`, `Double`, `Boolean`, or `Timestamp`\.  
For example, if the type value is `List` and the item type value is `String`, you can specify a list of strings for the property\. If the type value is `Map` and the item type value is `Boolean`, you can specify a string to Boolean mapping for the property\.

`PrimitiveType`  
For primitive values, the valid primitive type for the property\. A primitive type is a basic data type for resource property values\. The valid primitive types are `String`, `Long`, `Integer`, `Double`, `Boolean`, `Timestamp` or `Json`\. If valid values are a non\-primitive type, this field is omitted and the `Type` field indicates the valid value type\.

`Required`  
Indicates whether the property is required\.

`Type`  
For non\-primitive types, valid values for the property\. The valid types are a subproperty name, `List` or `Map`\. If valid values are a primitive type, this field is omitted and the `PrimitiveType` field indicates the valid value type\.  
A list is a comma\-separated list of values\. A map is a set of key\-value pairs, where the keys are always strings\. The value type for lists and maps are indicated by the `ItemType` or `PrimitiveItemType` field\.

`UpdateType`  
During a stack update, the update behavior when you add, remove, or modify the property\. AWS CloudFormation replaces the resource when you change immutable properties\. AWS CloudFormation doesn't replace the resource when you change mutable properties\. Conditional updates can be mutable or immutable, depending on, for example, which other properties you updated\. For more information, see the relevant [resource type](aws-template-resource-type-ref.md) documentation\.

## Resource specification<a name="cfn-resource-specification-format-resourcetype"></a>

The specification for each resource type includes the following fields\.

```
"Resource type name": {
  "Attributes": {
    "AttributeName": {
      "ItemType": "Return list or map type (non-primitive)",
      "PrimitiveItemType": "Return list or map type (primitive)",
      "PrimitiveType": "Return value type (primitive)",
      "Type": "Return value type (non-primitive)",
    }
  },
  "Documentation": "Link to the relevant documentation",
  "Properties": {
    *Property specifications*
  }
}
```

`Attributes`  
A list of resource attributes that you can use in an [`Fn::GetAtt`](intrinsic-function-reference-getatt.md) function\. For each attribute, this section provides the attribute name and the type of value that AWS CloudFormation returns\.    
`ItemType`  
If the value of the `Type` field is `List`, indicates the type of list that the `Fn::GetAtt` function returns for the attribute if the list contains non\-primitive types\. The valid type is a name of a property\.  
`PrimitiveItemType`  
If the value of the `Type` field is `List`, indicates the type of list that the `Fn::GetAtt` function returns for the attribute if the list contains primitive types\. For lists that contain non\-primitive types, the `ItemType` property indicates the valid value type\. The valid primitive types for lists are `String`, `Long`, `Integer`, `Double`, `Boolean`, or `Timestamp`\.  
For example, if the type value is `List` and the primitive item type value is `String`, the `Fn::GetAtt` function returns a list of strings\.  
`PrimitiveType`  
For primitive return values, the type of primitive value that the `Fn::GetAtt` function returns for the attribute\. A primitive type is a basic data type for resource property values\. The valid primitive types are `String`, `Long`, `Integer`, `Double`, `Boolean`, `Timestamp` or `Json`\.  
`Type`  
For non\-primitive return values, the type of value that the `Fn::GetAtt` function returns for the attribute\. The valid types are a property name or `List`\.  
A list is a comma\-separated list of values\. The value type for lists are indicated by the `ItemType` or `PrimitiveItemType` field\.

`Documentation`  
A link to the *AWS CloudFormation User Guide* for information about the resource\.

`Properties`  
A list of property specifications for the resource\. For details, see [Property specification](#cfn-resource-specification-format-propertytypes)\.

## Example resource specification<a name="w7739ab1c33c14c21c13"></a>

The following examples highlight and explain parts of the [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticsearch-domain.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticsearch-domain.html) resource specification\.

The `AWS::Elasticsearch::Domain` resource type contains subproperties, so the specification includes a `PropertyTypes` section\. This section is followed by the `ResourceSpecificationVersion` section, which shows the specification version as `1.0.0`\. After the specification version is the `ResourceType` section that specifies the resource type, provides a documentation link, and details the resource's properties\.

```
{
  "PropertyTypes": {
    ...

  },
  "ResourceSpecificationVersion": "1.0.0",
  "ResourceType": {
    "AWS::Elasticsearch::Domain": {
      "Documentation": "http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticsearch-domain.html",
      "Properties": {
        ...

        }
      }
    }
  }
}
```

Focusing on the `ResourceType` section, the following example shows two properties of the `AWS::Elasticsearch::Domain` resource type\. The `AdvancedOptions` property is not required and accepts a string to string map\. A map is a collection of key\-value pairs, where the keys are always strings\. The value type is indicated by the `ItemType` field, which is `String`\. Therefore, the type is a string to string map\. The update behavior for this property is mutable\. If update this property, AWS CloudFormation keeps the resource instead of creating a new one and then deleting the old one \(an immutable update\)\.

The `SnapshotOptions` property is not required and accepts a subproperty named `SnapshotOptions`\. Details of the `SnapshotOptions` subproperty is provided in the `PropertyTypes` section\.

```
{
  "PropertyTypes": {
    ...

  },
  "ResourceSpecificationVersion": "1.0.0",
  "ResourceType": {
    "AWS::Elasticsearch::Domain": {
      "Documentation": "http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticsearch-domain.html",
      "Properties": {
        ...

        "AdvancedOptions": {
          "Documentation": "http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticsearch-domain.html#cfn-elasticsearch-domain-advancedoptions",
          "DuplicatesAllowed": false,
          "PrimitiveItemType": "String",
          "Required": false,
          "Type": "Map",
          "UpdateType": "Mutable"
        },
        ...

        "SnapshotOptions": {
          "Documentation": "http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticsearch-domain.html#cfn-elasticsearch-domain-snapshotoptions",
          "Required": false,
          "Type": "SnapshotOptions",
          "UpdateType": "Mutable"
        },
        ...

      }
    }
  }
}
```

In the `PropertyTypes`, the specification lists all of the subproperties of a resource \(including nested subproperties\)\. The following example details the `AWS::Elasticsearch::Domain.SnapshotOptions` subproperty\. It contains one property named `AutomatedSnapshotStartHour`, which is not required and accepts integer value types\.

```
"PropertyTypes": {
  ...

  "AWS::Elasticsearch::Domain.SnapshotOptions": {
    "Documentation": "http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticsearch-domain-snapshotoptions.html",
    "Properties": {
      "AutomatedSnapshotStartHour": {
        "Documentation": "http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticsearch-domain-snapshotoptions.html#cfn-elasticsearch-domain-snapshotoptions-automatedsnapshotstarthour",
        "PrimitiveType": "Integer",
        "Required": false,
        "UpdateType": "Mutable"
      }
    }
  },
  ...
    
}
```

For your reference, the following example provides the entire `AWS::Elasticsearch::Domain` resource specification\.

```
{
  "PropertyTypes": {
    "AWS::Elasticsearch::Domain.EBSOptions": {
      "Documentation": "http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticsearch-domain-ebsoptions.html",
      "Properties": {
        "EBSEnabled": {
          "Documentation": "http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticsearch-domain-ebsoptions.html#cfn-elasticsearch-domain-ebsoptions-ebsenabled",
          "PrimitiveType": "Boolean",
          "Required": false,
          "UpdateType": "Mutable"
        },
        "Iops": {
          "Documentation": "http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticsearch-domain-ebsoptions.html#cfn-elasticsearch-domain-ebsoptions-iops",
          "PrimitiveType": "Integer",
          "Required": false,
          "UpdateType": "Mutable"
        },
        "VolumeSize": {
          "Documentation": "http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticsearch-domain-ebsoptions.html#cfn-elasticsearch-domain-ebsoptions-volumesize",
          "PrimitiveType": "Integer",
          "Required": false,
          "UpdateType": "Mutable"
        },
        "VolumeType": {
          "Documentation": "http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticsearch-domain-ebsoptions.html#cfn-elasticsearch-domain-ebsoptions-volumetype",
          "PrimitiveType": "String",
          "Required": false,
          "UpdateType": "Mutable"
        }
      }
    },
    "AWS::Elasticsearch::Domain.ElasticsearchClusterConfig": {
      "Documentation": "http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticsearch-domain-elasticsearchclusterconfig.html",
      "Properties": {
        "DedicatedMasterCount": {
          "Documentation": "http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticsearch-domain-elasticsearchclusterconfig.html#cfn-elasticsearch-domain-elasticseachclusterconfig-dedicatedmastercount",
          "PrimitiveType": "Integer",
          "Required": false,
          "UpdateType": "Mutable"
        },
        "DedicatedMasterEnabled": {
          "Documentation": "http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticsearch-domain-elasticsearchclusterconfig.html#cfn-elasticsearch-domain-elasticseachclusterconfig-dedicatedmasterenabled",
          "PrimitiveType": "Boolean",
          "Required": false,
          "UpdateType": "Mutable"
        },
        "DedicatedMasterType": {
          "Documentation": "http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticsearch-domain-elasticsearchclusterconfig.html#cfn-elasticsearch-domain-elasticseachclusterconfig-dedicatedmastertype",
          "PrimitiveType": "String",
          "Required": false,
          "UpdateType": "Mutable"
        },
        "InstanceCount": {
          "Documentation": "http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticsearch-domain-elasticsearchclusterconfig.html#cfn-elasticsearch-domain-elasticseachclusterconfig-instancecount",
          "PrimitiveType": "Integer",
          "Required": false,
          "UpdateType": "Mutable"
        },
        "InstanceType": {
          "Documentation": "http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticsearch-domain-elasticsearchclusterconfig.html#cfn-elasticsearch-domain-elasticseachclusterconfig-instancetype",
          "PrimitiveType": "String",
          "Required": false,
          "UpdateType": "Mutable"
        },
        "ZoneAwarenessEnabled": {
          "Documentation": "http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticsearch-domain-elasticsearchclusterconfig.html#cfn-elasticsearch-domain-elasticseachclusterconfig-zoneawarenessenabled",
          "PrimitiveType": "Boolean",
          "Required": false,
          "UpdateType": "Mutable"
        }
      }
    },
    "AWS::Elasticsearch::Domain.SnapshotOptions": {
      "Documentation": "http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticsearch-domain-snapshotoptions.html",
      "Properties": {
        "AutomatedSnapshotStartHour": {
          "Documentation": "http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticsearch-domain-snapshotoptions.html#cfn-elasticsearch-domain-snapshotoptions-automatedsnapshotstarthour",
          "PrimitiveType": "Integer",
          "Required": false,
          "UpdateType": "Mutable"
        }
      }
    },
    "Tag": {
      "Documentation": "http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html",
      "Properties": {
        "Key": {
          "Documentation": "http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html#cfn-resource-tags-key",
          "PrimitiveType": "String",
          "Required": true,
          "UpdateType": "Immutable"
        },
        "Value": {
          "Documentation": "http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html#cfn-resource-tags-value",
          "PrimitiveType": "String",
          "Required": true,
          "UpdateType": "Immutable"
        }
      }
    }
  },
  "ResourceType": {
    "AWS::Elasticsearch::Domain": {
      "Attributes": {
        "DomainArn": {
          "PrimitiveType": "String"
        },
        "DomainEndpoint": {
          "PrimitiveType": "String"
        }
      },
      "Documentation": "http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticsearch-domain.html",
      "Properties": {
        "AccessPolicies": {
          "Documentation": "http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticsearch-domain.html#cfn-elasticsearch-domain-accesspolicies",
          "PrimitiveType": "Json",
          "Required": false,
          "UpdateType": "Mutable"
        },
        "AdvancedOptions": {
          "Documentation": "http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticsearch-domain.html#cfn-elasticsearch-domain-advancedoptions",
          "DuplicatesAllowed": false,
          "PrimitiveItemType": "String",
          "Required": false,
          "Type": "Map",
          "UpdateType": "Mutable"
        },
        "DomainName": {
          "Documentation": "http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticsearch-domain.html#cfn-elasticsearch-domain-domainname",
          "PrimitiveType": "String",
          "Required": false,
          "UpdateType": "Immutable"
        },
        "EBSOptions": {
          "Documentation": "http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticsearch-domain.html#cfn-elasticsearch-domain-ebsoptions",
          "Required": false,
          "Type": "EBSOptions",
          "UpdateType": "Mutable"
        },
        "ElasticsearchClusterConfig": {
          "Documentation": "http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticsearch-domain.html#cfn-elasticsearch-domain-elasticsearchclusterconfig",
          "Required": false,
          "Type": "ElasticsearchClusterConfig",
          "UpdateType": "Mutable"
        },
        "ElasticsearchVersion": {
          "Documentation": "http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticsearch-domain.html#cfn-elasticsearch-domain-elasticsearchversion",
          "PrimitiveType": "String",
          "Required": false,
          "UpdateType": "Immutable"
        },
        "SnapshotOptions": {
          "Documentation": "http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticsearch-domain.html#cfn-elasticsearch-domain-snapshotoptions",
          "Required": false,
          "Type": "SnapshotOptions",
          "UpdateType": "Mutable"
        },
        "Tags": {
          "Documentation": "http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticsearch-domain.html#cfn-elasticsearch-domain-tags",
          "DuplicatesAllowed": true,
          "ItemType": "Tag",
          "Required": false,
          "Type": "List",
          "UpdateType": "Mutable"
        }
      }
    }
  },
  "ResourceSpecificationVersion": "1.4.1"
}
```