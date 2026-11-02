# LW

LW

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>address</th>
<th>instruction</th>
<th>Notes</th>
<th>read and write properties</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>59010~59057</td>
<td>In the extended mode, the communication of the specified station number is disabled.Corresponding station number 0~255,<br />
each address corresponds to 16 station numbers, 59010 means station number 0~15, and so onThe X-th bit is 1, allowing the communication with the X station number, and when it is 0,<br />
the communication with the X station number is closed.</td>
<td>COM1: 59010~59025<br />
COM2: 59026~59041<br />
COM3: 59106~59121<br />
Ethernet: 59042~59057</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>59058~59105</td>
<td>Station number communication status indication, corresponding to station number 0~255.<br />
each address corresponds to 16 station numbers, 59058 means station number 0~15, and so on the X bit is 1,<br />
the station number communication is abnormal; bit is 0, the station number communication is normal.</td>
<td>COM1: 59058~59073<br />
COM2: 59074~59089<br />
COM3: 59154~59169<br />
Ethernet: 59090~59105</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60000</td>
<td>local time seconds</td>
<td>Bcd code, valid value range 0-59</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60001</td>
<td>local time</td>
<td>Bcd code, valid value range 0-59</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60002</td>
<td>local time</td>
<td>Bcd code, valid value range 0-23</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60003</td>
<td>local time day</td>
<td>Bcd code, valid value range 1-31</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60004</td>
<td>local time month</td>
<td>Bcd code, valid value range 1-12</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60005</td>
<td>local time year</td>
<td>Bcd code, valid value range 0-9999</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60006</td>
<td>local time week</td>
<td>Bcd code, valid value range 1-7</td>
<td>R</td>
</tr>
<tr class="even">
<td>60007</td>
<td>system runtime</td>
<td>The time the system has been running, hours</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60008</td>
<td>system running time</td>
<td>System elapsed time, minutes</td>
<td>R</td>
</tr>
<tr class="even">
<td>60009</td>
<td>System runtime in seconds</td>
<td>System elapsed time, seconds</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60010</td>
<td>Current screen window number</td>
<td>The serial number of the current screen</td>
<td>R</td>
</tr>
<tr class="even">
<td>60012</td>
<td>current language</td>
<td>Corresponding language serial number</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60013</td>
<td>Numerical input allowable upper limit value</td>
<td>When the custom keyboard pops up, the upper limit of the allowed input is displayed in ASCII</td>
<td>R</td>
</tr>
<tr class="even">
<td>60023</td>
<td>Numerical input allowable lower limit value</td>
<td>When the custom keyboard pops up, the lower limit of the allowed input is displayed in ASCII</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60033</td>
<td>The input data content displayed on the keyboard</td>
<td>The input data content displayed on the keyboard, the characters input from the keyboard, ASCII display</td>
<td>R</td>
</tr>
<tr class="even">
<td>60065</td>
<td>The current system login user</td>
<td>current user serial number</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60066</td>
<td>Current system login user password</td>
<td>Display the current user's password, 16 characters, ASCII display</td>
<td>R</td>
</tr>
<tr class="even">
<td>60074</td>
<td>The current system login user name</td>
<td>Display the current user name, 32 characters, ASCII display</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60090</td>
<td>Whether user 1 is enabled</td>
<td>0 - not enabled, 1 - enabled</td>
<td>R</td>
</tr>
<tr class="even">
<td>60091</td>
<td>Whether user 2 is enabled</td>
<td>0 - not enabled, 1 - enabled</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60092</td>
<td>Whether user 3 is enabled</td>
<td>0 - not enabled, 1 - enabled</td>
<td>R</td>
</tr>
<tr class="even">
<td>60093</td>
<td>Whether user 4 is enabled</td>
<td>0 - not enabled, 1 - enabled</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60094</td>
<td>Whether user 5 is enabled</td>
<td>0 - not enabled, 1 - enabled</td>
<td>R</td>
</tr>
<tr class="even">
<td>60095</td>
<td>Whether user 6 is enabled</td>
<td>0 - not enabled, 1 - enabled</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60096</td>
<td>Whether user 7 is enabled</td>
<td>0 - not enabled, 1 - enabled</td>
<td>R</td>
</tr>
<tr class="even">
<td>60097</td>
<td>Whether user 8 is enabled</td>
<td>0 - not enabled, 1 - enabled</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60098</td>
<td>User 1 first name</td>
<td>32 characters, ASCII display</td>
<td>R</td>
</tr>
<tr class="even">
<td>60114</td>
<td>User 2 first name</td>
<td>32 characters, ASCII display</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60130</td>
<td>User 3 name</td>
<td>32 characters, ASCII display</td>
<td>R</td>
</tr>
<tr class="even">
<td>60146</td>
<td>User 4 first name</td>
<td>32 characters, ASCII display</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60162</td>
<td>User 5 name</td>
<td>32 characters, ASCII display</td>
<td>R</td>
</tr>
<tr class="even">
<td>60178</td>
<td>User 6 name</td>
<td>32 characters, ASCII display</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60194</td>
<td>User 7 first name</td>
<td>32 characters, ASCII display</td>
<td>R</td>
</tr>
<tr class="even">
<td>60210</td>
<td>User 8 first name</td>
<td>32 characters, ASCII display</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60226</td>
<td>User 1 password</td>
<td>16 characters, ASCII display</td>
<td>R</td>
</tr>
<tr class="even">
<td>60234</td>
<td>User 2 password</td>
<td>16 characters, ASCII display</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60242</td>
<td>User 3 password</td>
<td>16 characters, ASCII display</td>
<td>R</td>
</tr>
<tr class="even">
<td>60250</td>
<td>User 4 password</td>
<td>16 characters, ASCII display</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60258</td>
<td>User 5 password</td>
<td>16 characters, ASCII display</td>
<td>R</td>
</tr>
<tr class="even">
<td>60266</td>
<td>User 6 password</td>
<td>16 characters, ASCII display</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60274</td>
<td>User 7 password</td>
<td>16 characters, ASCII display</td>
<td>R</td>
</tr>
<tr class="even">
<td>60282</td>
<td>User 8 password</td>
<td>16 characters, ASCII display</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60290</td>
<td>screen saver time</td>
<td>Display the screen saver time specified during configuration, the setting range is 0~60</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60291</td>
<td>Indicator flashing cycle</td>
<td>The blinking period of the indicator light control, the minimum value is 0.1, the unit is s</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60292</td>
<td>The position of the X when touched</td>
<td>The position of the X coordinate when touched</td>
<td>R</td>
</tr>
<tr class="even">
<td>60293</td>
<td>Y's position when touched</td>
<td>The position of the Y coordinate when touched</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60294</td>
<td>The position of the X when the touch leaves</td>
<td>The position of the X coordinate when the touch leaves</td>
<td>R</td>
</tr>
<tr class="even">
<td>60295</td>
<td>The position of Y when the touch leaves</td>
<td>The position of the Y coordinate when the touch leaves</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60296</td>
<td>touch state</td>
<td>1-touch, 0-release</td>
<td>R</td>
</tr>
<tr class="even">
<td>60297</td>
<td>Checkout of COM1</td>
<td>Communication parameters, calibration, 0-NONE, 1-EVEN, 2-ODD</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60298</td>
<td>Baud rate of COM1</td>
<td>Communication parameters, baud rate, 0-1200, 1-2400, 2-4800, 3-9600, 4-19200, 5-38400, 6-57600, 7-115200</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60299</td>
<td>stop bit of COM1</td>
<td>Communication parameters, stop bits, 0-1stops, 1-2stops</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60300</td>
<td>Data length of COM1</td>
<td>Communication parameters, data length, 0-7bits, 1-8bits</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60301</td>
<td>HMI address of COM1</td>
<td>Communication parameters, HMI address</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60302</td>
<td>PLC address of COM1</td>
<td>Communication parameters, PLC address</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60303</td>
<td>COM1 PLC consecutive address interval</td>
<td>The length of the maximum continuous address that can be read in a single communication</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60304</td>
<td>COM1 communication time</td>
<td>Communication delay time</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60305</td>
<td>COM1 retries</td>
<td>The number of times the system resends when the communication is abnormal</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60306</td>
<td>COM1 address mode</td>
<td>Address mode, 0-standard mode, 1-extended mode</td>
<td>R</td>
</tr>
<tr class="even">
<td>60307</td>
<td>COM1 communication timeout time</td>
<td>Set the communication timeout time, in ms</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60308</td>
<td>COM1 communication current wait time</td>
<td>The current waiting time of communication, in ms</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60309</td>
<td>COM1 HMI location</td>
<td>0-local 1-remote</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60312</td>
<td>Checksum of COM2</td>
<td>Communication parameters, calibration, 0-NONE, 1-EVEN, 2-ODD</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60313</td>
<td>Baud rate of COM2</td>
<td>Communication parameters, baud rate, 0-1200, 1-2400, 2-4800, 3-9600, 4-19200, 5-38400, 6-57600, 7-115200</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60314</td>
<td>stop bit of COM2</td>
<td>Communication parameters, stop bits, 0-1stops, 1-2stops</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60315</td>
<td>Data length of COM2</td>
<td>Communication parameters, data length, 0-7bits, 1-8bits</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60316</td>
<td>HMI address of COM2</td>
<td>Communication parameters, HMI address</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60317</td>
<td>PLC address of COM2</td>
<td>Communication parameters, PLC address</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60318</td>
<td>COM2 PLC continuous address interval</td>
<td>The length of the maximum continuous address that can be read in a single communication</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60319</td>
<td>COM2 communication time</td>
<td>Communication delay time</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60320</td>
<td>COM2 retries</td>
<td>The number of times the system resends when the communication is abnormal</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60321</td>
<td>COM2 address mode</td>
<td>Address mode, 0-standard mode, 1-extended mode</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60322</td>
<td>COM2 communication timeout time</td>
<td>Set the communication timeout time, in ms</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60323</td>
<td>COM2 communication current wait time</td>
<td>The current waiting time of communication, in ms</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60324</td>
<td>COM2 HMI location</td>
<td>0-local, 1-remote</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61270</td>
<td>Checksum of COM3</td>
<td>Communication parameters, calibration, 0-NONE, 1-EVEN, 2-ODD</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61271</td>
<td>Baud rate of COM3</td>
<td>Communication parameters, baud rate, 0-1200, 1-2400, 2-4800, 3-9600, 4-19200, 5-38400, 6-57600, 7-115200</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61272</td>
<td>stop bit of COM3</td>
<td>Communication parameters, stop bits, 0-1stops, 1-2stops</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61273</td>
<td>Data length of COM3</td>
<td>Communication parameters, data length, 0-7bits, 1-8bits/td&gt;</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61274</td>
<td>HMI address of COM3</td>
<td>Communication parameters, HMI address</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61275</td>
<td>PLC address of COM3</td>
<td>Communication parameters, PLC address</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61276</td>
<td>COM3 PLC continuous address interval</td>
<td>The length of the maximum continuous address that can be read in a single communication</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61277</td>
<td>COM3 communication time</td>
<td>Communication delay time</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61278</td>
<td>COM3 retries</td>
<td>The number of times the system resends when the communication is abnormal</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61279</td>
<td>COM3 address mode</td>
<td>Address mode, 0-standard mode, 1-extended mode</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61280</td>
<td>COM3 communication timeout time</td>
<td>Set the communication timeout time, in ms</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61281</td>
<td>COM3 communication current wait time</td>
<td>The current waiting time of communication, in ms</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61282</td>
<td>COM3 HMI location</td>
<td>0-local, 1-remote</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60327</td>
<td>Number of historical alarms</td>
<td>The total number of historical alarms that occurred that were recorded</td>
<td>R/double word</td>
</tr>
<tr class="even">
<td>60329</td>
<td>Number of historical records</td>
<td>The total number of historical data records recorded</td>
<td>R/double word</td>
</tr>
<tr class="odd">
<td>60333</td>
<td>keyboard language switch</td>
<td>1-Chinese keyboard, 0-English keyboard, for standard keyboard</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60334</td>
<td>CPU usage</td>
<td>CPU runtime usage of the current system</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60335</td>
<td>The current brightness value of the backlight</td>
<td>The current brightness value of the backlight (140~450)</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60337</td>
<td>Current project creation time year</td>
<td>Current project file creation time year</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60338</td>
<td>Current project creation time month</td>
<td>Current project file creation time month</td>
<td>R</td>
</tr>
<tr class="even">
<td>60339</td>
<td>Current project creation date and time</td>
<td>The current project file creation date and time</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60340</td>
<td>current user language</td>
<td>set current language</td>
<td>W</td>
</tr>
<tr class="even">
<td>60359</td>
<td>When equal to 1, copy the historical alarms of the specified serial number range to the U disk</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60361</td>
<td>When equal to 1, copy the historical alarms of the specified time range to the U disk</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60363</td>
<td>Export historical alarm start sequence number</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60365</td>
<td>Export historical alarm end sequence number</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60367</td>
<td>Export history alarm start time</td>
<td>The length is 6 characters, which are the year, month, day, hour, minute and second.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60373</td>
<td>Export historical alarm end time</td>
<td>The length is 6 characters, which are the year, month, day, hour, minute and second.</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60379</td>
<td>File name when exporting historical alarms to U disk</td>
<td>22 characters long</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60408</td>
<td>The current group number control address of the historical data</td>
<td>Specify the current group number of historical data</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60409</td>
<td>When equal to 1, copy the historical data of the specified serial number range to the U disk</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60411</td>
<td>When equal to 1, copy the historical data of the specified time range to the U disk</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60413</td>
<td>Export historical data start sequence number</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60415</td>
<td>Export historical data end sequence number</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60417</td>
<td>Export historical data start time</td>
<td>The length is 6 characters, which are the year, month, day, hour, minute and second.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60423</td>
<td>End time of exporting historical data</td>
<td>The length is 6 characters, which are the year, month, day, hour, minute and second.</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60429</td>
<td>File name when exporting historical data to U disk</td>
<td>24 characters long</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60441</td>
<td>Modify User 1 Password Cache</td>
<td>16 characters long, ASCII display</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60449</td>
<td>Enable to modify the password of user 1</td>
<td>When it is 1, the password of user 1 will be changed to the password of the cache area, and it will be reset automatically after setting.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60451</td>
<td>Modify User 2 Password Cache</td>
<td>16 characters long, ASCII display</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60459</td>
<td>Enable to modify the password of user 2</td>
<td>When it is 1, the password of user 2 will be changed to the password of the cache area, and it will be reset automatically after setting.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60461</td>
<td>Modify User 3 Password Cache</td>
<td>16 characters long, ASCII display</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60469</td>
<td>Enable to modify the password of user 3</td>
<td>When it is 1, the password of user 3 will be changed to the password of the cache area, and it will be reset automatically after setting.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60471</td>
<td>Modify User 4 Password Cache</td>
<td>16 characters long, ASCII display</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60479</td>
<td>Enable to modify the password of user 4</td>
<td>When it is 1, the password of user 4 will be changed to the password of the cache area, and it will be reset automatically after setting.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60481</td>
<td>Modify User 5 Password Cache</td>
<td>16 characters long, ASCII display</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60489</td>
<td>Enable to modify the password of user 5</td>
<td>When it is 1, the password of user 5 will be changed to the password of the cache area, and it will be reset automatically after setting.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60491</td>
<td>Modify User 6 Password Cache</td>
<td>16 characters long, ASCII display</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60499</td>
<td>Enable to modify the password of user 6</td>
<td>When it is 1, the password of user 6 will be changed to the password of the cache area, and it will be reset automatically after setting.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60501</td>
<td>Modify user 7 password cache</td>
<td>16 characters long, ASCII display</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60509</td>
<td>Enable to modify the password of user 7</td>
<td>When it is 1, the password of user 7 will be changed to the password of the cache area, and it will be reset automatically after setting.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60511</td>
<td>Modify User 8 Password Cache</td>
<td>16 characters long, ASCII display</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60519</td>
<td>Enable to modify the password of user 8</td>
<td>When it is 1, the password of user 8 will be changed to the password of the cache area, and it will be reset automatically after setting.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60520</td>
<td>HMI model</td>
<td>40 characters</td>
<td>R</td>
</tr>
<tr class="even">
<td>60540</td>
<td>bootloader version number</td>
<td>40 characters</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60560</td>
<td>OS version number</td>
<td>40 characters</td>
<td>R</td>
</tr>
<tr class="even">
<td>60580</td>
<td>software version number</td>
<td>40 characters</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60600</td>
<td>Operation record enable</td>
<td>When it is 1, the operation record is allowed to be recorded</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60601</td>
<td>Number of operation records</td>
<td>Display the number of current operation records</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60602</td>
<td>Screen capture enabled</td>
<td>When it is 1, enable screen capture and reset automatically after setting</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60603</td>
<td>Screenshot storage location</td>
<td>0-U disk</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60604</td>
<td>Enable HMI protection</td>
<td>When 1, use HMI protection</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60605</td>
<td>Set the total number of password levels for HMI protection</td>
<td>Set the total number of password levels for HMI protection, up to 15 passwords can be set</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60606-60835</td>
<td>Setting the lifetime of the HMI protection</td>
<td>60606-60628 is the year, month, day, hour, minute, second and expiration prompt screen of the level 1 password and the unlock password (the password length is 16 characters)<br />
60629-60651 is the year, month, day, hour, minute, second and expiration prompt screen of the level 2 password, and the unlock password (password length is 16 characters)<br />
60652-60674 are the year, month, day, hour, minute, second, and expiration prompt screens for level 3 passwords, as well as the unlock password (password length is 16 characters)<br />
60675-60697 is the year, month, day, hour, minute, second and expiration prompt screen of the 4-level password and the unlock password (password length is 16 characters)<br />
60698-60720 is the year, month, day, hour, minute, second and expiration prompt screen of the 5-level password and the unlock password (the password length is 16 characters)<br />
60721-60743 are the year, month, day, hour, minute, second and expiration prompt screen of the 6-level password and the unlock password (password length is 16 characters)<br />
60744-60766 is the year, month, day, hour, minute, second and expiration prompt screen of the 7-level password and the unlock password (the password length is 16 characters)<br />
60767-60789 is the year, month, day, hour, minute, second and expiration prompt screen of the 8-level password and the unlock password (the password length is 16 characters)<br />
60790-60812 is the year, month, day, hour, minute, second and expiration prompt screen of the 9-level password and the unlock password (password length is 16 characters)<br />
60813-60835 is the year, month, day, hour, minute, second and expiration prompt screen of the 10-level password and the unlock password (the password length is 16 characters)</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>63000-63114</td>
<td>Setting the lifetime of the HMI protection</td>
<td>63000-63022 is the year, month, day, hour, minute, second and expiration prompt screen of the 11-level password and the unlock password (the password length is 16 characters)<br />
63023-63045 is the year, month, day, hour, minute, second and expiration prompt screen of the 12-level password and the unlock password (password length is 16 characters)<br />
63046-63068 is the year, month, day, hour, minute, second and expiration prompt screen of the 13-level password and the unlock password (password length is 16 characters)<br />
63069-63091 is the year, month, day, hour, minute, second and expiration prompt screen of the 14-level password and the unlock password (the password length is 16 characters)<br />
63092-63114 are the year, month, day, hour, minute, second and expiration prompt screens for the 15-level password and the unlock password (password length is 16 characters)</td>
<td></td>
</tr>
<tr class="odd">
<td>63115~63130</td>
<td>The highest level password to modify the input address</td>
<td>63115~63131 The highest level password modification address (password length is 16 characters), after the input is completed, enter 1 in LW63131 to make the currently set password effective</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>63131</td>
<td>Highest level password enable address</td>
<td>63115~63130 After the highest level password input is completed, enter 1 in this address to make the highest level password effective</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60836</td>
<td>Enable store to HMI</td>
<td>When it is 1, the HMI protection setting is stored in the HMI, and the setting is automatically reset.</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60837</td>
<td>Initialize HMI protection state</td>
<td>Reset the HMI protection to the initial state. Unlocked users need to unlock again</td>
<td>W</td>
</tr>
<tr class="odd">
<td>60997</td>
<td>USB input function assignment.</td>
<td>Default is 0, USB keyboard input or USB mouse operationWhen it is 1, it is used for scanning gun scanning input</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60998</td>
<td>USB two-digit barcode scanning end symbol definition 0-ENTER, 1-TAB+ENTER</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60999</td>
<td>USB two-digit barcode scan code length</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61000 - 61127</td>
<td>Two-digit barcode scanning code storage and use</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61128</td>
<td>Use of printer parameters</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61138</td>
<td>Import recipe source recipe ID number</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61139</td>
<td>Import recipe destination recipe ID number</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61140</td>
<td>Clear recipe ID number</td>
<td>-1 when the initial value is displayed using a 16-bit integer; otherwise, 65535</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61141</td>
<td>Switch the current recipe group number when the HMI is running</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61143</td>
<td>Specify the group number when importing and exporting the formula U disk</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61146</td>
<td>Specifies the window number to print when the register triggers printing</td>
<td>Enter the serial number of the window to be printed, set LB60175 to trigger printing, and automatically reset</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>62020-62039</td>
<td>Current recipe name</td>
<td>ASCII display control, unicode encoding, length 20,Display the current recipe name</td>
<td>R</td>
</tr>
<tr class="odd">
<td>62040</td>
<td>User login level selection</td>
<td>Set the user level that needs to be logged in, here corresponds to the user level checked in the "touch screen parameter setting" ?? "user password setting" option</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>62041~62056</td>
<td>User login password input address</td>
<td>Correctly enter 62040 to set the corresponding password of the user level. The highest authority password can unlock the current user level of all levels (the password length is 16 characters), and complete the user login operation.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>62057</td>
<td>HMI delay times limit register</td>
<td>Check the delay option in HMI protection settings, you can modify the number of delays here, the default value is 1</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>63141~63146</td>
<td>Dynamic Password Expiration Time Settings</td>
<td>Year, month, day, hour, minute, second: LW63141~63146 Data type: 16-bit integer, set LB60182 after setting the date, the setting will take effect and reset automatically</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>63147~63152</td>
<td>Dynamic password key setting address</td>
<td>Modify the dynamic password key, set address: LW63147 Data type: ASCII Length: 6, set LB60179 to take effect after setting, and reset automatically</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>63153~63184</td>
<td>Formula Name Modification</td>
<td>ASCII input control, length 32, modified LB60180 take effect IP, port number, station number After the setting is completed, set LB60178 to take effect</td>
<td>W</td>
</tr>
<tr class="odd">
<td>63186~63189</td>
<td>IP address of the Ethernet device</td>
<td>The IP address of the Ethernet device in the standard mode, data type: 16-bit integer IP, port number, station number After the setting is completed, set LB60178 to take effect</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>63190</td>
<td>Station number of the Ethernet device</td>
<td>The station number of the Ethernet device in standard mode, data type: 16-bit integer IP, port number, and station number are set to take effect after setting LB60178</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>63191</td>
<td>Port number of the Ethernet device</td>
<td>The port number of the Ethernet device in standard mode, data type: 16-bit integer IP, port number, station number After the setting is completed, set LB60178 to take effect</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60838~60853</td>
<td>Currently logged in user name</td>
<td>User rights function, display the current login user name, control type: ASCII display control, length 32</td>
<td>R</td>
</tr>
<tr class="odd">
<td>63200~63215</td>
<td>Currently logged in user group</td>
<td>User rights function, displays the user group name of the currently logged in user (the first group to which he/she belongs), control type: ASCII display control, length 32</td>
<td>R</td>
</tr>
</tbody>
</table>
