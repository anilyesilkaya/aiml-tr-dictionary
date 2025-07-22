---
layout: term
turkish: Pekiştirmeli Öğrenme (PÖ)
english: Reinforcement Learning (RL)
categories:
    - Derin Öğrenme
    - Büyük Dil Modelleri (LLM)
    - Bilgisayar Bilimleri
similar: [chatgpt, gpt, llm]
---

_İsim_ — Pekiştirmeli öğrenme (PÖ), insanın öğrenme biçimini temel alan bir yapay zeka (YZ) eğitim yöntemidir. Pekiştirmeli öğrenme sürecinde, İngilizcede "agent" olarak adlandırılan _etmen_ (veya _eylemen_), insan benzeri deneme-yanılma yoluyla bir görevi öğrenebilmektedir. Bu öğrenme biçimi aynı zamanda çocuk veya hayvan eğitiminde de kullanılmaktadır. Pekiştirmeli öğrenme süreci şu adımlarla gerçekleşir:

1. Etmen, çevresini gözlemler ve mevcut durumu algılar.
2. Gözlemine dayanarak etmen bir _eylem_ (_action_) gerçekleştirir. Bu eylem, etmenin _ilkesine_ (_policy_) bağlı olarak, önceden tanımlanmış bir eylem kümesinden seçilir (örneğin, bir oyun kolunu yukarı, aşağı, sağa veya sola hareket ettirmek).
3. Etmen, gerçekleştirdiği eylemin sonucuna göre bir _ödül_ veya _ceza_ alır.
4. Aldığı ödül veya cezaya göre etmen, gelecekteki eylemlerini ayarlar. Etmenin amacı, zaman içinde aldığı toplam ödül miktarını en üst düzeye çıkarmak veya cezaları en aza indirmektir.

Bu döngüsel süreç, etmenin zamanla _eniyi_ (_optimal_) imal davranışı öğrenmesini sağlar.