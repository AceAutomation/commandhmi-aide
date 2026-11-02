# Can

Este controlador permite a las pantallas táctiles de la serie HM comunicarse con dispositivos CAN. Antes de usarlo, lea atentamente este capítulo y las especificaciones técnicas.

Cómo establecer la conexión con dispositivos CAN

**1. Conexión de hardware**

Cable de conexión:

RS485

|                  |      |                 |      |
|------------------|------|-----------------|------|
| **HM COM1/COM2** |      | **CAN**         |      |
| 1                | CANL | definido por el usuario | CANL |
| 4                | CANH | definido por el usuario | CANH |
| 5                | GND  | definido por el usuario | GND  |

**2. Ajustes de software**

La función CAN se usa llamando a las funciones del sistema desde un script

```c
int onCanxStart(PortID); Start can equipment
int onCanxstop (PortID); Off can equipment
int setBitrate (PortID); Set the can communication rate
int onCanxstop ( CanID, CanMask, PortID ); Can id filter
int reciveData ( data, Len, PortID ); Receive can data
int sendData ( data, Len, PortID, CanId, CanType ); Send can data
```

**3. Ejemplo**

 1, Ajustar la velocidad del puerto e iniciar el dispositivo CAN

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
<span id="cb2-4"><a href="#cb2-4" aria-hidden="true" tabindex="-1"></a>Bitrate <span class="op">=</span> <span class="dv">5</span><span class="op">*</span><span class="dv">1000</span><span class="op">;</span> <span class="co">// Velocidad del puerto 5k; rango de ajuste de 5k, 10k, 20k a 1M</span></span>
<span id="cb2-5"><a href="#cb2-5" aria-hidden="true" tabindex="-1"></a>Result <span class="op">=</span> <span class="dv">0</span><span class="op">;</span></span></code></pre></div>
<p>         Result = setBitrate ( Bitrate, PortID );    // COM0: velocidad de comunicación 5000; devuelve 0 si es correcto y un valor distinto de 0 en caso de error</p>
<div class="sourceCode" id="cb3"><pre class="sourceCode c"><code class="sourceCode c"><span id="cb3-1"><a href="#cb3-1" aria-hidden="true" tabindex="-1"></a>Result <span class="op">=</span> onCanxStart <span class="op">(</span> PortID <span class="op">);</span> <span class="co">// Devuelve 0 si es correcto, distinto de 0 en caso de error</span></span>
<span id="cb3-2"><a href="#cb3-2" aria-hidden="true" tabindex="-1"></a><span class="op">}</span></span></code></pre></div></td>
</tr>
</tbody>
</table>
 </td>
</tr>
</tbody>
</table>

2, Recibir datos

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
<p>    unsigned data[128];                // Búfer de recepción de datos</p>
<div class="sourceCode" id="cb3"><pre class="sourceCode c"><code class="sourceCode c"><span id="cb3-1"><a href="#cb3-1" aria-hidden="true" tabindex="-1"></a>PortID <span class="op">=</span> <span class="dv">0</span><span class="op">;</span> <span class="co">//0：COM0 1：COM1</span></span>
<span id="cb3-2"><a href="#cb3-2" aria-hidden="true" tabindex="-1"></a>Len <span class="op">=</span> <span class="dv">128</span><span class="op">;</span> <span class="co">// Longitud del búfer de recepción</span></span>
<span id="cb3-3"><a href="#cb3-3" aria-hidden="true" tabindex="-1"></a>Result <span class="op">=</span> reciveData <span class="op">(</span> <span class="op">(</span> <span class="dt">unsigned</span> <span class="dt">char</span> <span class="op">*</span> <span class="op">)</span> data<span class="op">,</span> Len<span class="op">,</span> PortID <span class="op">);;</span></span>
<span id="cb3-4"><a href="#cb3-4" aria-hidden="true" tabindex="-1"></a><span class="op">}</span></span></code></pre></div></td>
</tr>
</tbody>
</table>
 </td>
</tr>
</tbody>
</table>

3, Enviar datos

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
<span id="cb2-6"><a href="#cb2-6" aria-hidden="true" tabindex="-1"></a>Len <span class="op">=</span> <span class="dv">127</span><span class="op">;</span> <span class="co">// Longitud de transmisión</span></span>
<span id="cb2-7"><a href="#cb2-7" aria-hidden="true" tabindex="-1"></a>CanId <span class="op">=</span> <span class="bn">0x22</span><span class="op">;</span> <span class="co">//CAN ID</span></span>
<span id="cb2-8"><a href="#cb2-8" aria-hidden="true" tabindex="-1"></a>CanType <span class="op">=</span> <span class="dv">0</span><span class="op">;</span> <span class="co">// Tipo de trama: trama estándar: 0, trama extendida: 0x80000000</span></span>
<span id="cb2-9"><a href="#cb2-9" aria-hidden="true" tabindex="-1"></a><span class="cf">for</span> <span class="op">(</span> i <span class="op">=</span> <span class="dv">0</span><span class="op">;</span> i <span class="op">&lt;</span> <span class="dv">128</span><span class="op">;</span> <span class="op">++</span>i <span class="op">)</span></span>
<span id="cb2-10"><a href="#cb2-10" aria-hidden="true" tabindex="-1"></a><span class="op">{</span></span>
<span id="cb2-11"><a href="#cb2-11" aria-hidden="true" tabindex="-1"></a>data<span class="op">[</span>i<span class="op">]</span> <span class="op">=</span> i<span class="op">;</span></span>
<span id="cb2-12"><a href="#cb2-12" aria-hidden="true" tabindex="-1"></a><span class="op">}</span></span></code></pre></div>
<p>         Result = sendData ( ( unsigned char * ) data, Len, PortID, CanId, CanType );// Trama extendida, COM0 envía datos, longitud 127, CAN ID 0x22</p>
<p>}</p></td>
</tr>
</tbody>
</table>
 </td>
</tr>
</tbody>
</table>
