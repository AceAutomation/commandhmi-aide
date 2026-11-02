# Registres réservés du système CommandHMI

CommandHMI réserve certains registres à des usages particuliers ; consultez les instructions correspondantes avant de les utiliser. Il s'agit des LB (bits mémoire locaux), LW (mots mémoire locaux) et RWI (index de recette).

Par exemple :

LB : LB0-LB65535 ; LB50000-LB51999 constituent la zone sauvegardée en cas de coupure d'alimentation ;

LW : LW0-LW65535 ; LW50000-LW51993 constituent la zone sauvegardée en cas de coupure d'alimentation. LW51994~LW51999 sont à usage interne et ne doivent pas être utilisés ;

RWI: RWI0~RWI65535.

**Sommaire :**

•   [LB](local-register/lb.md)

•   [LW](local-register/lw.md)

•   [RWI](local-register/rwi.md)
