# Reserved Registers of CommandHMI System

CommandHMI reserves some registers for special use, and users must refer to the related instructions when using these registers, including LB (Local Memory Bit); LW (Local Memory Register) and RWI (Formula Index).

For example:

LB: LB0-LB65535 and LB50000-LB51999 belong to the area of power failure protection;

LW: LW0-LW65535 and LW50000-LW51993 belong to the area of power failure protection. And LW51994~LW51999 are used by interior,  not external;

RWI: RWI0~RWI65535.

**Contents：**

•   [LB](local-register/lb.md)

•   [LW](local-register/lw.md)

•   [RWI](local-register/rwi.md)
