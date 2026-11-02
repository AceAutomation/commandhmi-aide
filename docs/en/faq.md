# FAQ & Solutions

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>       <strong>No.</strong></p></td>
<td colspan="2"><p><strong>Phenomenon</strong></p></td>
<td><p><strong>Reason analysis</strong></p></td>
<td><p><strong>Solution</strong></p></td>
</tr>
<tr class="even">
<td rowspan="6"><p><strong>Display</strong></p></td>
<td rowspan="5"><p>Black Screen</p></td>
<td rowspan="3"><p>Black screen once powered on</p></td>
<td><p>Power problems</p></td>
<td><p>1、Check the power supply connection; 2、Check the power type; change the type if it is not independent 24VDC（±20%）.</p></td>
</tr>
<tr class="odd">
<td><p>There is something wrong with the configuration project, such as wrong application of macro, including applying null pointer, wild pointer, off-normal array, and divisor of 0.</p></td>
<td><p>Dial the Dial switch 2 to ON and re-download configuration project to test simply; if macro runs improperly, debug it and apply correct macro programming methods.</p></td>
</tr>
<tr class="even">
<td><p>Main engine trouble: Flat cable corrosion of LCD, crystal oscillator problem, etc.</p></td>
<td><p>Contact to the after-sale service for depot repair.</p></td>
</tr>
<tr class="odd">
<td rowspan="2"><p>Sudden black screen during normal operation; or sometimes black screen, crash</p></td>
<td><p>Power problem</p></td>
<td><p>Check whether the power wire and the power are fine.</p></td>
</tr>
<tr class="even">
<td><p>Main engine trouble</p></td>
<td><p>Contact to the after-sale service for depot repair.</p></td>
</tr>
<tr class="odd">
<td colspan="2"><p>Lines on the screen, vertical or horizontal line</p></td>
<td><p>LCD failure</p></td>
<td><p>Contact to the after-sale service for depot repair if each screen has the line phenomenon.</p></td>
</tr>
<tr class="even">
<td rowspan="4"><p><strong>Touch</strong></p></td>
<td colspan="2" rowspan="2"><p>Slow touch response and difficulty to touch controls</p></td>
<td><p>Installation problem</p></td>
<td><p>1. Check whether the open whole is so small that it squeezes HMI and if so install it according to right hole size; 2. Check whether setscrews are too tight and ensure the stress of four corners as consistent as possible.</p></td>
</tr>
<tr class="odd">
<td><p>Improper configuration project</p></td>
<td><p>Too much configuration project message, background macros and over range screen variables and controls; modify the configuration program, add or reduce controls and screens reasonably.</p></td>
</tr>
<tr class="even">
<td colspan="2"><p>Touch failure</p></td>
<td><p>Coordinate adjustment or touch panel damage</p></td>
<td><p>1. Dial the dial switch on 1 to execute coordinate adjustment;</p>
<p>2. <span id="OLE_LINK4"></span><span id="OLE_LINK3"></span>Contact to the after-sale service for depot repair if the former doesn’t work.</p></td>
</tr>
<tr class="odd">
<td colspan="2"><p>Jump wire（In Keyboard, press A but display X or others）</p></td>
<td><p>Touch panel failure</p></td>
<td><p>Contact to the after-sale service for depot repair.</p></td>
</tr>
<tr class="even">
<td rowspan="9"><p><strong>Communication failure</strong></p></td>
<td rowspan="6"><p>Communication outage between HMI and controller</p></td>
<td rowspan="3"><p>Communication is unavailable all the time</p></td>
<td><p>Failure of communication devices  （PLC, SCM, etc.）</p></td>
<td><p>Ensure fine sate of communication port and rematch communication parameters.</p></td>
</tr>
<tr class="odd">
<td><p>Communication port failure of HMI</p></td>
<td><p>Contact to the after-sale service for depot repair.</p></td>
</tr>
<tr class="even">
<td><p>Disconnection of communication cable</p></td>
<td><p>Employ specific cable of CommandHMI as far as possible.</p></td>
</tr>
<tr class="odd">
<td rowspan="3"><p>Communication interrupt after a period time of normal operation</p></td>
<td><p>Communication wire connection appears corrosion and oxidation due to long-time operation.</p></td>
<td><p>Change communication wire or re-weld it.</p></td>
</tr>
<tr class="even">
<td><p>Environment interference</p></td>
<td><p>Shied interference source reasonably; employ shielded wire; proper ground connection</p></td>
</tr>
<tr class="odd">
<td><p>Main engine trouble of HMI（due to strong magnet and current or lightning at scene）</p></td>
<td><p>Contact to the after-sale service for depot repair.</p></td>
</tr>
<tr class="even">
<td colspan="2" rowspan="3"><p>HMI cannot connect PC and downloading is unavailable.</p></td>
<td><p>Wrong installation of PC USB driver</p></td>
<td><p>Select corresponding system driver and reinstall USB driver.</p></td>
</tr>
<tr class="odd">
<td><p>Size and model of HMI are inconsistent with the actual ones.</p></td>
<td><p>Modify and match the right model of HMI in configuration software.</p></td>
</tr>
<tr class="even">
<td><p>Damage of HMI downloading port</p></td>
<td><p>Contact to the after-sale service for depot repair. (check method: Connect another HMI with the same USB cable and PC to see whether downloading is available; if so, fault point locates on the USB communication port of HMI）</p></td>
</tr>
<tr class="odd">
<td rowspan="3"><p><strong>Application</strong></p></td>
<td colspan="2"><p>Unavailable configuration</p></td>
<td><p>Illegal control or macro in configuration</p></td>
<td><p>Modify the configuration</p></td>
</tr>
<tr class="even">
<td colspan="2"><p>Unsuccessful macro compilation</p></td>
<td><p>Installation directory of HM in environmental variables</p></td>
<td><p>Bring forward the installation directory of CommandHMI in environmental variables.</p></td>
</tr>
<tr class="odd">
<td colspan="2"><p>Off-line and On-line simulation cannot function in the meantime.</p></td>
<td><p>Run without administrator rights</p></td>
<td><p>Run CommandHMI as administrator</p></td>
</tr>
</tbody>
</table>
