# Pipeline

The function of the control is to set the line diameter according to the set location of the specified control

<img src="conduit.files/image004.jpg" width="488" alt="ScreenShot00831.jpg" />

Pipeline general dialog

Ø  Style: set line display style, style has the following several effects, display effect reference "[style](#style)"

Ø Gradual layer: setting up the line of the pipeline to display the effect, the layer has the following results, the display effect is refer to the "[gradual layer](#Graduallayer)"

Ø Diameter: the diameter of the pipeline is set, which is used to change the diameter of the pipeline“[diameter](#diameter)”.

Ø Thickness: the thickness of the pipeline is set, and the thickness of the pipe is added on the basis of the diameter of the pipeline. The effect is referenced "[thickness](#thickness)"

Ø Edge: the color of the pipeline thickness is set, which is the color of the pipeline edge when the pipeline thickness is 0

Ø  Pipe wall/content: set the line main display color

Ø Wall/content color variable

<img src="conduit.files/image005.jpg" width="451" alt="ScreenShot00832.jpg" />

l  See color: when the pipe wall/content color variable function is enabled, the line displays the color, the color content is selected from the pipe wall/content, tube wall/content color \# 2, tube wall/content color \# 3, which is only shown in the configuration software, and the position control of the color controlled word is displayed in the actual operation

l  Tube wall/content color \# 2, tube wall/content color \# 3: set the different colors of the line

l  Scintillation control: control the line flashing

Ø  Flow control：

l  Control word: word, double word

l  Flow effect: (note that only after the pipe page is set to enable the flow effect of the pipe, the following types can be applied to the pipes that enable the flow effect).

Preset type: setting pipe flow effect

Default color: set the flow color of the pipe

The preset length ratio is (7) : the length ratio of the pipe is set

All use the preset type, color, and length: choose to apply a type to all the pipes that enable the flow effect of the pipe page

Ø Control word：

<img src="conduit.files/image006.jpg" width="450" alt="ScreenShot00833.jpg" />

The user enables the control of the tube wall/content color variable and the effect control of the effect of the effect control, which is different from the different display effect of a control control of the selected register. Take lw0 as an example

<table>
<colgroup>
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>register</strong></p></td>
<td><p><strong>No. 0</strong></p></td>
<td><p><strong>No. 1</strong></p></td>
<td><p><strong>No. 2</strong></p></td>
<td><p><strong>No.3</strong></p></td>
<td><p><strong>No. 4</strong></p></td>
<td><p><strong>No. 5</strong></p></td>
<td><p><strong>No. 6</strong></p></td>
<td><p><strong>No. 7</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>LW0</strong></p>
<p><strong>（The corresponding bit is on on）</strong></p></td>
<td><p>Set the tube wall color</p>
<p>Tube wall/content color #3</p></td>
<td><p>Set the tube wall color</p>
<p>Tube wall/content color #3</p></td>
<td><p>Line flashing</p>
<p>The current two are on or offColor is the color of the tube wall/content set</p>
<p>The current two are only set up one time, the line color is inThe pipeline content is switched between the pipeline content #</p></td>
<td><p>Pipeline flow</p></td>
<td><p>retention</p></td>
<td><p>retention</p></td>
<td><p>retention</p></td>
<td><p>retention</p></td>
</tr>
</tbody>
</table>

Pipe setting interface：

<img src="conduit.files/image007.jpg" width="488" alt="ScreenShot00834.jpg" />

Ø  Pipe setting interface

l  X1，Y1，X2，Y2：

The coordinate point of the pipe, the left coordinate (x1,y1), the right coordinate (x2, y2).

The user can modify the tube coordinate, need to be careful, the transverse tube can only modify the x coordinate, the longitudinal tube can only modify the y coordinate, the Angle coordinate cannot be modified, but can modify the Angle coordinate style type。

l  Flow effect: the user can set up each pipe to display different kinds of flow effect, display color, length ratio, etc.

If the user USES the same type of display effect, you can only enable the flow effect here, using all the preset functions in the general interface, and can be applied to the current control for all the pipes that start the flow effect.

The display interface is the same as his control, which can refer to the "bit switch" display page.

<span id="style"></span>style：

style 1<img src="conduit.files/image008.jpg" width="172" alt="ScreenShot00835.jpg" /> style 2<img src="conduit.files/image009.jpg" width="178" alt="ScreenShot00836.jpg" /> style 3<img src="conduit.files/image008.jpg" width="179" alt="ScreenShot00495.jpg" /> style 4<img src="conduit.files/image009.jpg" width="177" alt="ScreenShot00496.jpg" /> style 5<img src="conduit.files/image011.jpg" width="187" alt="2019_7_30_11_37_36.jpg" />

<span id="Graduallayer"></span>Gradual layer：

Pure color <img src="conduit.files/image011.jpg" width="182" alt="ScreenShot00498.jpg" /> Three-dimensional style 1<img src="conduit.files/image012.jpg" width="180" alt="ScreenShot00499.jpg" /> Three-dimensional style 2<img src="conduit.files/image013.jpg" width="180" alt="ScreenShot00500.jpg" /> Three-dimensional style 3<img src="conduit.files/image014.jpg" width="179" alt="ScreenShot00501.jpg" />

<span id="diameter"></span>diameter：

diameter 10<img src="conduit.files/image015.jpg" width="157" alt="ScreenShot00506.jpg" /> diameter 20<img src="conduit.files/image016.jpg" width="188" alt="ScreenShot00507.jpg" /> diameter 30<img src="conduit.files/image017.jpg" width="220" alt="ScreenShot00508.jpg" />

<span id="thickness"></span>thickness：

thickness 0<img src="conduit.files/image018.jpg" width="183" alt="ScreenShot00502.jpg" /> thickness 1<img src="conduit.files/image019.jpg" width="174" alt="ScreenShot00505.jpg" /> thickness 4<img src="conduit.files/image020.jpg" width="178" alt="ScreenShot00503.jpg" /> thickness 8<img src="conduit.files/image021.jpg" width="187" alt="ScreenShot00504.jpg" />
