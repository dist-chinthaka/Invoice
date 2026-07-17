# Sinha Distributor — Invoice App

[Live Demo](https://theekshanamadumal.github.io/invoice-generator-html/)


### Setup & User Guide / ස්ථාපනය සහ භාවිත මාර්ගෝපදේශය

**Printer:** Woosim PORTI-SW40 (Bluetooth thermal printer, 80mm paper)

---

# 🇬🇧 ENGLISH

## 1. What this app does

Open `sinha-invoice.html` in a web browser. No installation, no internet needed after the first load. You can:

- Create bills by picking items from your product catalogue
- Edit product names, units, and rates (saved automatically in the browser)
- Preview the receipt exactly as it will print
- **Print** directly to the Woosim PORTI-SW40 over Bluetooth
- **Download or Share** the bill as a PDF

> ⚠️ Your saved products live in the browser's storage. If you clear browser data, they reset to the defaults. Always use the same browser on the same device.

## 2. Know your printer

| Setting | Value |
|---|---|
| Bluetooth type | Classic (v2.1 + EDR) — *not* BLE on most units |
| Pairing PIN |'1234' Usually `0000` |
| Baud rate | 57600 (fixed — do not change) |
| Paper | 80mm thermal roll |
| Line width | 48 characters (matches the app exactly) |

**Self-test:** hold the **FEED** button while switching the printer ON. It prints its Bluetooth name and settings — useful if pairing gives trouble.

## 3. Setup — Android phone (recommended)

The easiest and most reliable way to print.

**One-time setup:**
1. Install the free **RawBT** app from the Google Play Store.
2. Turn the printer ON. In your phone's **Settings → Bluetooth**, pair with **PORTI-SW40** (PIN `1234`).
3. Open **RawBT → Settings → Connection method → Bluetooth**, and select the PORTI-SW40.
4. In RawBT, run its test print once to confirm.

**Daily use:**
1. Open `sinha-invoice.html` in Chrome.
2. Make the bill, then tap **🖨 Print Receipt**.
3. The first time, Android asks to open RawBT — allow it and tick "always".
4. The bill prints. Done.

**Alternative (no RawBT):** tap **🔗 Connect (Bluetooth)**. This uses BLE and works *only if your printer unit supports BLE* — most SW40s don't. If the printer never appears in the scan list, use RawBT.

## 4. Setup — iPhone / iPad

Apple does not allow web pages (or ordinary apps) to talk to Bluetooth *Classic* printers, so there are two options:

**Option A — Bluetooth (only if your unit supports BLE):**
1. Install the free **Bluefy** browser from the App Store.
2. Open `sinha-invoice.html` inside Bluefy (send the file to yourself and open it, or host it on any website).
3. Tap **🔗 Connect (Bluetooth)** and pick the printer from the scan list.
4. Tap **Test Print**. If it prints — you're set.
5. If the printer **never appears** in the scan list, your unit is Classic-only, and an iPhone cannot connect to it directly. Use Option B.

**Option B — Share the bill (always works):**
1. Make the bill and tap **📤 Share Bill (PDF)**.
2. The iOS share sheet opens — send to WhatsApp, save to Files, AirPrint, or any printing app.

💡 **Practical tip for shops:** keep one Android phone (even a cheap one) or a laptop as the "printing device", and use the iPhone for making/sharing bills.

## 5. Setup — Windows / Mac laptop

Works in **Chrome** or **Edge** (not Firefox/Safari).

**One-time setup:**
1. Turn the printer ON. Pair it in **Windows Settings → Bluetooth** (PIN `1234`).
2. Windows creates a COM port for it. If you want to check: *Control Panel → Bluetooth settings → COM Ports* — note the **Outgoing** port (e.g. COM5).

**Daily use:**
1. Open `sinha-invoice.html` in Chrome/Edge.
2. Click **🔗 Connect (Laptop / PC)** and choose the printer's **Outgoing** COM port.
3. The status dot turns green. Click **Test Print** to confirm.
4. Make bills and click **🖨 Print Receipt**. The connection stays open until you close the tab or switch the printer off.

## 6. Making a bill (all devices)

1. **Products tab** — add your items once: name, unit (PKT/TIN/BTL...), rate. Edit any field by tapping it; changes save automatically.
2. **Invoice tab** — check business details, customer name, and date. Tap **+ Add Item**, search, and pick products. Adjust Qty/Rate per line.
3. **Preview tab** — see the receipt exactly as it prints.
4. Print, download PDF, or share.

## 7. Troubleshooting

| Problem | Fix |
|---|---|
| Nothing prints, no error | Printer off / out of range (10m) / paper out. Check the printer's LEDs. |
| Android: "Print" does nothing | RawBT not installed, or printer not selected inside RawBT settings. |
| Laptop: two COM ports listed | Choose the **Outgoing** one. |
| Laptop: port opens but garbage prints | Wrong port selected — try the other one. |
| BLE scan never finds the printer | The unit is Bluetooth-Classic-only. Use RawBT (Android) or a laptop. |
| Prints stop mid-receipt | Battery low — charge the printer. |
| Columns misaligned | Run **Test Print** — the ruler line `1234...48` must exactly fill the paper width. |
| Products disappeared | Browser data was cleared. Re-add them (keep a backup list). |

---

# 🇱🇰 සිංහල

## 1. මෙම යෙදුම කරන දේ

`sinha-invoice.html` ගොනුව බ්‍රවුසරයකින් (Chrome) විවෘත කරන්න. ස්ථාපනයක් අවශ්‍ය නැත. පළමු වර load වූ පසු අන්තර්ජාලයද අවශ්‍ය නැත. ඔබට කළ හැකි දේ:

- භාණ්ඩ ලැයිස්තුවෙන් අයිතම තෝරා බිල්පත් සෑදීම
- භාණ්ඩ නම්, ඒකක සහ මිල සංස්කරණය (ස්වයංක්‍රීයව සුරැකේ)
- මුද්‍රණය වන ආකාරයටම බිල්පත පෙරදසුන (Preview) බැලීම
- Woosim PORTI-SW40 වෙත Bluetooth හරහා **කෙලින්ම මුද්‍රණය**
- බිල්පත **PDF ලෙස බාගත කිරීම හෝ Share කිරීම**

> ⚠️ ඔබ එකතු කරන භාණ්ඩ බ්‍රවුසරයේ මතකයේ සුරැකේ. බ්‍රවුසර දත්ත (browser data) මකා දැමුවහොත් ඒවා නැති වේ. සැමවිටම එකම උපකරණයේ එකම බ්‍රවුසරය භාවිත කරන්න.

## 2. ප්‍රින්ටරය ගැන දැනගත යුතු දේ

| සැකසුම | අගය |
|---|---|
| Bluetooth වර්ගය | Classic (v2.1 + EDR) — බොහෝ ඒකකවල BLE නැත |
| Pair කිරීමේ PIN | '1234' සාමාන්‍යයෙන් `0000` |
| Baud rate | 57600 (ස්ථිරයි — වෙනස් නොකරන්න) |
| කඩදාසිය | 80mm thermal roll |
| පේළියක අකුරු | 48 (යෙදුමට හරියටම ගැළපේ) |

**Self-test:** ප්‍රින්ටරය ON කරන අතරතුර **FEED** බොත්තම ඔබාගෙන සිටින්න. එවිට ප්‍රින්ටරයේ Bluetooth නම සහ සැකසුම් මුද්‍රණය වේ — pair කිරීමේ ගැටලුවකදී ප්‍රයෝජනවත් වේ.

## 3. ස්ථාපනය — Android දුරකථනය (නිර්දේශිතයි)

මුද්‍රණයට පහසුම හා විශ්වාසවන්තම ක්‍රමය මෙයයි.

**එක් වරක් පමණක් කළ යුතු දේ:**
1. Google Play Store එකෙන් නොමිලේ ලැබෙන **RawBT** යෙදුම install කරන්න.
2. ප්‍රින්ටරය ON කරන්න. දුරකථනයේ **Settings → Bluetooth** වෙත ගොස් **PORTI-SW40** සමඟ pair කරන්න (PIN `1234`).
3. **RawBT → Settings → Connection method → Bluetooth** තෝරා, PORTI-SW40 select කරන්න.
4. RawBT තුළින් test print එකක් කර තහවුරු කරගන්න.

**දිනපතා භාවිතය:**
1. Chrome එකෙන් `sinha-invoice.html` විවෘත කරන්න.
2. බිල්පත සාදා **🖨 Print Receipt** ඔබන්න.
3. පළමු වතාවේ RawBT විවෘත කිරීමට Android අවසර ඉල්ලයි — "always" තෝරා allow කරන්න.
4. බිල්පත මුද්‍රණය වේ.

**විකල්පය (RawBT නැතිව):** **🔗 Connect (Bluetooth)** ඔබන්න. මෙය BLE භාවිත කරන අතර *ඔබේ ප්‍රින්ටර් ඒකකය BLE සපෝට් කරන්නේ නම් පමණක්* වැඩ කරයි — බොහෝ SW40 වල BLE නැත. Scan ලැයිස්තුවේ ප්‍රින්ටරය කිසිසේත් නොපෙනේ නම් RawBT ක්‍රමය භාවිත කරන්න.

## 4. ස්ථාපනය — iPhone / iPad

Apple සමාගම web පිටුවලට (සහ සාමාන්‍ය app වලට) Bluetooth *Classic* ප්‍රින්ටර් සමඟ සම්බන්ධ වීමට ඉඩ නොදේ. එබැවින් ක්‍රම දෙකක් ඇත:

**ක්‍රමය A — Bluetooth (ඔබේ ඒකකයේ BLE ඇත්නම් පමණයි):**
1. App Store එකෙන් නොමිලේ ලැබෙන **Bluefy** බ්‍රවුසරය install කරන්න.
2. `sinha-invoice.html` ගොනුව Bluefy තුළින් විවෘත කරන්න.
3. **🔗 Connect (Bluetooth)** ඔබා, scan ලැයිස්තුවෙන් ප්‍රින්ටරය තෝරන්න.
4. **Test Print** ඔබන්න. මුද්‍රණය වුවහොත් — සූදානම්.
5. Scan ලැයිස්තුවේ ප්‍රින්ටරය **කිසිසේත් නොපෙනේ නම්**, ඔබේ ඒකකය Classic-only බැවින් iPhone එකකට කෙලින්ම සම්බන්ධ විය නොහැක. ක්‍රමය B භාවිත කරන්න.

**ක්‍රමය B — බිල්පත Share කිරීම (සැමවිටම වැඩ කරයි):**
1. බිල්පත සාදා **📤 Share Bill (PDF)** ඔබන්න.
2. iOS share sheet එක විවෘත වේ — WhatsApp, Files, AirPrint, හෝ ඕනෑම printing app එකකට යවන්න.

💡 **වෙළඳසැල් සඳහා ප්‍රායෝගික උපදෙසක්:** මුද්‍රණයට Android දුරකථනයක් (ලාභ එකක් වුවද) හෝ laptop එකක් තබාගෙන, iPhone එක බිල්පත් සෑදීමට/share කිරීමට භාවිත කරන්න.

## 5. ස්ථාපනය — Windows / Mac ලැප්ටොප්

**Chrome** හෝ **Edge** තුළ වැඩ කරයි (Firefox/Safari නොවේ).

**එක් වරක් පමණක්:**
1. ප්‍රින්ටරය ON කර **Windows Settings → Bluetooth** තුළින් pair කරන්න (PIN `1234`).
2. Windows විසින් COM port එකක් සාදයි. පරීක්ෂා කිරීමට: *Control Panel → Bluetooth settings → COM Ports* — **Outgoing** port එක (උදා: COM5) සටහන් කරගන්න.

**දිනපතා භාවිතය:**
1. Chrome/Edge එකෙන් `sinha-invoice.html` විවෘත කරන්න.
2. **🔗 Connect (Laptop / PC)** click කර ප්‍රින්ටරයේ **Outgoing** COM port එක තෝරන්න.
3. තත්ත්ව තිත (dot) කොළ පැහැ වේ. **Test Print** කර තහවුරු කරන්න.
4. බිල්පත් සාදා **🖨 Print Receipt** click කරන්න. Tab එක වසන තුරු හෝ ප්‍රින්ටරය off කරන තුරු සම්බන්ධතාවය පවතී.

## 6. බිල්පතක් සෑදීම (සියලු උපකරණවල)

1. **Products tab** — භාණ්ඩ එක් වරක් එකතු කරන්න: නම, ඒකකය (PKT/TIN/BTL...), මිල. ඕනෑම කොටුවක් ඔබා සංස්කරණය කළ හැක; වෙනස්කම් ස්වයංක්‍රීයව සුරැකේ.
2. **Invoice tab** — ව්‍යාපාර විස්තර, ගැනුම්කරුගේ නම සහ දිනය පරීක්ෂා කරන්න. **+ Add Item** ඔබා, search කර, භාණ්ඩ තෝරන්න. එක් එක් පේළියේ Qty/Rate වෙනස් කළ හැක.
3. **Preview tab** — මුද්‍රණය වන ආකාරයටම බිල්පත බලන්න.
4. මුද්‍රණය කරන්න, PDF බාගන්න, හෝ share කරන්න.

## 7. ගැටලු නිරාකරණය

| ගැටලුව | විසඳුම |
|---|---|
| කිසිවක් මුද්‍රණය නොවේ, error නැත | ප්‍රින්ටරය off / දුර වැඩියි (10m සීමාව) / කඩදාසි ඉවරයි. ප්‍රින්ටරයේ LED බලන්න. |
| Android: "Print" ඔබද්දී කිසිවක් නොවේ | RawBT install කර නැත, නැතහොත් RawBT settings තුළ ප්‍රින්ටරය තෝරා නැත. |
| ලැප්ටොප්: COM port දෙකක් පෙනේ | **Outgoing** එක තෝරන්න. |
| ලැප්ටොප්: port විවෘත වේ, නමුත් අකුරු විකෘතියි | වැරදි port එක — අනෙක උත්සාහ කරන්න. |
| BLE scan එකේ ප්‍රින්ටරය නොපෙනේ | ඒකකය Bluetooth-Classic-only. RawBT (Android) හෝ ලැප්ටොප් භාවිත කරන්න. |
| බිල්පත මැදදී මුද්‍රණය නවතී | බැටරිය අඩුයි — ප්‍රින්ටරය charge කරන්න. |
| තීරු (columns) නොගැළපේ | **Test Print** කරන්න — `1234...48` රූලර් පේළිය කඩදාසියේ පළල හරියටම පිරවිය යුතුය. |
| එකතු කළ භාණ්ඩ නැති වී ඇත | බ්‍රවුසර දත්ත මකා ඇත. නැවත එකතු කරන්න (backup ලැයිස්තුවක් තබාගන්න). |

---

*Fixed printer settings (do not change / වෙනස් නොකරන්න): 57600 baud · 8 data bits · no parity · 1 stop bit.*
