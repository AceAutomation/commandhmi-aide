# Can

Met dit stuurprogramma communiceert het touchscreen van de HM-serie met CAN-apparaten. Lees vóór gebruik aandachtig dit hoofdstuk en de technische documentatie.

Verbinding maken met CAN-apparaten

**1. Hardwareaansluiting**

Verbindingskabel:

RS485

|                  |      |                 |      |
|------------------|------|-----------------|------|
| **HM COM1/COM2** |      | **CAN**         |      |
| 1                | CANL | door gebruiker gedefinieerd | CANL |
| 4                | CANH | door gebruiker gedefinieerd | CANH |
| 5                | GND  | door gebruiker gedefinieerd | GND  |

**2. Software-instellingen**

De CAN-functie wordt gerealiseerd door systeemfuncties in een script aan te roepen

```c
int onCanxStart(PortID); Start can equipment
int onCanxstop (PortID); Off can equipment
int setBitrate (PortID); Set the can communication rate
int onCanxstop ( CanID, CanMask, PortID ); Can id filter
int reciveData ( data, Len, PortID ); Receive can data
int sendData ( data, Len, PortID, CanId, CanType ); Send can data
```

**3. Voorbeeld**

 1. Poortsnelheid instellen en het CAN-apparaat starten

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><div class="sourceCode" id="cb1"><pre class="sourceCode c"><code class="sourceCode c"><span id="cb1-1"><a href="#cb1-1" aria-hidden="true" tabindex="-1"></a><span class="pp">#include </span><span class="im">&quot;MacroInit.h&quot;</span></span>
<span id="cb1-2"><a href="#cb1-2" aria-hidden="true" tabindex="-1"></a><span class="dt">void</span> Macro_main <span class="op">(</span> IN <span class="op">*</span>p <span class="op">)</span></span>
<span id="cb1-3"><a href="#cb1-3" aria-hidden="true" tabindex="-1"></a><span class="op">{</span></span></code></pre></div>
<p>         MarcoInit</p>
<div class="sourceCode" id="cb2"><pre class="sourceCode c"><code class="sourceCode c"><span id="cb2-1"><a href="#cb2-1" aria-hidden="true" tabindex="-1"></a><span class="co">//ToDo</span></span>
<span id="cb2-2"><a href="#cb2-2" aria-hidden="true" tabindex="-1"></a><span class="dt">int</span> PortID<span class="op">,</span> Result<span class="op">,</span> Bitrate<span class="op">;</span></span>
<span id="cb2-3"><a href="#cb2-3" aria-hidden="true" tabindex="-1"></a>PortID <span class="op">=</span> <span class="dv">0</span><span class="op">;</span> <span class="co">//0：COM0 1：COM1</span></span>
<span id="cb2-4"><a href="#cb2-4" aria-hidden="true" tabindex="-1"></a>Bitrate <span class="op">=</span> <span class="dv">5</span><span class="op">*</span><span class="dv">1000</span><span class="op">;</span> <span class="co">// Poortsnelheid 5k; instelbereik 5k, 10k, 20k tot 1M</span></span>
<span id="cb2-5"><a href="#cb2-5" aria-hidden="true" tabindex="-1"></a>Result <span class="op">=</span> <span class="dv">0</span><span class="op">;</span></span></code></pre></div>
<p>         Result = setBitrate ( Bitrate, PortID );    // COM0: communicatiesnelheid 5000; retourwaarde 0 = OK, anders fout</p>
<div class="sourceCode" id="cb3"><pre class="sourceCode c"><code class="sourceCode c"><span id="cb3-1"><a href="#cb3-1" aria-hidden="true" tabindex="-1"></a>Result <span class="op">=</span> onCanxStart <span class="op">(</span> PortID <span class="op">);</span> <span class="co">// Retourwaarde 0 = OK, anders fout</span></span>
<span id="cb3-2"><a href="#cb3-2" aria-hidden="true" tabindex="-1"></a><span class="op">}</span></span></code></pre></div></td>
</tr>
</tbody>
</table>
 </td>
</tr>
</tbody>
</table>

