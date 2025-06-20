---
layout: "lesson"
lang: "hi"
title: "बेसिक LaTeX डॉक्यूमेंट संरचना"
description: "यह पाठ एक LaTeX डॉक्यूमेंट की मूल संरचना को दिखाता है, और इसे एक PDF फ़ाइल में कैसे बदलना है, साथ ही LaTeX को नियंत्रित करने के लिए उपयोग किए जाने वाले मुख्य विशेष करैक्टर्स को भी समझाता है।"
toc-anchor-text: "डॉक्यूमेंट संरचना"
toc-description: "किसी डॉक्यूमेंट की मूल संरचना"
---

# बेसिक LaTeX डॉक्यूमेंट संरचना

<span
  class="summary">यह पाठ एक LaTeX डॉक्यूमेंट की मूल संरचना को दिखाता है, और इसे एक PDF फ़ाइल में कैसे बदलना है, साथ ही LaTeX को नियंत्रित करने के लिए उपयोग किए जाने वाले मुख्य विशेष करैक्टर्स को भी समझाता है।</span>

आपका पहला LaTeX डॉक्यूमेंट बहुत ही सरल होगा: इसका उद्देश्य आपको यह दिखाना है कि एक LaTeX डॉक्यूमेंट कैसा दिखता है और इसे सफलतापूर्वक टाइपसेट कैसे किया जाता है। अब आपको [कोड-उदाहरणों का उपयोग कैसे करना है?](help) को देखने का पहला अवसर भी मिलेगा, जो `learnlatex.org` पर उपलब्ध हैं।  

यदि आप लोकल इन्सटाल्ड LaTeX का उपयोग कर रहे हैं, तो अपने संपादक में `first.tex` नामक एक नई फ़ाइल बनाएं और नीचे दिए गए पाठ को कॉपी-पेस्ट करें या टाइप करें।  

यदि आप ऑनलाइन प्रणाली का उपयोग कर रहे हैं, तो आप उदाहरण में दिए गए ‘Run at TeXLive.net’ या ‘Open in Overleaf’ बटनों पर क्लिक करके इसे आज़मा सकते हैं!

<p class="hint">हम सुझाव देते हैं कि आप ऑनलाइन विकल्पों को आज़माएँ, भले ही आपने अपने सिस्टम पर लोकली LaTeX इनस्टॉल कर लिया हो; यह विभिन्न विकल्पों के काम करने के तरीके को समझने का एक अच्छा अवसर है।</p>

```latex
\documentclass{article}
\usepackage[T1]{fontenc}

\begin{document}
Hey world!

This is a first document.
\end{document}
```

फ़ाइल को सेव करें और इसे एक PDF डॉक्यूमेंट में टाइपसेट करें। यदि आप स्थानीय LaTeX स्थापना का उपयोग कर रहे हैं, तो आपको कौन सा बटन दबाना है, यह आपके द्वारा चुने गए संपादक पर निर्भर करेगा। आपको एक PDF फ़ाइल प्राप्त होनी चाहिए जिसमें ऊपर दिया गया पाठ _साथ ही_ एक पृष्ठ संख्या होगी; LaTeX इसे स्वचालित रूप से जोड़ता है।  

`first.pdf` आउटपुट को अपने पसंदीदा PDF व्यूअर प्रोग्राम में खोलें। शानदार दिख रहा है न?—बधाई हो आपको!  

यदि आप PDF के बजाय HTML आउटपुट प्राप्त करना चाहते हैं, तो [सहायता](./help) देखें कि इसे कैसे किया जा सकता है।


## त्रुटियों (Errors) को संभालना  

त्रुटियाँ होना सामान्य है। सुनिश्चित करें कि आपने टेक्स्ट फ़ाइल में प्रत्येक पंक्ति को ठीक वैसे ही लिखा है जैसा ऊपर दिया गया है। कभी-कभी छोटे से बदलाव भी परिणाम में बड़े अंतर ला सकते हैं, यहाँ तक कि डॉक्यूमेंट को काम न करने योग्य भी बना सकते हैं। यदि आप अटक जाते हैं, तो डॉक्यूमेंट को मिटाकर इसे ऊपर दी गई पंक्तियों से दोबारा कॉपी करें।  

यदि आपका LaTeX टाइपसेटिंग रन एक प्रश्नचिह्न (`?`) पर समाप्त होता है, तो आप `x` टाइप करके और `<Enter>` दबाकर इससे बाहर निकल सकते हैं।  

LaTeX की त्रुटि संदेश प्रणाली उपयोगी होने की कोशिश करती है, लेकिन यह वर्ड प्रोसेसर के संदेशों की तरह नहीं होती। कुछ संपादक त्रुटि संदेशों को पूरा-पूरा नहीं दिखाते हैं, जिससे महत्वपूर्ण जानकारी छिप सकती है। LaTeX हमेशा एक लॉग फ़ाइल बनाता है, जिसका नाम `.log` से समाप्त होता है। आप वहाँ हमेशा त्रुटि की पूरी जानकारी देख सकते हैं, और यदि कोई समस्या आती है, तो विशेषज्ञ LaTeX उपयोगकर्ता अक्सर आपकी लॉग फ़ाइल की ही एक प्रति माँगते हैं।



<p class="hint">हम त्रुटियों से निपटने के बारे में अधिक जानकारी <a href="./lesson-15">पाठ 15</a>में देते हैं।</p>

## आपने क्या सीखा  

पहला डॉक्यूमेंट बुनियादी चीज़ें दिखाता है।

