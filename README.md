# H2-storage-model
Excel model of a combined Wind-power with hydrogen store system. The hydrogen is produced with electrolysis at high winds and consumed at low winds. Input data is per hour production of wind power in kW during a year. This data is given for example by Svenska Kraftnät in Sweden and publically available.

Upper and a lower limits for the power output are given as input parameters, as well as hydrogen store size in kilo-tons (kt). Also efficiency parameters are needed (that is, energy to produce a kg of hydrogen and how much energy is returned when consuming it in a hydrogen gas turbine).

It is then possible to follow the level of the hydrogen store over the year. If it overflows, the amount over the top is considered as "Surplus H2" that could be used for other, non power balancing, purposes. If the storage underflows, output from the combined power system simply decreases.
