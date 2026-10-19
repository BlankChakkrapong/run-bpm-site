---
title: Privacy Policy — Run BPM
---

# นโยบายความเป็นส่วนตัว — Run BPM / Privacy Policy — Run BPM

> ปรับปรุงล่าสุด / Last updated: 18 ต.ค. 2026 (version 0.1.0)

---

## ภาษาไทย

Run BPM เป็นส่วนขยาย Chrome ที่ฟังเสียงของแท็บที่คุณเลือก แล้วบอกว่าจังหวะเพลง (BPM) เข้ากับจังหวะก้าววิ่ง (cadence) ของคุณไหม

### สรุปสั้น ๆ
- **ประมวลผลในเครื่องทั้งหมด** เสียงถูกวิเคราะห์ในเบราว์เซอร์ของคุณเท่านั้น
- **ไม่บันทึกเสียง** และไม่ส่งข้อมูลใด ๆ ออกนอกเครื่อง
- **ไม่มี analytics** ไม่มีบัญชีผู้ใช้ ไม่มีเซิร์ฟเวอร์ ไม่มีโฆษณา
- ส่วนขยายไม่ส่ง network request ใด ๆ (ฟอนต์และไฟล์ทั้งหมดอยู่ในตัวส่วนขยาย)

### เสียงจากแท็บ
- Run BPM เริ่มฟังเฉพาะเมื่อคุณกดปุ่ม "เริ่มฟังแท็บนี้" ในแท็บนั้นเอง ไม่มีการฟังอัตโนมัติ
- เสียงถูกส่งเข้าตัววิเคราะห์จังหวะในหน่วยความจำ ผลที่ได้คือตัวเลข BPM และค่าความมั่นใจ ตัวเสียงไม่ถูกเขียนลงดิสก์และไม่ถูกส่งไปที่ใด
- การฟังหยุดเมื่อคุณกด "หยุดฟัง" ปิดแท็บนั้น หรือเริ่มฟังแท็บอื่น

### ข้อมูลที่เก็บในเครื่อง

| ข้อมูล | ที่เก็บ | อยู่นานแค่ไหน |
|---|---|---|
| cadence เป้าหมาย, ช่วงคลาดเคลื่อน (tolerance), ภาษาที่เลือก | `chrome.storage.local` | จนกว่าคุณจะถอนการติดตั้งส่วนขยาย |
| สถานะการฟังชั่วคราว: แท็บที่กำลังฟัง (หมายเลขและชื่อแท็บ), ค่า BPM ล่าสุด, ค่าที่คุณเคาะเอง | `chrome.storage.session` | หายเมื่อปิดเบราว์เซอร์ |

ข้อมูลทั้งหมดนี้อยู่ในเครื่องของคุณเท่านั้น Run BPM ไม่ได้ซิงก์ข้ามอุปกรณ์ (ไม่ใช้ `chrome.storage.sync`)

### สิทธิ์ที่ขอ
- `tabCapture` — จับเสียงของแท็บที่คุณกดเริ่ม เพื่อวิเคราะห์จังหวะ
- `offscreen` — เปิดหน้าซ่อนสำหรับประมวลผลเสียง (service worker ประมวลผลเสียงเองไม่ได้)
- `activeTab` — เข้าถึงแท็บที่คุณใช้งานอยู่ตอนกดไอคอน เพื่อระบุแท็บที่จะฟังและแสดงชื่อแท็บใน popup
- `storage` — เก็บค่าตั้งด้านบนในเครื่อง

Run BPM ไม่ขอสิทธิ์เข้าถึงเว็บไซต์ (host permission) และอ่านเนื้อหาหน้าเว็บไม่ได้

### การเปิดเผยข้อมูล
เราไม่เก็บ ไม่ขาย และไม่ส่งต่อข้อมูลของคุณให้ใคร เพราะไม่มีข้อมูลใดออกจากเครื่องของคุณตั้งแต่แรก

### ติดต่อ
แจ้งปัญหาหรือสอบถามได้ที่ GitHub Issues: https://github.com/BlankChakkrapong/run-bpm-site/issues

---

## English

Run BPM is a Chrome extension that listens to the tab you choose and tells you whether the song's tempo (BPM) matches your running cadence.

### In short
- **Everything is processed on your device**, inside your browser.
- **No audio is recorded**, and no data leaves your device.
- **No analytics**, no accounts, no servers, no ads.
- The extension makes no network requests (fonts and all files ship inside the extension).

### Tab audio
- Run BPM only starts listening when you press "Listen to this tab" in that tab. It never listens automatically.
- Audio is fed to a tempo analyzer in memory. The output is a BPM number and a confidence value. The audio itself is never written to disk or sent anywhere.
- Listening stops when you press "Stop", close that tab, or start listening to another tab.

### Data stored on your device

| Data | Where | How long |
|---|---|---|
| Target cadence, tolerance, chosen language | `chrome.storage.local` | Until you uninstall the extension |
| Temporary listening state: the tab being analyzed (tab id and title), the latest BPM, a tempo you tapped yourself | `chrome.storage.session` | Cleared when you close the browser |

All of this stays on your device. Run BPM does not sync across devices (it does not use `chrome.storage.sync`).

### Permissions
- `tabCapture` — capture the audio of the tab you start, to analyze its tempo.
- `offscreen` — open a hidden page to process audio (a service worker cannot process audio itself).
- `activeTab` — access the tab you are using when you click the icon, to identify the tab to listen to and show its title in the popup.
- `storage` — keep the settings above on your device.

Run BPM requests no host permissions and cannot read the content of web pages.

### Sharing
We do not collect, sell, or share your data, because none of it ever leaves your device.

### Contact
Questions or problems: GitHub Issues — https://github.com/BlankChakkrapong/run-bpm-site/issues
