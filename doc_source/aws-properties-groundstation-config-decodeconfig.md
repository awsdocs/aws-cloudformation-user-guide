# AWS::GroundStation::Config DecodeConfig<a name="aws-properties-groundstation-config-decodeconfig"></a>

 Defines decoding settings\. 

## Syntax<a name="aws-properties-groundstation-config-decodeconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-groundstation-config-decodeconfig-syntax.json"></a>

```
{
  "[UnvalidatedJSON](#cfn-groundstation-config-decodeconfig-unvalidatedjson)" : JSON
}
```

### YAML<a name="aws-properties-groundstation-config-decodeconfig-syntax.yaml"></a>

```
  [UnvalidatedJSON](#cfn-groundstation-config-decodeconfig-unvalidatedjson): 
    JSON
```

## Properties<a name="aws-properties-groundstation-config-decodeconfig-properties"></a>

`UnvalidatedJSON`  <a name="cfn-groundstation-config-decodeconfig-unvalidatedjson"></a>
 The decoding settings are in JSON format and define a set of steps to perform to decode the data\.   
*Required*: Yes  
*Type*: JSON  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-groundstation-config-decodeconfig--examples"></a>

### Create a DecodeConfig<a name="aws-properties-groundstation-config-decodeconfig--examples--Create_a_DecodeConfig"></a>

The following example creates a Ground Station `DecodeConfig`

#### JSON<a name="aws-properties-groundstation-config-decodeconfig--examples--Create_a_DecodeConfig--json"></a>

```
{
  "DecodeConfig": {
    "UnvalidatedJSON": "{ \"edges\":[ { \"from\":\"I-Ingress\", \"to\":\"IQ-Recombiner\" }, { \"from\":\"Q-Ingress\", \"to\":\"IQ-Recombiner\" }, { \"from\":\"IQ-Recombiner\", \"to\":\"CcsdsViterbiDecoder\" }, { \"from\":\"CcsdsViterbiDecoder\", \"to\":\"NrzmDecoder\" }, { \"from\":\"NrzmDecoder\", \"to\":\"UncodedFramesEgress\" } ], \"nodeConfigs\":{ \"I-Ingress\":{ \"type\":\"CODED_SYMBOLS_INGRESS\", \"codedSymbolsIngress\":{ \"source\":\"I\" } }, \"Q-Ingress\":{ \"type\":\"CODED_SYMBOLS_INGRESS\", \"codedSymbolsIngress\":{ \"source\":\"Q\" } }, \"IQ-Recombiner\":{ \"type\":\"IQ_RECOMBINER\" }, \"CcsdsViterbiDecoder\":{ \"type\":\"CCSDS_171_133_VITERBI_DECODER\", \"ccsds171133ViterbiDecoder\":{ \"codeRate\":\"ONE_HALF\" } }, \"NrzmDecoder\":{ \"type\":\"NRZ_M_DECODER\" }, \"UncodedFramesEgress\":{ \"type\":\"UNCODED_FRAMES_EGRESS\" } } }"
  }
}
```

#### YAML<a name="aws-properties-groundstation-config-decodeconfig--examples--Create_a_DecodeConfig--yaml"></a>

```
DecodeConfig:
  UnvalidatedJSON: '{
    "edges":[
      {
        "from":"I-Ingress",
        "to":"IQ-Recombiner"
      },
      {
        "from":"Q-Ingress",
        "to":"IQ-Recombiner"
      },
      {
        "from":"IQ-Recombiner",
        "to":"CcsdsViterbiDecoder"
      },
      {
        "from":"CcsdsViterbiDecoder",
        "to":"NrzmDecoder"
      },
      {
        "from":"NrzmDecoder",
        "to":"UncodedFramesEgress"
      }
    ],
    "nodeConfigs":{
      "I-Ingress":{
        "type":"CODED_SYMBOLS_INGRESS",
        "codedSymbolsIngress":{
          "source":"I"
        }
      },
      "Q-Ingress":{
        "type":"CODED_SYMBOLS_INGRESS",
        "codedSymbolsIngress":{
          "source":"Q"
        }
      },
      "IQ-Recombiner":{
        "type":"IQ_RECOMBINER"
      },
      "CcsdsViterbiDecoder":{
        "type":"CCSDS_171_133_VITERBI_DECODER",
        "ccsds171133ViterbiDecoder":{
          "codeRate":"ONE_HALF"
        }
      },
      "NrzmDecoder":{
        "type":"NRZ_M_DECODER"
      },
      "UncodedFramesEgress":{
        "type":"UNCODED_FRAMES_EGRESS"
      }
    }
  }'
```