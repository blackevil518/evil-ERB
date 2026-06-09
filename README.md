<!--
  This is a metadata comment block for contributors.
  Last Updated: 2026-06-09
  Project Status: Active / Educational
-->
<!-- PROJECT SHIELDS -->
<div align="center">

[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
[![Python 3.x][python-shield]][python-url]

</div>

<!-- PROJECT LOGO & HEADER -->
<br />
<div align="center">
  <!-- يمكنك إضافة شعار مشروعك هنا -->
  <!-- <img src="images/logo.png" alt="Logo" width="80" height="80"> -->

  <h1 align="center">evil-ERB</h1>

  <p align="center">
    <strong>منصة تعليمية تفاعلية لفهم البرمجيات الخبيثة وطرق الحماية منها</strong><br />
    <strong>An Interactive Educational Platform to Understand Malware and Defense Mechanisms</strong>
    <br />
    <br />
    <a href="#-المقدمة"><strong>استكشف الوثائق »</strong></a>
    <br />
    <br />
    <a href="https://github.com/blackevil518/evil-ERB/issues/new?labels=bug&template=bug-report---.md">الإبلاغ عن خطأ</a>
    ·
    <a href="https://github.com/blackevil518/evil-ERB/issues/new?labels=enhancement&template=feature-request---.md">طلب ميزة</a>
    ·
    <a href="#-المساهمة">كيف تساهم؟</a>
  </p>
</div>

<!-- TABLE OF CONTENTS -->
<details>
  <summary>📑 <strong>جدول المحتويات | Table of Contents</strong></summary>
  <ol>
    <li><a href="#-المقدمة">المقدمة</a></li>
    <li><a href="#-المشروع">المشروع</a></li>
    <li><a href="#-الميزات-الرئيسية">الميزات الرئيسية</a></li>
    <li><a href="#-المتطلبات-النظام">متطلبات النظام</a></li>
    <li><a href="#-التثبيت-والتشغيل">التثبيت والتشغيل</a></li>
    <li><a href="#-الاستخدام">الاستخدام</a></li>
    <li><a href="#-الهيكلة-المقترحة-للمشروع">الهيكلة المقترحة للمشروع</a></li>
    <li><a href="#-المساهمة">المساهمة</a></li>
    <li><a href="#-الترخيص">الترخيص</a></li>
    <li><a href="#-جهات-الاتصال">جهات الاتصال</a></li>
    <li><a href="#-شكر-وتقدير">شكر وتقدير</a></li>
  </ol>
</details>

## 🚀 المقدمة

**evil-ERB** هو مشروع تعليمي هادف، صُمم ليكون بيئة آمنة وتفاعلية لاستكشاف وفهم آليات عمل البرمجيات الخبيثة، مثل برامج الفدية (Ransomware)، وطرق الحماية والدفاع السيبراني. المشروع موجه للمطورين، طلاب الأمن السيبراني، وكل مهتم بفهم الجانب العملي للهجمات الإلكترونية بهدف التعلم والوقاية.

> **تنبيه أخلاقي:** هذا المشروع للأغراض التعليمية والبحثية فقط. استخدام هذه المعرفة في أي نشاط غير قانوني هو مسؤولية المستخدم وحده، ويتعارض مع روح المشروع وأهدافه.

***

## 📖 المشروع

يهدف هذا المشروع إلى توفير مختبر تعليمي عملي، يمكن من خلاله دراسة كيفية بناء وتفكيك الأدوات المستخدمة في الهجمات السيبرانية، مما يمكن المستخدمين من فهم نقاط الضعف وتطوير آليات حماية أكثر فعالية. يتكون المشروع من عدة وحدات (Modules) موزعة على عدة ملفات تفاعلية.

***

## ✨ الميزات الرئيسية

*   **وحدة برامج الفدية التعليمية:** ملف `ransomware.py` يحتوي على نموذج تعليمي مبسط لفهم آلية عمل برامج الفدية وكيفية انتشارها.
*   **بيئة آمنة ومعزولة:** تم تصميم الكود ليعمل في بيئة اختبارية، مع التأكيد على ضرورة استخدامه في بيئة معزولة لأغراض التعلم فقط.
*   **سهولة التوسع:** هيكل المشروع يسمح بإضافة وحدات تعليمية أخرى بسهولة، مثل وحدات تحليل الشبكات أو أدوات الاختراق الأخلاقي.
*   **تعليمي وتفاعلي:** الشيفرة مصحوبة بتعليقات وشرح يوضح كل خطوة، مما يجعله مناسبًا كمنهاج تعليمي.

***

## 🖥️ المتطلبات (النظام)

*   **لغة البرمجة:** Python 3.10 أو أحدث [python-shield]
*   **المكتبات الأساسية:** (سيتم إدراجها في ملف `requirements.txt`) على سبيل المثال: `os`, `datetime`, `hashlib`
*   **بيئة التشغيل:** يوصى باستخدام بيئة افتراضية (Virtual Environment) معزولة تمامًا عن النظام الأساسي.

***

## ⚙️ التثبيت والتشغيل

1.  **استنساخ المستودع:**
    ```sh
    git clone https://github.com/blackevil518/evil-ERB.git
    cd evil-ERB
