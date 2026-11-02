# Scroll bar

The scroll bar is a control that is used to see the data of the table class control, which is convenient for users to browse the table data quickly. Only the following controls are supported only: alarm display, historical alarm display, formula data display, historical data display, operating log display

The control is used for the associated controls to display too much data, unable to display the complete situation once, and can be used to display the remaining part of the data

<img src="scrollbar.files/image004.jpg" width="859" alt="ScreenShot00819.jpg" />

Scroll bar dialog box

The control function is described in detail below (the control is mainly divided into two categories: scroll buttons and scroll bars)

Ø  Scroll bar: control table data refresh in a scroll bar

<img src="scrollbar.files/image005.jpg" width="859" alt="ScreenShot00820.jpg" />

l  Background color: setting control background color

l  Symbol color: set the control symbol color

l  Direction: set the scroll bar control to control the direction of the table data

n  Level: control table horizontal data display

n  Vertical data display control table

l  The associated object number, the current page exists in any of the controls mentioned in the previous section, can be associated with the corresponding control to achieve the effect of the control. If the current page does not have any of these controls, the error message will be prompted. "the associated object cannot be empty. The object number is the data in the upper left corner number of the control.

Take the historical data display as an example, which is the effect of the scroll bar control

There are 75 data in the current historical data display, and the historical data display and the scroll bar are all at the bottom

<img src="scrollbar.files/image008.jpg" width="585" alt="ScreenShot00822.jpg" />

Move the scroll bar to the middle position, and the data display is shown as shown below：

<img src="scrollbar.files/image008.jpg" width="585" alt="ScreenShot00822.jpg" />

Ø  Scroll button: button mode control table data refresh

<img src="scrollbar.files/image006.jpg" width="859" alt="ScreenShot00821.jpg" />

l Border color: set the border color of the control

l  Background color: setting control background color

l  Symbol color: set the color of the symbol in the control

l  direction

n  Level: control table level data display

n  Vertical: control table vertical mode data display

l  Associated object number: reference to the previous description

l Function key

n  The button interval, the spacing between the buttons

n  To the end/to the end: the mobile table data is at the start or end, as with the following two buttons, when the data is already in the starting or end location, and the click button will pop-up the dialog box prompt operation is invalid

n  Page/page/page/left page/right: move a page of pages each time

n  Top/down or left/right: move a data in the corresponding direction each time

n  Pause: if the current table data is in a changing state, clicking this button can stop the table data changes and again click back to the original state. If the current direction of the table is fixed, it will not change, click the button prompt, and the function is invalidTake the historical data display as an example, and the image below is the effect of the scroll button control

The current historical data display has 71 data

<img src="scrollbar.files/image008.jpg" width="585" alt="ScreenShot00822.jpg" />

If you click the stop button during the program runtime <img src="scrollbar.files/suspend.jpg" width="40" alt="suspend" />，Stop the table refresh and pop up the following dialog

<img src="scrollbar.files/image009.jpg" width="257" alt="ScreenShot00826.jpg" />

Click the stop button again <img src="scrollbar.files/suspend.jpg" width="40" alt="suspend" />，Refresh the table and pop up the following dialog

<img src="scrollbar.files/image010.jpg" width="265" alt="ScreenShot00827.jpg" />

When you click the button <img src="scrollbar.files/screenshot00849.jpg" width="44" />，The historical data display data is changed as shown below, and the data jumps to the beginning. Again, if you click on the tail button <img src="scrollbar.files/screenshot00850.jpg" width="32" />，Data jump to the end

<img src="scrollbar.files/image011.jpg" width="585" alt="ScreenShot00828.jpg" />

When you click the next page button <img src="scrollbar.files/screenshot00851.jpg" width="40" />，The historical data display is changed in the following diagram, the current historical data display, a page of up to 5 Numbers, and the historical data display displays the next 5 Numbers when the next page button is clicked. Again, click on the front page button <img src="scrollbar.files/image015.jpg" width="37" alt="ScreenShot00529.jpg" />，Show the number of five Numbers

<img src="scrollbar.files/image012.jpg" width="584" alt="2019_7_27_15_06_20.jpg" />

When you click on the button <img src="scrollbar.files/image017.jpg" width="40" alt="ScreenShot00530.jpg" />，The historical data display is shown in the following diagram, showing the number of 1 in the top, and the same thing, when you click on the button <img src="scrollbar.files/image018.jpg" width="37" alt="ScreenShot00532.jpg" />，The bottom shows a number of data

<img src="scrollbar.files/image013.jpg" width="584" alt="2019_7_27_15_06_54.jpg" />
