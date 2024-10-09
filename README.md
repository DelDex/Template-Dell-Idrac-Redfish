# Template Dell Idrac Redfish

This Zabbix template is designed to collect power data from Dell iDRAC using the Redfish API. It monitors power consumption, power supply status, redundancy, and voltage metrics.

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
1. `Redfish Power Control {#MEMBERID} Name`  
   **Key**: `http.redfish.powercontrol.name[{#MEMBERID}]`
   
2. `Redfish Power Control {#MEMBERID} PowerCapacityWatts`  
   **Key**: `http.redfish.powercontrol.powercapacitywatts[{#MEMBERID}]`
   
3. `Redfish Power Control {#MEMBERID} PowerConsumedWatts`  
   **Key**: `http.redfish.powercontrol.powerconsumedwatts[{#MEMBERID}]`
   
4. `Redfish Power Control {#MEMBERID} PowerLimit CorrectionInMs`  
   **Key**: `http.redfish.powercontrol.powerlimit.correctioninms[{#MEMBERID}]`
   
5. `Redfish Power Control {#MEMBERID} PowerLimit LimitException`  
   **Key**: `http.redfish.powercontrol.powerlimit.limitexception[{#MEMBERID}]`
   
6. `Redfish Power Control {#MEMBERID} PowerLimit LimitInWatts`  
   **Key**: `http.redfish.powercontrol.powerlimit.limitInwatts[{#MEMBERID}]`
   
7. `Redfish Power Control {#MEMBERID} PowerMetrics AverageConsumedWatts`  
   **Key**: `http.redfish.powercontrol.powermetrics.averageconsumedwatts[{#MEMBERID}]`
   
8. `Redfish Power Control {#MEMBERID} PowerMetrics IntervalInMin`  
   **Key**: `http.redfish.powercontrol.powermetrics.intervalinmin[{#MEMBERID}]`
   
9. `Redfish Power Control {#MEMBERID} PowerMetrics MaxConsumedWatts`  
   **Key**: `http.redfish.powercontrol.powermetrics.maxconsumedwatts[{#MEMBERID}]`
   
10. `Redfish Power Control {#MEMBERID} PowerMetrics MinConsumedWatts`  
    **Key**: `http.redfish.powercontrol.powermetrics.minconsumedwatts[{#MEMBERID}]`
   
11. `Redfish Power Control {#MEMBERID} PowerRequestedWatts`  
    **Key**: `http.redfish.powercontrol.powerrequestedwatts[{#MEMBERID}]`

## Power Supplies Item Prototypes
1. `Redfish Power Supply {#MEMBERID} EfficiencyPercent`  
   **Key**: `http.redfish.powersupply.efficiencypercent[{#MEMBERID}]`
   
2. `Redfish Power Supply {#MEMBERID} FirmwareVersion`  
   **Key**: `http.redfish.powersupply.firmwareversion[{#MEMBERID}]`
   
3. `Redfish Power Supply {#MEMBERID} HotPluggable`  
   **Key**: `http.redfish.powersupply.hotpluggable[{#MEMBERID}]`
   
4. `Redfish Power Supply {#MEMBERID} InputRanges MaximumVoltage`  
   **Key**: `http.redfish.powersupply.inputranges.maximumvoltage[{#MEMBERID}]`
   
5. `Redfish Power Supply {#MEMBERID} InputRanges MinimumFrequencyHz`  
   **Key**: `http.redfish.powersupply.inputranges.minimumfrequencyhz[{#MEMBERID}]`
   
6. `Redfish Power Supply {#MEMBERID} InputRanges OutputWattage`  
   **Key**: `http.redfish.powersupply.inputranges.outputwattage[{#MEMBERID}]`
   
7. `Redfish Power Supply {#MEMBERID} LastPowerOutputWatts`  
   **Key**: `http.redfish.powersupply.lastpoweroutputwatts[{#MEMBERID}]`
   
8. `Redfish Power Supply {#MEMBERID} LineInputVoltage`  
   **Key**: `http.redfish.powersupply.lineinputvoltage[{#MEMBERID}]`
   
