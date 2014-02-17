ScientificQuantities
====================

A template based C++11 class for definition and conversion of scientific quantities. 

The base class is based on the MKS (meter/kilogram/second) system of unit. From these we derive the other units. 
The following units are defined but this is not an exhaustive list: Mass, Length, Time, Area, Volume, Speed, Acceleration, Frequency, Force, Pressure, Angle. See https://en.wikipedia.org/wiki/International_System_of_Units#Units_and_prefixes

I created this class so I would avoid having to keep track of what units is being used across my code. These classes do the following:
- They explicitely enforce to give a unit when assigning a value: Angle a1 = 90_deg; Angle a2 = 1.2_rad;
- They prevent you from incorrectly performing calculations between units; what is kg⋅m2⋅s−3⋅A−1? WATT!! This is correct but K⋅m probably not!
- They do the conversions for you: Length l1 = 120_m; l1.in(km) => 0.12