जैसे कि एक LaTeX डॉक्यूमेंट टेक्स्ट और कमांड्स के मिश्रण होते हैं।कमांड्स एक बैकस्लैश (`\`) से शुरू होते हैं और कभी-कभी इनमें कर्ली ब्रेसेस `{ }` में arguments होते हैं (या कभी-कभी वर्ग कोष्ठक `[ ]` में वैकल्पिक तर्क होते हैं)। इसके बाद, जब आप LaTeX को अपनी फ़ाइल टाइपसेट करने के लिए कहते हैं, तो आपको एक आउटपुट PDF मिलता है।


हर LaTeX डॉक्यूमेंट में `\begin{document}` से शुरू होता है और इससे मिलने वाला टैग `\end{document}` होता है।  
इन दोनों के बीच *डॉक्यूमेंट बॉडी* होती है, जहाँ आपकी सामग्री लिखी जाती है। इस उदाहरण में बॉडी में दो पैराग्राफ़ हैं (LaTeX में पैराग्राफ़ को अलग करने के लिए एक या अधिक खाली पंक्तियाँ दी जाती हैं)।  

`\begin{document}` से पहले का भाग *डॉक्यूमेंट प्रीएम्बल* कहलाता है, जिसमें दस्तावेज़ का लेआउट सेट करने के लिए कोड लिखा जाता है।  
`\usepackage` कमांड को [बाद के पाठ](lesson-06) में समझाया गया है। इस साइट के अधिकतर कोड-उदाहरणों में इसे फ़ॉन्ट एन्कोडिंग सेट करने के लिए उपयोग किया जाता है।  

LaTeX में अन्य `\begin{...}` टैग और `\end{...}` टैग भी जोड़े जाते हैं, जिन्हें *एनवायरनमेंट्स* कहा जाता है।

आपको इन्हें सही तरीके से मिलाना होता है, यानी हर `\begin{x}` के लिए एक `\end{x}` होना चाहिए। यदि आप इन्हें नेस्ट करते हैं, तो आपको `\begin{x} ... \begin{y}` के लिए `\end{y} ... \end{x}` का उपयोग करना होगा, ताकि `\begin` और `\end` क्रम आपस से मेल खाएँ।  

हम LaTeX फ़ाइल में टिप्पणियाँ (comments) `%` के साथ शुरू करते हैं; आइए इसका उपयोग संरचना को दिखाने के लिए एक उदाहरण-कोड लिखें:


```latex
\documentclass[a4paper,12pt]{article} % The document class with options
% Select T1 font encoding: suitable for Western European Latin scripts
\usepackage[T1]{fontenc}
% A comment in the preamble
\begin{document}
% This is a comment
This is   a simple
document\footnote{with a footnote}.

This is a new paragraph.
\end{document}
```
ऊपर आप देख सकते हैं कि हमारे पास दो पैराग्राफ़ हैं: इसे अलग करने के लिए 'खाली पंक्ति' का उपयोग किया गया है। साथ ही, ध्यान दें कि कई 'खाली स्थान (spaces)' एक ही 'खाली स्थान' के रूप में माने जाते हैं।  

कभी-कभी, आपको एक *'हार्ड'* स्पेस की आवश्यकता हो सकती है, जो लाइन ब्रेक पर विभाजित न हो। LaTeX में, हम इसे `~` का उपयोग करके बना सकते हैं, जिससे दो टेक्स्ट टुकड़ों को एक साथ जोड़ा जा सकता है। यह विशेष रूप से तब उपयोगी होता है जब हम पाठ्यक्रम में आगे चलकर क्रॉस-रेफरेंस (cross-references) बनाना शुरू करेंगे।


## विशेष वर्ण (Special Characters)  

आपने शायद देखा होगा कि ``\``, `{` और `}` का LaTeX में विशेष अर्थ होता है। `\` का प्रयोग LaTeX को निर्देश (command) देने के लिए उपयोग किया जाता है। कर्ली ब्रेसेस `{` और `}` का उपयोग *अनिवार्य arguments* (mandatory arguments) को दिखाने के लिए किया जाता है, यानी ऐसी जानकारी जिसे कमांड को समझने के लिए आवश्यक होती है।  


कुछ अन्य चिन्ह भी विशेष अर्थ रखते हैं। उदाहरण के लिए, हमने देखा कि `~` एक *हार्ड स्पेस* बनाता है। इनमें से अधिकांश विशेष चिन्ह आमतौर पर सामान्य पाठ में बहुत कम उपयोग होते हैं, इसलिए इन्हें विशेष अर्थों के लिए चुना गया है।  


यदि आपको इन विशेष चिन्हों को टेक्स्ट में प्रदर्शित करने की आवश्यकता हो, तो हमने इसके बारे में [अधिक जानकारी](more-03) पृष्ठ पर दी है।




## अभ्यास (Exercise)  

आप कुछ 'ऑनलाइन संपादन और टाइपसेटिंग प्रणाली' के साथ दिए गए कोड- उदाहरण के साथ अभ्यास करें; सामग्री को टाइपसेट करने के लिए ऊपर दिए गए बटन पर क्लिक करें, फिर इसी वेबपेज में इसे संपादित भी करें और दोबारा टाइपसेट करें।  

अपने पहले डॉक्यूमेंट में कुछ नया पाठ जोड़ने का प्रयास करें, फिर इसे टाइपसेट करें और अपने PDF में आए बदलाव को देखें। कुछ अलग-अलग पैराग्राफ़ बनाकर देखें और अलग-अलग मात्रा में खाली स्थान (spaces) जोड़ें। अपने संपादक (editor) को एक्सप्लोर करें; अपने स्रोत कोड पर क्लिक करें और देखें कि PDF में उसी पंक्ति पर कैसे जाया जा सकता है। कुछ *हार्ड स्पेसेस* (`~`) जोड़कर देखें और देखें कि वे लाइन ब्रेकिंग को कैसे प्रभावित करते हैं।
