# AWS::Events::Rule InputTransformer<a name="aws-properties-events-rule-inputtransformer"></a>

Contains the parameters needed for you to provide custom input to a target based on one or more pieces of data extracted from the event\.

## Syntax<a name="aws-properties-events-rule-inputtransformer-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-events-rule-inputtransformer-syntax.json"></a>

```
{
  "[InputPathsMap](#cfn-events-rule-inputtransformer-inputpathsmap)" : {Key : Value, ...},
  "[InputTemplate](#cfn-events-rule-inputtransformer-inputtemplate)" : String
}
```

### YAML<a name="aws-properties-events-rule-inputtransformer-syntax.yaml"></a>

```
  [InputPathsMap](#cfn-events-rule-inputtransformer-inputpathsmap): 
    Key : Value
  [InputTemplate](#cfn-events-rule-inputtransformer-inputtemplate): String
```

## Properties<a name="aws-properties-events-rule-inputtransformer-properties"></a>

`InputPathsMap`  <a name="cfn-events-rule-inputtransformer-inputpathsmap"></a>
Map of JSON paths to be extracted from the event\. You can then insert these in the template in `InputTemplate` to produce the output you want to be sent to the target\.  
 `InputPathsMap` is an array key\-value pairs, where each value is a valid JSON path\. You can have as many as 100 key\-value pairs\. You must use JSON dot notation, not bracket notation\.  
The keys cannot start with "AWS\."   
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InputTemplate`  <a name="cfn-events-rule-inputtransformer-inputtemplate"></a>
Input template where you specify placeholders that will be filled with the values of the keys from `InputPathsMap` to customize the data sent to the target\. Enclose each `InputPathsMaps` value in brackets: <*value*>   
If `InputTemplate` is a JSON object \(surrounded by curly braces\), the following restrictions apply:  
+ The placeholder cannot be used as an object key\.
The following example shows the syntax for using `InputPathsMap` and `InputTemplate`\.  
 ` "InputTransformer":`   
 `{`   
 `"InputPathsMap": {"instance": "$.detail.instance","status": "$.detail.status"},`   
 `"InputTemplate": "<instance> is in state <status>"`   
 `}`   
To have the `InputTemplate` include quote marks within a JSON string, escape each quote marks with a slash, as in the following example:  
 ` "InputTransformer":`   
 `{`   
 `"InputPathsMap": {"instance": "$.detail.instance","status": "$.detail.status"},`   
 `"InputTemplate": "<instance> is in state \"<status>\""`   
 `}`   
The `InputTemplate` can also be valid JSON with varibles in quotes or out, as in the following example:  
 ` "InputTransformer":`   
 `{`   
 `"InputPathsMap": {"instance": "$.detail.instance","status": "$.detail.status"},`   
 `"InputTemplate": '{"myInstance": <instance>,"myStatus": "<instance> is in state \"<status>\""}'`   
 `}`   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `8192`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-events-rule-inputtransformer--examples"></a>



### Transform input into a string<a name="aws-properties-events-rule-inputtransformer--examples--Transform_input_into_a_string"></a>

The following example takes `instance` and `state` and outputs a string\. 

#### JSON<a name="aws-properties-events-rule-inputtransformer--examples--Transform_input_into_a_string--json"></a>

```
"InputTransformer": {
    "InputPathsMap": {
       "instance": "$.detail.instance-id",
       "state": "$.detail.state"
    },
    "InputTemplate": "\"instance <instance> is in <state>\"\n  }\n"
}
```

#### YAML<a name="aws-properties-events-rule-inputtransformer--examples--Transform_input_into_a_string--yaml"></a>

```
InputTransformer:
  InputPathsMap:
    "instance" : "$.detail.instance-id"
    "state" : "$.detail.state"
  InputTemplate: |
    "instance <instance> is in <state>"
```

### Transform input into JSON<a name="aws-properties-events-rule-inputtransformer--examples--Transform_input_into_JSON"></a>

The following example takes `instance` and `state` and outputs JSON that includes strings and variables\.

#### JSON<a name="aws-properties-events-rule-inputtransformer--examples--Transform_input_into_JSON--json"></a>

```
"InputTransformer": {
    "InputPathsMap": {
       "instance": "$.detail.instance-id",
       "state": "$.detail.state"
    },
    "InputTemplate": "{\n   \"instance\" : <instance>,\n   \"state\" : <state>,\n   \"instanceStatus\": \"instance \\\"<instance>\\\" is in <state>\"\n}\n"
}
```

#### YAML<a name="aws-properties-events-rule-inputtransformer--examples--Transform_input_into_JSON--yaml"></a>

```
InputTransformer:
  InputPathsMap:
    "instance" : "$.detail.instance-id"
    "state" : "$.detail.state"
  InputTemplate: |
    {
       "instance" : <instance>,
       "state" : <state>,
       "instanceStatus": "instance \"<instance>\" is in <state>"
    }
```

### Transform input and substitute a variable<a name="aws-properties-events-rule-inputtransformer--examples--Transform_input_and_substitute_a_variable"></a>

The following example defines a variable `RootDomainName`\. It then takes `instance` and `state`, substitutes `RootDomainName` for `domain`, and outputs JSON\.

#### JSON<a name="aws-properties-events-rule-inputtransformer--examples--Transform_input_and_substitute_a_variable--json"></a>

```
"Parameters": {
    "RootDomainName": {
        "Description": "Domain name to use",
        "Type": "String",
        "Default": "testdomain.com"
    }
},
```

#### JSON<a name="aws-properties-events-rule-inputtransformer--examples--Transform_input_and_substitute_a_variable--json"></a>

```
"InputTransformer": {
    "InputPathsMap": {
       "instance": "$.detail.instance-id",
       "state": "$.detail.state"
    },
    "InputTemplate": {
        "Fn::Sub": [
            "{\n   \"domain\": \"${Domain}\",\n   \"instance\" : <instance>,\n   \"state\" : <state>,\n   \"instanceStatus\": \"instance \\\"<instance>\\\" is in <state>\"\n} - ( Domain: !Ref RootDomainName )\n"
        ]
    }
}
```

#### YAML<a name="aws-properties-events-rule-inputtransformer--examples--Transform_input_and_substitute_a_variable--yaml"></a>

```
Parameters:
  RootDomainName:
    Description: Domain name to use
    Type: String
    Default: testdomain.com
```

#### YAML<a name="aws-properties-events-rule-inputtransformer--examples--Transform_input_and_substitute_a_variable--yaml"></a>

```
InputTransformer:
  InputPathsMap:
    "instance" : "$.detail.instance-id"
    "state" : "$.detail.state"
  InputTemplate: !Sub 
    - |
      {
         "domain": "${Domain}",
         "instance" : <instance>,
         "state" : <state>,
         "instanceStatus": "instance \"<instance>\" is in <state>"
      }
    - Domain: !Ref RootDomainName
```