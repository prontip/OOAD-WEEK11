# OOAD-WEEK11
State Diagram

พรทิพย์ เกิดรัตน์ 57030199

รูปที่1

![](http://www.plantuml.com/plantuml/img/ZP6n2i8m68JtFCNHKIXYidMGJfsqVG1n23RIGasa-KjVtmHhcYW5j-JklkF_azAI76bw38nw6XIQfzALrCp9f93PkQTRTsZg3D8Yt5WueG1QiwTfr30Qr2dSlt6Uu3pW_3zS9BW8kDZ4Bxihylo8U4gVSMXgyMrBnDPQv0FkVKvcHl5MaUop-6VJgj7ly1CIIKabBSMPfTe5t3GiBbgb3xOefTAj_xyN)

@startuml
title OpenFan
state "switch1ON" as switch1ON
switch1ON :  do/turn on the fan
state "switch2ON" as switch2ON
switch2ON :  do/turn on the fan
state "switch3ON" as switch3ON
switch3ON :  do/turn on the fan
[*] --> switch1ON : turnON
[*] --> switch2ON : turnON
[*] --> switch3ON : turnON
switch1ON --> FanLow :switch ON
switch2ON --> FanModerate :switch ON
switch3ON --> FanLowFast :switch ON
FanLow -->[*]
FanModerate -->[*]
FanLowFast -->[*]
@enduml


รูปที่2

![](http://www.plantuml.com/plantuml/img/VP4n2uCm48Nt-nM7Oq6wEvI2pdMnBgM3QAo2JKGZ_ltUnMWrYal8tRtxU2_HjMu49gbKyBgyqVTl_LZhl8hB4WCzT39-GAypBT1R1XvcFIuLh1OG2tNbBLGITSNWxNPOPVBpR5S4su5DPKb9Qch242gdgnGD3kq1CbAZTA7S0wS-0nT_FOUXfo3xb2FW4yoLUuxH6HLE52S7BLY1dLFI8zBaxOHb13jQjBFCdnYOXCX_ivTR4RYsvlvTo6BuDW0_)

title TVno
[*] -->switchOff :turnON
state "switchOff" as switchOff
switchOff :  do/turn on the TV
state "switchChangUp" as switchChangUp
switchChangUp :  do/TVChange The channel up
state "switchChangDown" as switchChangDown
switchChangDown :  do/TVChange The channel down
switchOff --> TVon :TVon
TVon --> switchChangUp :TVChangeChannel
switchChangUp -->TVChangChannelUp
TVon --> switchChangDown :TVChangeChannel
switchChangDown -->TVChangChannelDown
switchOff -->[*] :do/TV Off
TVChangChannelDown -->[*]
TVChangChannelUp -->[*]
@enduml


รูปที่3

![](http://www.plantuml.com/plantuml/img/SoWkIImgAStDuIh9BCb9LV0lICtpISmjAE82IfIaAYWLbsUM96SO-lifAIGMAy1vN72MWfM2Gag-VabfKPv2Vfv2IKQg0iW0hcYjM0NT8bqxX1uha1h_F2IjO7cGQf0n4645eDbG4P0iq1GkXzIy590BkRW0)

@startuml
title OpenLampr
state "switch1ON" as switch1ON
switch1ON :  do/turn on the Lamp
[*] -r-> switch1ON:turnOn
switch1ON -r-> LampON :switch ON
LampON -r->[*]
@enduml

รูปที่4

![](http://www.plantuml.com/plantuml/img/SoWkIImgAStDuIh9BCb9LV0lICqBIqmkBSrLICv9JSnBBU82gYX9LL0gBiyiISumzFTJKaWiLe3pkE0i1Ik5b7nzLCqAcSKAPH0HhcYjM0LTNJk4LgkIqg8y_pma4q3I40ES8VgXfbb1b2W0hSCc3TG6D1oVES4b-GLbQ6QvkN7XKWCrq24rBmKKD5nS0000)

@startuml
title OpenVacuum cleaner
state "switch1ON" as switch1ON
switch1ON : do/Vacuum cleaner is vacuum 
[*] --> switch1ON:turnOn
switch1ON --> VacuumCleanerVacuum :switch ON
VacuumCleanerVacuum -->[*]
switch1ON --> VacuumCleanerStopvacuum :switch OFF
VacuumCleanerStopvacuum -->[*]
@enduml


รูปที่5

![](http://www.plantuml.com/plantuml/img/RL2n2eD03Dtp5S6n8DqTnB53yGR7qk7GWC8r5Y_gxpV7SRPNt9ANzrvUqdYnYwml1pA98pHlOhCHW-92MFXzaduqRO7MOseW5LZXC5zbNHXdHXbL7xIFonFBiZxuLM0O_ifq6EkE7FLofurSS8jWQ_Bj6UadI8R3gU5_l1jPYUUTi3LLcdVXAocFckUu4lL4Q8W7_Hm2m0S0)

@startuml
title OpenOven
state "switchON" as switchON
switchON : do/turn on the Oven
[*] --> switchON:turnOn
switchON -->switchSelectLevelON :switchNO
state "switchSelectLevelON" as switchSelectLevelON
switchSelectLevelON : do/turn on the HeatOven
switchSelectLevelON -->HeatOvenStart :switchON
HeatOvenStart -->[*]
@enduml 


รูปที่6

![](http://www.plantuml.com/plantuml/img/RP0n3i8m34Ltd-AFxS00R7Gf4WVW2b6Rj9RQ1CKkLMvFKq22mc9Rt_zzIwv5JTHf78YKTR1mncE7SwDyPqsuiEcY6K6hZzYXk4Oh0fbPcnxx4jfRZo9PAGauIN1QaHt4el0XIp_COSlCxDjKBTCdzWSyRi1yJcFm7N92jIhV4TdHJuespFwrzoqxUlTd5GqtgfSv_-41)

@startuml

title fan - Activity Diagram 
start
if (Press switch 1) then (yes)
  :soft;
else (no)
  if (Press switch 2) then (yes)
  :windy;
  else (no)
    if (Press switch 3) then (yes)
    :strong wind;
    else (no)
      :shut down;
    endif
  endif
endif
stop
@enduml


รูปที่7

![](http://www.plantuml.com/plantuml/img/JOqn3i8m40JxUyMMJi47e0aI9HqliC8vFiavetW1vVSngUXMevtTiJ6kV2z5Q2oAOdCcJhXEj8znmytYlCO5SXJ54iBZQvmogWzWLaVOj0q2dE-7NFqYMfeYUFt7ANNkJqjzghvaxFdtkmC0)

@startuml
title light - Activity Diagram 
start
if (Switch on) then (yes)
  :Light on;
else (no)
  :Light off;
endif
stop
@enduml


รูป8

![](http://www.plantuml.com/plantuml/img/LOun3i8m40JxVSMMJi47e0c27_02AzZa9FiEsGSelq-8H46vcjLenkwn-QiMmCLBugMQYblZWUV9vIs-y2hnqM8bWFqEI6QuVSIdcQO3VKxAiAG-W3p-3AOdfD8JWze_o7aZUfVy5TeJ6BUrHwm0
)

@startuml
title Cmonitor - Activity Diagram 
start
if (Switch on) then (yes)
  :monitor on;
else (no)
  :monitor off;
endif
stop
@enduml


รูปที่9

![](http://www.plantuml.com/plantuml/img/NOyn3eCm34Ltdy8Z3Bq0MQZ4tALGgMD4as8f915nGRrz4sYgg1xixw__BBaDB1T-pGQ0YOt2_eOdF8zCA_4REvBFHSu807iGW3HMrurudD3P6dbI5gkBgm5ZDVsAJci1oWI5rLs5mhSYwW8VVCQ_kMRmANAm-MG1T6wpVqY4aYjscS0Vf-o3DEHvzFY3ym1jtDB77m00
)

@startuml
title TV - Activity Diagram 
start
if (Switch on) then (No)
    :Tv off;
else (Yes)
    :Tv on;
  if (Switch Up) then (Yes)
  :Up;
  else (No)
    if (Switch Down) then (Yes)
    :Down;
    else(No)
    endif
  endif
endif
stop
@enduml


รูปที่10

![](http://www.plantuml.com/plantuml/img/RL2n2eD03Dtp5S6n8DqTnB53yGR7qk7GWC8r5Y_gxpV7SRPNt9ANzrvUqdYnYwml1pA98pHlOhCHW-92MFXzaduqRO7MOseW5LZXC5zbNHXdHXbL7xIFonFBiZxuLM0O_ifq6EkE7FLofurSS8jWQ_Bj6UadI8R3gU5_l1jPYUUTi3LLcdVXAocFckUu4lL4Q8W7_Hm2m0S0)

@startuml
title OpenOven
state "switchON" as switchON
switchON : do/turn on the Oven
[*] --> switchON:turnOn
switchON -->switchSelectLevelON :switchNO
state "switchSelectLevelON" as switchSelectLevelON
switchSelectLevelON : do/turn on the HeatOven
switchSelectLevelON -->HeatOvenStart :switchON
HeatOvenStart -->[*]
@enduml 
