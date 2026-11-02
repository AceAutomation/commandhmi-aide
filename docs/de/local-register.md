# Reservierte Register des CommandHMI-Systems

CommandHMI reserviert einige Register für besondere Zwecke; bei ihrer Verwendung sind die zugehörigen Hinweise zu beachten. Dies betrifft LB (lokale Bitspeicher), LW (lokale Wortregister) und RWI (Rezeptindex).

Beispiel:

LB: LB0-LB65535; LB50000-LB51999 sind der remanente (spannungsausfallsichere) Bereich;

LW: LW0-LW65535; LW50000-LW51993 sind der remanente (spannungsausfallsichere) Bereich. LW51994~LW51999 werden intern verwendet und stehen extern nicht zur Verfügung;

RWI: RWI0~RWI65535.

**Inhalt:**

•   [LB](local-register/lb.md)

•   [LW](local-register/lw.md)

•   [RWI](local-register/rwi.md)
