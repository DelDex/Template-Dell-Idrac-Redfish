# Template Dell Idrac Redfish

This Zabbix template is designed to collect power data from Dell iDRAC using the Redfish API. It monitors power consumption, power supply status, redundancy, and voltage metrics.

## Authors
- **Robert Gladewitz**
- **Deljin Davis Kanukadan**
## Features
- **Data collected via Redfish API**: The template retrieves power-related data from Dell iDRAC through the Redfish API.
- **Multiple discovery rules**: Automatically discovers and monitors power control, power supplies, redundancy status, and voltage levels.
- **Granular monitoring**: Each power control and supply item includes detailed metrics such as power consumption, limits, and efficiency.

## Items
- **Redfish PowerData**:  
  **Key**: `Redfish.PowerData`

## Discovery Rules
- **PowerControl**:  
  **Key**: `http.redfish.powercontrol`
  
- **PowerSupplies**:  
  **Key**: `http.redfish.powersupply`
  
- **Redundancy**:  
  **Key**: `http.redfish.redundancy`
  
- **Voltages**:  
  **Key**: `http.redfish.voltages`

## Power Control Item Prototypes

| **Prototype**                                                   | **Key**                                                                                     |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| Redfish Power Control {#MEMBERID} Name                           | `http.redfish.powercontrol.name[{#MEMBERID}]`                                                |
| Redfish Power Control {#MEMBERID} PowerCapacityWatts             | `http.redfish.powercontrol.powercapacitywatts[{#MEMBERID}]`                                  |
| Redfish Power Control {#MEMBERID} PowerConsumedWatts             | `http.redfish.powercontrol.powerconsumedwatts[{#MEMBERID}]`                                  |
| Redfish Power Control {#MEMBERID} PowerLimit CorrectionInMs      | `http.redfish.powercontrol.powerlimit.correctioninms[{#MEMBERID}]`                           |
| Redfish Power Control {#MEMBERID} PowerLimit LimitException      | `http.redfish.powercontrol.powerlimit.limitexception[{#MEMBERID}]`                           |
| Redfish Power Control {#MEMBERID} PowerLimit LimitInWatts        | `http.redfish.powercontrol.powerlimit.limitInwatts[{#MEMBERID}]`                             |
| Redfish Power Control {#MEMBERID} PowerMetrics AverageConsumedWatts | `http.redfish.powercontrol.powermetrics.averageconsumedwatts[{#MEMBERID}]`                    |
| Redfish Power Control {#MEMBERID} PowerMetrics IntervalInMin     | `http.redfish.powercontrol.powermetrics.intervalinmin[{#MEMBERID}]`                          |
| Redfish Power Control {#MEMBERID} PowerMetrics MaxConsumedWatts  | `http.redfish.powercontrol.powermetrics.maxconsumedwatts[{#MEMBERID}]`                       |
| Redfish Power Control {#MEMBERID} PowerMetrics MinConsumedWatts  | `http.redfish.powercontrol.powermetrics.minconsumedwatts[{#MEMBERID}]`                       |
| Redfish Power Control {#MEMBERID} PowerRequestedWatts            | `http.redfish.powercontrol.powerrequestedwatts[{#MEMBERID}]`                                 |

## Power Supplies Item Prototypes

| **Prototype**                                                     | **Key**                                                                                     |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| Redfish Power Supply {#MEMBERID} EfficiencyPercent                 | `http.redfish.powersupply.efficiencypercent[{#MEMBERID}]`                                    |
| Redfish Power Supply {#MEMBERID} FirmwareVersion                   | `http.redfish.powersupply.firmwareversion[{#MEMBERID}]`                                      |
| Redfish Power Supply {#MEMBERID} HotPluggable                      | `http.redfish.powersupply.hotpluggable[{#MEMBERID}]`                                         |
| Redfish Power Supply {#MEMBERID} InputRanges MaximumVoltage        | `http.redfish.powersupply.inputranges.maximumvoltage[{#MEMBERID}]`                           |
| Redfish Power Supply {#MEMBERID} InputRanges MinimumFrequencyHz    | `http.redfish.powersupply.inputranges.minimumfrequencyhz[{#MEMBERID}]`                       |
| Redfish Power Supply {#MEMBERID} InputRanges OutputWattage         | `http.redfish.powersupply.inputranges.outputwattage[{#MEMBERID}]`                            |
| Redfish Power Supply {#MEMBERID} LastPowerOutputWatts              | `http.redfish.powersupply.lastpoweroutputwatts[{#MEMBERID}]`                                 |
| Redfish Power Supply {#MEMBERID} LineInputVoltage                  | `http.redfish.powersupply.lineinputvoltage[{#MEMBERID}]`                                     |
| Redfish Power Supply {#MEMBERID} LineInputVoltageType              | `http.redfish.powersupply.lineinputvoltagetype[{#MEMBERID}]`                                 |
| Redfish Power Supply {#MEMBERID} Manufacturer                      | `http.redfish.powersupply.manufacturer[{#MEMBERID}]`                                         |
| Redfish Power Supply {#MEMBERID} Model                             | `http.redfish.powersupply.model[{#MEMBERID}]`                                                |
| Redfish Power Supply {#MEMBERID} PowerCapacityWatts                | `http.redfish.powersupply.powercapacitywatts[{#MEMBERID}]`                                   |
| Redfish Power Supply {#MEMBERID} PowerInputWatts                   | `http.redfish.powersupply.powerinputwatts[{#MEMBERID}]`                                      |
| Redfish Power Supply {#MEMBERID} PowerOutputWatts                  | `http.redfish.powersupply.poweroutputwatts[{#MEMBERID}]`                                     |
| Redfish Power Supply {#MEMBERID} PowerSupplyType                   | `http.redfish.powersupply.powersupplytype[{#MEMBERID}]`                                      |
| Redfish Power Supply {#MEMBERID} SerialNumber                      | `http.redfish.powersupply.serialnumber[{#MEMBERID}]`                                         |
| Redfish Power Supply {#MEMBERID} SparePartNumber                   | `http.redfish.powersupply.sparepartnumber[{#MEMBERID}]`                                      |

## Redundancy Item Prototypes

| **Prototype**                                                     | **Key**                                                                                     |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| Redfish Redundancy {#MEMBERID} MaxNumSupported                     | `http.redfish.redundancy.maxnumsupported[{#MEMBERID}]`                                       |
| Redfish Redundancy {#MEMBERID} MinNumNeeded                        | `http.redfish.redundancy.minnumneeded[{#MEMBERID}]`                                          |
| Redfish Redundancy {#MEMBERID} Mode                                | `http.redfish.redundancy.mode[{#MEMBERID}]`                                                  |
| Redfish Redundancy {#MEMBERID} Name                                | `http.redfish.redundancy.name[{#MEMBERID}]`                                                  |
| Redfish Redundancy {#MEMBERID} Status Health                       | `http.redfish.redundancy.status.health[{#MEMBERID}]`                                         |
| Redfish Redundancy {#MEMBERID} Status State                        | `http.redfish.redundancy.status.state[{#MEMBERID}]`                                          |

## Voltages Item Prototypes

| **Prototype**                                                     | **Key**                                                                                     |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| Redfish Voltages {#MEMBERID} LowerThresholdCritical                | `http.redfish.voltages.lowerthresholdcritical[{#MEMBERID}]`                                  |
| Redfish Voltages {#MEMBERID} LowerThresholdFatal                   | `http.redfish.voltages.lowerthresholdfatal[{#MEMBERID}]`                                     |
| Redfish Voltages {#MEMBERID} LowerThresholdNonCritical             | `http.redfish.voltages.lowerthresholdnoncritical[{#MEMBERID}]`                               |
| Redfish Voltages {#MEMBERID} Name                                  | `http.redfish.voltages.name[{#MEMBERID}]`                                                    |
| Redfish Voltages {#MEMBERID} PhysicalContext                       | `http.redfish.voltages.physicalcontext[{#MEMBERID}]`                                         |
| Redfish Voltages {#MEMBERID} ReadingVolts                          | `http.redfish.voltages.readingvolts[{#MEMBERID}]`                                            |
| Redfish Voltages {#MEMBERID} SensorNumber                          | `http.redfish.voltages.sensornumber[{#MEMBERID}]`                                            |
| Redfish Voltages {#MEMBERID} Status Health                         | `http.redfish.voltages.statushealth[{#MEMBERID}]`                                            |
| Redfish Voltages {#MEMBERID} Status State                          | `http.redfish.voltages.status.state[{#MEMBERID}]`                                            |
| Redfish Voltages {#MEMBERID} UpperThresholdCritical                | `http.redfish.voltages.upperthresholdcritical[{#MEMBERID}]`                                  |
| Redfish Voltages {#MEMBERID} UpperThresholdFatal                   | `http.redfish.voltages.upperthresholdfatal[{#MEMBERID}]`                                     |
| Redfish Voltages {#MEMBERID} UpperThresholdNonCritical             | `http.redfish.voltages.upperthresholdnoncritical[{#MEMBERID}]`                               |

## Triggers

There are no triggers in this template.