2. Gegevens ontvangen

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><div class="sourceCode" id="cb1"><pre class="sourceCode c"><code class="sourceCode c"><span id="cb1-1"><a href="#cb1-1" aria-hidden="true" tabindex="-1"></a><span class="pp">#include </span><span class="im">&quot;MacroInit.h&quot;</span></span>
<span id="cb1-2"><a href="#cb1-2" aria-hidden="true" tabindex="-1"></a><span class="dt">void</span> Macro_main <span class="op">(</span> IN <span class="op">*</span>p <span class="op">)</span></span>
<span id="cb1-3"><a href="#cb1-3" aria-hidden="true" tabindex="-1"></a><span class="op">{</span></span></code></pre></div>
<p>    MarcoInit</p>
<div class="sourceCode" id="cb2"><pre class="sourceCode c"><code class="sourceCode c"><span id="cb2-1"><a href="#cb2-1" aria-hidden="true" tabindex="-1"></a><span class="co">//ToDo</span></span>
<span id="cb2-2"><a href="#cb2-2" aria-hidden="true" tabindex="-1"></a><span class="dt">int</span> PortID<span class="op">,</span> Result<span class="op">,</span> Len<span class="op">;</span></span></code></pre></div>
<p>    unsigned data[128];                // Ontvangstbuffer</p>
<div class="sourceCode" id="cb3"><pre class="sourceCode c"><code class="sourceCode c"><span id="cb3-1"><a href="#cb3-1" aria-hidden="true" tabindex="-1"></a>PortID <span class="op">=</span> <span class="dv">0</span><span class="op">;</span> <span class="co">//0：COM0 1：COM1</span></span>
<span id="cb3-2"><a href="#cb3-2" aria-hidden="true" tabindex="-1"></a>Len <span class="op">=</span> <span class="dv">128</span><span class="op">;</span> <span class="co">// Lengte van de ontvangstbuffer</span></span>
<span id="cb3-3"><a href="#cb3-3" aria-hidden="true" tabindex="-1"></a>Result <span class="op">=</span> reciveData <span class="op">(</span> <span class="op">(</span> <span class="dt">unsigned</span> <span class="dt">char</span> <span class="op">*</span> <span class="op">)</span> data<span class="op">,</span> Len<span class="op">,</span> PortID <span class="op">);;</span></span>
<span id="cb3-4"><a href="#cb3-4" aria-hidden="true" tabindex="-1"></a><span class="op">}</span></span></code></pre></div></td>
</tr>
</tbody>
</table>
 </td>
</tr>
</tbody>
</table>

3. Gegevens verzenden

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><div class="sourceCode" id="cb1"><pre class="sourceCode c"><code class="sourceCode c"><span id="cb1-1"><a href="#cb1-1" aria-hidden="true" tabindex="-1"></a><span class="pp">#include </span><span class="im">&quot;MacroInit.h&quot;</span></span>
<span id="cb1-2"><a href="#cb1-2" aria-hidden="true" tabindex="-1"></a><span class="dt">void</span> Macro_main <span class="op">(</span> IN <span class="op">*</span>p <span class="op">)</span></span>
<span id="cb1-3"><a href="#cb1-3" aria-hidden="true" tabindex="-1"></a><span class="op">{</span></span></code></pre></div>
<p>         MarcoInit</p>
<div class="sourceCode" id="cb2"><pre class="sourceCode c"><code class="sourceCode c"><span id="cb2-1"><a href="#cb2-1" aria-hidden="true" tabindex="-1"></a><span class="co">//ToDo</span></span>
<span id="cb2-2"><a href="#cb2-2" aria-hidden="true" tabindex="-1"></a><span class="dt">int</span> PortID<span class="op">,</span> Result<span class="op">,</span> Len<span class="op">,</span> CanType<span class="op">,</span> CanId<span class="op">,</span> i<span class="op">;</span></span>
<span id="cb2-3"><a href="#cb2-3" aria-hidden="true" tabindex="-1"></a><span class="dt">unsigned</span> <span class="dt">char</span> data<span class="op">[</span><span class="dv">128</span><span class="op">];</span></span>
<span id="cb2-4"><a href="#cb2-4" aria-hidden="true" tabindex="-1"></a>PortID <span class="op">=</span> <span class="dv">0</span><span class="op">;</span> <span class="co">//0：COM0 1：COM1</span></span>
<span id="cb2-5"><a href="#cb2-5" aria-hidden="true" tabindex="-1"></a>Result <span class="op">=</span> <span class="dv">0</span><span class="op">;</span></span>
<span id="cb2-6"><a href="#cb2-6" aria-hidden="true" tabindex="-1"></a>Len <span class="op">=</span> <span class="dv">127</span><span class="op">;</span> <span class="co">// Zendlengte</span></span>
<span id="cb2-7"><a href="#cb2-7" aria-hidden="true" tabindex="-1"></a>CanId <span class="op">=</span> <span class="bn">0x22</span><span class="op">;</span> <span class="co">//CAN ID</span></span>
<span id="cb2-8"><a href="#cb2-8" aria-hidden="true" tabindex="-1"></a>CanType <span class="op">=</span> <span class="dv">0</span><span class="op">;</span> <span class="co">// Frametype: standaardframe 0, uitgebreid frame 0x80000000</span></span>
<span id="cb2-9"><a href="#cb2-9" aria-hidden="true" tabindex="-1"></a><span class="cf">for</span> <span class="op">(</span> i <span class="op">=</span> <span class="dv">0</span><span class="op">;</span> i <span class="op">&lt;</span> <span class="dv">128</span><span class="op">;</span> <span class="op">++</span>i <span class="op">)</span></span>
<span id="cb2-10"><a href="#cb2-10" aria-hidden="true" tabindex="-1"></a><span class="op">{</span></span>
<span id="cb2-11"><a href="#cb2-11" aria-hidden="true" tabindex="-1"></a>data<span class="op">[</span>i<span class="op">]</span> <span class="op">=</span> i<span class="op">;</span></span>
<span id="cb2-12"><a href="#cb2-12" aria-hidden="true" tabindex="-1"></a><span class="op">}</span></span></code></pre></div>
<p>         Result = sendData ( ( unsigned char * ) data, Len, PortID, CanId, CanType );// Uitgebreid frame, COM0 verzendt gegevens, lengte 127, CAN ID 0x22</p>
<p>}</p></td>
</tr>
</tbody>
</table>
 </td>
</tr>
</tbody>
</table>
