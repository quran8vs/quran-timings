# توقيتات القرآن - مزامنة الصوت مع الآيات 📖

بيانات توقيت شاملة للآيات القرآنية لـ 20 قارئاً مختلفاً، مما يمكّن مزامنة سلسة بين الملفات الصوتية والنصوص القرآنية في التطبيقات والمواقع الإلكترونية.

[![الترخيص](https://img.shields.io/badge/License-MIT-green)](LICENSE)
![الإصدار](https://img.shields.io/badge/Version-1.0.0-blue)
![القراء](https://img.shields.io/badge/Reciters-20%2B-success)
![التغطية](https://img.shields.io/badge/Coverage-114%20Surahs-blue)

---


## القراء | Reciters

| ID | اسم القارئ (العربية) | Reciter Name (English) |
|:---|:---|:---|
| 7 | مشاري راشد العفاسي | Mishari Rashid al Afasy |
| 159 | ماهر المعيقلى | Maher al Muaiqly |
| 19 | أحمد بن علي العجمي | Ahmed ibn Ali al Ajmy |
| 5 | هاني الرفاعي | Hani ar Rifai |
| 9 | محمد صديق المنشاوي | Mohamed Siddiq al Minshawi |
| 3 | عبدالرحمن السديس | Abdur Rahman as Sudais |
| 1 | عبد الباسط عبد الصمد | AbdulBaset AbdulSamad - Mujawwad |
| 2 | عبد الباسط عبد الصمد | AbdulBaset AbdulSamad - Murattal |
| 10 | سعود الشريم | Saud ash Shuraim |
| 158 | عبدالله علي جابر | Abdullah Ali Jabir |
| 161 | خليفة الطنيجي | Khalifah Al Tunaiji |
| 6 | محمود خليل الحصري | Mahmoud Khalil Al Husary |
| 13 | سعد الغامدي | Saad al Ghamdi |
| 160 | بندر بليلة | Bandar Baleela |
| 4 | أبو بكر الشاطرى | Abu Bakr al Shatri |
| 175 | عبدالله حمد أبو شريدة | Abdullah Hamad Abu Sharida |
| 12 | محمود خليل الحصري | Mahmoud Khalil Al Husary |
| 173 | مشاري راشد العفاسي | Mishari Rashid al Afasy |
| 168 | محمد صديق المنشاوي | Mohamed Siddiq al Minshawi - Kids |
| 174 | ياسر الدوسري | Yasser Ad Dussary |

---

## هيكل البيانات | Data Structure

### مثال: سورة الكوثر (108)، الآية 1 | Example: Surah Al-Kawthar (108), Verse 1

```json
{
  "verse_key": "108:1",
  "timestamp_from": 0,
  "timestamp_to": 11110,
  "duration": 11,
  "segments": [
    [1, 1500.0, 4770.0],
    [2, 4780.0, 7810.0],
    [3, 7820.0, 9990.0]
  ]
}
```

**شرح | Explanation:**
- `verse_key`: السورة:الآية | Surah:Verse
- `timestamp_from`: البداية (ميلي ثانية) | Start (milliseconds)
- `timestamp_to`: النهاية (ميلي ثانية) | End (milliseconds)
- `segments`: توقيتات الكلمات | Word timings `[word_number, start, end]`

---

## الاستخدام | Usage

```javascript
fetch('https://raw.githubusercontent.com/quran8vs/quran-timings/main/7/108.json')
  .then(r => r.json())
  .then(data => {
    const verse = data.audio_files[0].verse_timings[0];
    console.log(verse);
  });

```

---

**License**: MIT | **Source**: Quran.com
