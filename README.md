<p align="center">
  <img src="7c6943b2-10e6-4523-aff1-f3372c69988a.png" alt="Islamic Azad University North Tehran Branch" width="180"/>
</p>

<h1 align="center">COVID-SegNet: Encoder–Decoder-Based Architecture for COVID-19 Lesion Segmentation in Chest X-Ray</h1>

<p align="center">
  پروژهٔ درس <strong>یادگیری ماشین</strong><br>
  دانشگاه آزاد اسلامی، واحد تهران شمال<br>
  استاد: <strong>دکتر ملیحه ثابتی</strong>
</p>

---

## 📄 معرفی پروژه

در این پروژه، پیاده‌سازی مقاله‌ای با عنوان زیر انجام شده است:

> COVID-SegNet: Encoder–Decoder-Based Architecture for COVID-19 Lesion Segmentation in Chest X-Ray

این مقاله یک معماری پیشنهادی برای **تقسیم‌بندی نواحی آلوده به کووید-۱۹ در تصاویر اشعه ایکس قفسه سینه (CXR)** معرفی می‌کند. مدل طراحی‌شده بر پایه UNet بوده و با استفاده از ماژول‌های توجه (Attention) و ASPP تقویت شده است.

---

## 🗂 دیتاست

برای آموزش و ارزیابی مدل از دیتاست **QaTa-COV19** استفاده شده است که شامل ۲۹۵۱ تصویر CXR همراه با ماسک‌های Ground Truth می‌باشد.

📥 آدرس دیتاست:  
[https://www.kaggle.com/datasets/aysendegerli/qatacov19-dataset](https://www.kaggle.com/datasets/aysendegerli/qatacov19-dataset)

---

## 🧠 روش کار

- استفاده از معماری پایه UNet
- افزودن مکانیزم‌های scSE Attention (channel + spatial attention)
- استفاده از Atrous Spatial Pyramid Pooling با نرخ‌های گسترش ۲، ۳، ۴
- آموزش بر روی Google Colab با GPU نوع P100
- استفاده از 5-Fold Cross-Validation برای ارزیابی

---

## 🛠 تنظیمات اجرا

| پارامتر | مقدار |
|---------|--------|
| زبان برنامه‌نویسی | Python |
| فریم‌ورک | TensorFlow / Keras |
| تعداد epoch | 200 |
| Batch size | 4 |
| Optimizer | Adam (lr=0.0005) |
| Loss function | Dice Loss |

---

## 📊 نتایج به‌دست‌آمده

| Fold | Dice Score | Jaccard Index |
|------|------------|----------------|
| 1    | 0.8202     | 0.6952         |
| 3    | **0.8407** | **0.7253**     |
| میانگین | 0.8325     | 0.7132         |

---

## 📌 نکات تکمیلی

- پیاده‌سازی با استفاده از ساختار Encoder-Decoder طراحی شده است.
- مدل دارای حدود ۶.۵ میلیون پارامتر می‌باشد و در مقایسه با مدل‌هایی مانند Inception-v3 بسیار سبک‌تر است.
- تصاویر خروجی به‌صورت کیفی نیز در مقاله اصلی نشان‌دهنده عملکرد مناسب در حالت‌های شدید، متوسط و خفیف هستند.

---

## 📚 منابع

- [مقاله اصلی - Springer](https://doi.org/10.1007/s00530-023-01096-9)
- [دیتاست QaTa-COV19 - Kaggle](https://www.kaggle.com/datasets/aysendegerli/qatacov19-dataset)

---

<p align="center"><i>این پروژه صرفاً جهت آموزش و ارائه در درس یادگیری ماشین تهیه شده است.</i></p>
