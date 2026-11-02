# Registri riservati del sistema CommandHMI

CommandHMI riserva alcuni registri a usi speciali; per usarli occorre fare riferimento alle relative istruzioni. Si tratta di LB (bit di memoria locale), LW (registri di memoria locale) e RWI (indice ricette).

Per esempio:

LB: LB0-LB65535; LB50000-LB51999 è l'area con ritenzione in caso di mancanza di alimentazione;

LW: LW0-LW65535; LW50000-LW51993 è l'area con ritenzione in caso di mancanza di alimentazione. LW51994~LW51999 sono riservati all'uso interno e non vanno usati;

RWI: RWI0~RWI65535.

**Indice:**

•   [LB](local-register/lb.md)

•   [LW](local-register/lw.md)

•   [RWI](local-register/rwi.md)
