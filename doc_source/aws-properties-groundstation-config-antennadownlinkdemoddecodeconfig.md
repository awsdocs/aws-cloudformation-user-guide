# AWS::GroundStation::Config AntennaDownlinkDemodDecodeConfig<a name="aws-properties-groundstation-config-antennadownlinkdemoddecodeconfig"></a>

 Provides information about how AWS Ground Station should configure an antenna for downlink during a contact\. Use an antenna downlink demod decode config in a mission profile to receive the downlink data that has been demodulated and decoded\. 

## Syntax<a name="aws-properties-groundstation-config-antennadownlinkdemoddecodeconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-groundstation-config-antennadownlinkdemoddecodeconfig-syntax.json"></a>

```
{
  "[DecodeConfig](#cfn-groundstation-config-antennadownlinkdemoddecodeconfig-decodeconfig)" : DecodeConfig,
  "[DemodulationConfig](#cfn-groundstation-config-antennadownlinkdemoddecodeconfig-demodulationconfig)" : DemodulationConfig,
  "[SpectrumConfig](#cfn-groundstation-config-antennadownlinkconfig-spectrumconfig)" : SpectrumConfig
}
```

### YAML<a name="aws-properties-groundstation-config-antennadownlinkdemoddecodeconfig-syntax.yaml"></a>

```
  [DecodeConfig](#cfn-groundstation-config-antennadownlinkdemoddecodeconfig-decodeconfig): 
    DecodeConfig
  [DemodulationConfig](#cfn-groundstation-config-antennadownlinkdemoddecodeconfig-demodulationconfig): 
    DemodulationConfig
  [SpectrumConfig](#cfn-groundstation-config-antennadownlinkconfig-spectrumconfig): 
    SpectrumConfig
```

## Properties<a name="aws-properties-groundstation-config-antennadownlinkdemoddecodeconfig-properties"></a>

`DecodeConfig`  <a name="cfn-groundstation-config-antennadownlinkdemoddecodeconfig-decodeconfig"></a>
 Defines how the RF signal will be decoded\.   
*Required*: Yes  
*Type*: [DecodeConfig](aws-properties-groundstation-config-decodeconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DemodulationConfig`  <a name="cfn-groundstation-config-antennadownlinkdemoddecodeconfig-demodulationconfig"></a>
 Defines how the RF signal will be demodulated\.   
*Required*: Yes  
*Type*: [DemodulationConfig](aws-properties-groundstation-config-demodulationconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SpectrumConfig`  <a name="cfn-groundstation-config-antennadownlinkconfig-spectrumconfig"></a>
 Defines the spectrum configuration\.   
*Required*: Yes  
*Type*: [SpectrumConfig](aws-properties-groundstation-config-spectrumconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-groundstation-config-antennadownlinkdemoddecodeconfig--examples"></a>

### Create an AntennaDownlinkDemodDecodeConfig<a name="aws-properties-groundstation-config-antennadownlinkdemoddecodeconfig--examples--Create_an_AntennaDownlinkDemodDecodeConfig"></a>

The following example creates a Ground Station `AntennaDownlinkDemodDecodeConfig`

#### JSON<a name="aws-properties-groundstation-config-antennadownlinkdemoddecodeconfig--examples--Create_an_AntennaDownlinkDemodDecodeConfig--json"></a>

```
{
  "AntennaDownlinkDemodDecodeConfig": {
    "SpectrumConfig": {
      "CenterFrequency": {
        "Value": 7812,
        "Units": "MHz"
      },
      "Polarization": "RIGHT_HAND",
      "Bandwidth": {
        "Value": 30,
        "Units": "MHz"
      }
    },
    "DemodulationConfig": {
      "UnvalidatedJSON": "{ \"type\":\"QPSK\", \"qpsk\":{ \"carrierFrequencyRecovery\":{ \"centerFrequency\":{ \"value\":7812, \"units\":\"MHz\" }, \"range\":{ \"value\":250, \"units\":\"kHz\" } }, \"symbolTimingRecovery\":{ \"symbolRate\":{ \"value\":15, \"units\":\"Msps\" }, \"range\":{ \"value\":0.75, \"units\":\"ksps\" }, \"matchedFilter\":{ \"type\":\"ROOT_RAISED_COSINE\", \"rolloffFactor\":0.5 } } } }"
    },
    "DecodeConfig": {
      "UnvalidatedJSON": "{ \"edges\":[ { \"from\":\"I-Ingress\", \"to\":\"IQ-Recombiner\" }, { \"from\":\"Q-Ingress\", \"to\":\"IQ-Recombiner\" }, { \"from\":\"IQ-Recombiner\", \"to\":\"CcsdsViterbiDecoder\" }, { \"from\":\"CcsdsViterbiDecoder\", \"to\":\"NrzmDecoder\" }, { \"from\":\"NrzmDecoder\", \"to\":\"UncodedFramesEgress\" } ], \"nodeConfigs\":{ \"I-Ingress\":{ \"type\":\"CODED_SYMBOLS_INGRESS\", \"codedSymbolsIngress\":{ \"source\":\"I\" } }, \"Q-Ingress\":{ \"type\":\"CODED_SYMBOLS_INGRESS\", \"codedSymbolsIngress\":{ \"source\":\"Q\" } }, \"IQ-Recombiner\":{ \"type\":\"IQ_RECOMBINER\" }, \"CcsdsViterbiDecoder\":{ \"type\":\"CCSDS_171_133_VITERBI_DECODER\", \"ccsds171133ViterbiDecoder\":{ \"codeRate\":\"ONE_HALF\" } }, \"NrzmDecoder\":{ \"type\":\"NRZ_M_DECODER\" }, \"UncodedFramesEgress\":{ \"type\":\"UNCODED_FRAMES_EGRESS\" } } }"
    }
  }
}
```

#### YAML<a name="aws-properties-groundstation-config-antennadownlinkdemoddecodeconfig--examples--Create_an_AntennaDownlinkDemodDecodeConfig--yaml"></a>

```
AntennaDownlinkDemodDecodeConfig:
  SpectrumConfig:
    CenterFrequency:
      Value: 7812
      Units: MHz
    Polarization: RIGHT_HAND
    Bandwidth:
      Value: 30
      Units: MHz
    DemodulationConfig:
      UnvalidatedJSON: '{
        "type":"QPSK",
        "qpsk":{
          "carrierFrequencyRecovery":{
            "centerFrequency":{
              "value":7812,
              "units":"MHz"
            },
            "range":{
              "value":250,
              "units":"kHz"
            }
          },
          "symbolTimingRecovery":{
            "symbolRate":{
              "value":15,
              "units":"Msps"
          },
          "range":{
            "value":0.75,
            "units":"ksps"
          },
          "matchedFilter":{
            "type":"ROOT_RAISED_COSINE",
            "rolloffFactor":0.5
          }
        }
      }
    }'
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