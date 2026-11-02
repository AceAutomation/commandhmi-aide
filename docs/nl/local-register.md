# Gereserveerde systeemregisters van CommandHMI

CommandHMI reserveert een aantal registers voor speciale doeleinden; raadpleeg bij het gebruik ervan de bijbehorende instructies. Het gaat om LB (lokale geheugenbit), LW (lokaal geheugenregister) en RWI (receptindex).

Bijvoorbeeld:

LB: LB0-LB65535; LB50000-LB51999 behoren tot het tegen stroomuitval beveiligde gebied;

LW: LW0-LW65535; LW50000-LW51993 behoren tot het tegen stroomuitval beveiligde gebied. LW51994~LW51999 zijn voor intern gebruik, niet voor extern gebruik;

RWI: RWI0~RWI65535.

**Inhoud:**

•   [LB](local-register/lb.md)

•   [LW](local-register/lw.md)

•   [RWI](local-register/rwi.md)