9. `Redfish Power Supply {#MEMBERID} LineInputVoltageType`  
   **Key**: `http.redfish.powersupply.lineinputvoltagetype[{#MEMBERID}]`
   
10. `Redfish Power Supply {#MEMBERID} Manufacturer`  
    **Key**: `http.redfish.powersupply.manufacturer[{#MEMBERID}]`
    
11. `Redfish Power Supply {#MEMBERID} Model`  
    **Key**: `http.redfish.powersupply.model[{#MEMBERID}]`
    
12. `Redfish Power Supply {#MEMBERID} PowerCapacityWatts`  
    **Key**: `http.redfish.powersupply.powercapacitywatts[{#MEMBERID}]`
    
13. `Redfish Power Supply {#MEMBERID} PowerInputWatts`  
    **Key**: `http.redfish.powersupply.powerinputwatts[{#MEMBERID}]`
    
14. `Redfish Power Supply {#MEMBERID} PowerOutputWatts`  
    **Key**: `http.redfish.powersupply.poweroutputwatts[{#MEMBERID}]`

## Redundancy Item Prototypes
1. `Redfish Redundancy {#MEMBERID} MaxNumSupported`  
   **Key**: `http.redfish.redundancy.maxnumsupported[{#MEMBERID}]`
   
2. `Redfish Redundancy {#MEMBERID} MinNumNeeded`  
   **Key**: `http.redfish.redundancy.minnumneeded[{#MEMBERID}]`
   
3. `Redfish Redundancy {#MEMBERID} Mode`  
   **Key**: `http.redfish.redundancy.mode[{#MEMBERID}]`
   
4. `Redfish Redundancy {#MEMBERID} Name`  
   **Key**: `http.redfish.redundancy.name[{#MEMBERID}]`
   
5. `Redfish Redundancy {#MEMBERID} Status Health`  
   **Key**: `http.redfish.redundancy.status.health[{#MEMBERID}]`
   
6. `Redfish Redundancy {#MEMBERID} Status State`  
   **Key**: `http.redfish.redundancy.status.state[{#MEMBERID}]`

## Voltages Item Prototypes
1. `Redfish Voltages {#MEMBERID} LowerThresholdCritical`  
   **Key**: `http.redfish.voltages.lowerthresholdcritical[{#MEMBERID}]`
   
2. `Redfish Voltages {#MEMBERID} LowerThresholdFatal`  
   **Key**: `http.redfish.voltages.lowerthresholdfatal[{#MEMBERID}]`
   
3. `Redfish Voltages {#MEMBERID} LowerThresholdNonCritical`  
   **Key**: `http.redfish.voltages.lowerthresholdnoncritical[{#MEMBERID}]`
   
4. `Redfish Voltages {#MEMBERID} Name`  
   **Key**: `http.redfish.voltages.name[{#MEMBERID}]`
   
5. `Redfish Voltages {#MEMBERID} PhysicalContext`  
   **Key**: `http.redfish.voltages.physicalcontext[{#MEMBERID}]`
   
6. `Redfish Voltages {#MEMBERID} ReadingVolts`  
   **Key**: `http.redfish.voltages.readingvolts[{#MEMBERID}]`
   
7. `Redfish Voltages {#MEMBERID} SensorNumber`  
   **Key**: `http.redfish.voltages.sensornumber[{#MEMBERID}]`
   
8. `Redfish Voltages {#MEMBERID} Status Health`  
   **Key**: `http.redfish.voltages.statushealth[{#MEMBERID}]`
   
9. `Redfish Voltages {#MEMBERID} Status State`  
   **Key**: `http.redfish.voltages.status.state[{#MEMBERID}]`
   
10. `Redfish Voltages {#MEMBERID} UpperThresholdCritical`  
    **Key**: `http.redfish.voltages.upperthresholdcritical[{#MEMBERID}]`
    
11. `Redfish Voltages {#MEMBERID} UpperThresholdFatal`  
    **Key**: `http.redfish.volt
