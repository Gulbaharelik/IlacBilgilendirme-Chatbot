# İlaç Bilgilendirme - Chatbot
Bu proje, kullanıcıların ilaçlarla ilgili doğal dilde yönelttiği sorulara yapay zekâ ve doğal dil işleme teknikleri kullanarak yanıt verebilen bir İlaç Bilgilendirme Soru-Cevap Chatbotu geliştirmeyi amaçlamaktadır.

## 📌 Proje Hakkında

Proje kapsamında, ilaç sorularına cevap verme görevini farklı yöntemlerle ele alan iki ayrı yapay zekâ yaklaşımı geliştirilmiş ve karşılaştırılmıştır:

-  DistilBERT Tabanlı Extractive Question Answering
-  Sentence-BERT + T5 Tabanlı Retrieval-Augmented Generation (RAG)

DistilBERT tabanlı model, verilen bağlam içerisinden sorunun cevabını doğrudan bulmaya odaklanırken; RAG tabanlı sistem, kullanıcı sorusuna semantik olarak en yakın bilgileri Sentence-BERT ile getirerek bu bilgileri T5 modeline aktarmakta ve doğal dilde cevap üretmektedir.

Projenin temel amacı, ilaçlarla ilgili soru-cevap görevinde farklı doğal dil işleme yaklaşımlarının performansını incelemek ve bu yaklaşımların güçlü ve zayıf yönlerini karşılaştırmaktır.

## 🎯 Amaç

Bu projenin amacı, ilaçlarla ilgili kullanıcı sorularını doğal dil işleme yöntemleriyle analiz ederek uygun cevaplar üretebilen bir chatbot sistemi geliştirmektir.

Projede, aynı problem için iki farklı yaklaşım uygulanmıştır: **DistilBERT tabanlı Extractive QA** ve **Sentence-BERT + T5 tabanlı RAG**. Bu yapı sayesinde hem doğrudan cevap çıkarma hem de ilgili bilgileri getirerek doğal dilde cevap üretme yaklaşımları incelenmiştir.

## 📂 Proje Dosya Yapısı
- 📄 Rapor: `docs/Proje Raporu.docx`
- 💻 Kaynak Kodlar: `src/DistilBERT.ipynb`-`src/RAG.ipynb`
- 📄 Kütüphaneler: `requirements.docx`

## Kullanılan Teknolojiler

- Transformers
→ DistilBERT ve T5 modelleri

- Datasets
→ MedicationQA veri seti

- PyTorch
→ Model eğitimi ve tensor işlemleri

- Sentence Transformers
→ Semantic retrieval / embedding

- Evaluate
→ Model değerlendirme metrikleri

- Gradio
→ Chatbot arayüzü

- Pandas
→ Veri işleme

## 📄 Rapor

Projenin teorik ve uygulamalı detaylarına aşağıdaki rapordan ulaşılabilir:

**[Proje Raporu](docs/ProjeRaporu.docx)**

## ⚙️ Kurulum

Projeyi çalıştırmak için aşağıdaki adımlar izlenebilir.

### 1. Projeyi Klonlama

Öncelikle proje GitHub üzerinden bilgisayara indirilir:

```bash
git clone https://github.com/Gulbaharelik/REPO-ADI.git
cd REPO-ADI
```

### 2. Gerekli Kütüphanelerin Yüklenmesi

Projede kullanılan Python kütüphaneleri `requirements.txt` dosyasında bulunmaktadır.

Gerekli bağımlılıkları yüklemek için aşağıdaki komut çalıştırılır:

```bash
pip install -r requirements.txt
```

### 3. Notebookların Çalıştırılması

Projede iki farklı model yaklaşımı bulunmaktadır:

* **DistilBERT:** Extractive Question Answering yaklaşımı
* **RAG:** Sentence-BERT + T5 tabanlı Retrieval-Augmented Generation yaklaşımı

Her iki model için ilgili `.ipynb` dosyası **Google Colab** ortamında açılarak hücreler sırasıyla çalıştırılabilir.

### 4. Model Dosyalarının Kullanılması

Model eğitimleri tamamlandıktan sonra oluşturulan model ağırlıkları, ilgili notebook içerisinde yer alan Gradio arayüzlerinde kullanılmaktadır.

DistilBERT ve RAG modelleri birbirinden bağımsız olarak çalıştırılabilir. Her iki model yaklaşımı için ayrı bir chatbot arayüzü bulunmaktadır.

### 5. Chatbot Arayüzünün Çalıştırılması

İlgili notebook içerisindeki Gradio kodu çalıştırıldığında chatbot arayüzü oluşturulur.

Kullanıcı arayüz üzerinden ilaçlarla ilgili **İngilizce bir soru** girerek model tarafından oluşturulan cevabı görüntüleyebilir.

> **Not:** Proje Google Colab ortamında geliştirilmiştir. Özellikle RAG sisteminde kullanılan T5 modelinin eğitimi için GPU kullanılması önerilmektedir.


## ⚠️ Etik Kullanım

Bu proje eğitim ve akademik çalışma amacıyla geliştirilmiştir. Chatbot tarafından verilen bilgiler profesyonel tıbbi tavsiye yerine geçmez.
