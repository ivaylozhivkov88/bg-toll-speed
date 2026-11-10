<div align="center">

<img src="assets/banner.svg" alt="BG Toll Speed" width="100%"/>

<br/>

![Android](https://img.shields.io/badge/Android-5AA9FF?style=for-the-badge&logo=android&logoColor=white)
![Kotlin](https://img.shields.io/badge/Kotlin-5AA9FF?style=for-the-badge&logo=kotlin&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-5AA9FF?style=for-the-badge&logo=firebase&logoColor=white)
![Maps](https://img.shields.io/badge/Maps_and_GPS-4CC76A?style=for-the-badge&labelColor=0D1A2E&color=4CC76A)

**Warns Bulgarian drivers about average-speed sections and tells them how fast they can go.**

</div>

> **Showcase repository.** This page presents the product and the engineering behind it. The source code is private.

---

## How it works

Average-speed cameras measure the time between an entry and an exit camera. The app does the same maths on the phone, so the driver sees the average speed and the limit before the exit camera does.

<div align="center">
<img src="assets/screens/section-control.jpg" width="46%" alt="Section control explained"/>
<img src="assets/screens/overlay.jpg" width="46%" alt="Speed bubble over the map"/>
</div>

<div align="center">
<img src="assets/screens/virtual-gates.jpg" width="92%" alt="Virtual gates and tunnel handling"/>
</div>

## What it does

| | |
|---|---|
| **Section detection** | Recognises entry and exit of a section by direction and position |
| **Average speed** | Live average, current speed and the maximum you can still hold to the end |
| **Correct limits** | Limits by road type, such as 90 km/h on first-class roads and 140 on motorways |
| **Voice** | Spoken warnings before a section, before its end and a summary at the finish |
| **Speed bubble** | A floating bubble over Google Maps or Waze |
| **Runs in the background** | Keeps tracking with the screen off, in the background and on rotation |
| **Sections across Bulgaria** | Sections and directions stored in the cloud and updated without a new release |

## Engineering

| Area | Approach |
|---|---|
| Detection | Virtual gates: a perpendicular crossing test at entry and exit, real path length along the route polyline, and tunnel handling for lost GPS |
| Tracking | Foreground location service with a dedicated section detector and map controller |
| Data | Firestore repository for sections, with Python scripts that upload and validate new ones |
| Monetisation | Play Billing for a Pro tier, rewarded ads |
| Release | Release notes and store listings in Bulgarian and English |

## Design language

<table>
<tr>
<td bgcolor="#0D1A2E" width="130" align="center"><b><font color="#FFFFFF">#0D1A2E</font></b><br/><sub><font color="#FFFFFF">night</font></sub></td>
<td bgcolor="#5AA9FF" width="130" align="center"><b>#5AA9FF</b><br/><sub>route blue</sub></td>
<td bgcolor="#4CC76A" width="130" align="center"><b>#4CC76A</b><br/><sub>safe</sub></td>
<td bgcolor="#F39222" width="130" align="center"><b>#F39222</b><br/><sub>caution</sub></td>
<td bgcolor="#E2483F" width="130" align="center"><b><font color="#FFFFFF">#E2483F</font></b><br/><sub><font color="#FFFFFF">over limit</font></sub></td>
</tr>
</table>

A dashboard look for the car: dark blue background and a traffic-light palette, so one glance says whether you are safe.

---

<div align="center">

Built by [@ivaylozhivkov88](https://github.com/ivaylozhivkov88)

</div>
