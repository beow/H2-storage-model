# H2-storage-model
Excel model of a combined Wind-power with hydrogen store system. The hydrogen is produced with electrolysis at high winds and consumed at low winds. Input data is per hour production of wind power in kW during a year. This data is given for example by Svenska Kraftnät in Sweden and publically available.

Upper and a lower limits around a base level for the power output are given as input parameters, as well as hydrogen store size in kilo-tons (kt). Also efficiency parameters are needed (that is, energy to produce a kg of hydrogen and how much energy is returned when consuming it in a hydrogen gas turbine). Also electrolysis capacity can be set.

It is then possible to follow the "capped" output power levels and the level of the hydrogen store over the year. If it overflows, the amount over the top is considered as "Surplus H2" that could be used for other, non power balancing, purposes. If the storage underflows, output from the combined power system simply decreases. Also if the wind power above the upper output limit exceeds the electrolysis capacity, the output will be higer than the target "capped" output.

In v1.3 the output power baselines can be chosen to be either of
- Fixed
- Moving Average (EMA)
- Sinus shaped

The moving average base line simulates a "low pass filtered" power output. The sinus output may be used to fit either the yearly consumption rate or a yearly production profile.  

![screenshot](https://github.com/beow/H2-storage-model/blob/main/WindH2model.jpg)

WindPowerPlusH2storeSystem.xlsx have data for Sweden 2020 and is hence a template for leap years. For non-leap years, the WindPowerPlusH2storeSystemSweden2021.xlsx may be used as template.

2021-03-17:

Added a Wind + Water power system simulation that models a system where wind power is balanced with a water storage system to produce a stable power output. The model is based on the Swedish wind power pattern of 2021 together with other energy sources the same year and models an output that (roughly) follows the consumption pattern that year. Then it is possible to scale the windpower (with the same wind pattern) and see how water (plus a smaller component of import/export) power manages to regulate the wind power.

WindPowerPlusWaterStoreSystemSweden2021.xlsx

2021-04-04:

Added a Wind + H2 simulation for Germany 2020. 
Data from 
Agora Energiewende (2021): Agorameter