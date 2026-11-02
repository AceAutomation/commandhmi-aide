# Registros reservados del sistema CommandHMI

CommandHMI reserva algunos registros para usos especiales; consulte sus instrucciones antes de usarlos: LB (bits de memoria local), LW (registros de memoria local) y RWI (índice de recetas).

Por ejemplo:

LB: LB0-LB65535; LB50000-LB51999 forman la zona remanente (protegida ante cortes de alimentación);

LW: LW0-LW65535; LW50000-LW51993 forman la zona remanente. LW51994~LW51999 son de uso interno, no externo;

RWI: RWI0~RWI65535.

**Contenido:**

•   [LB](local-register/lb.md)

•   [LW](local-register/lw.md)

•   [RWI](local-register/rwi.md)
