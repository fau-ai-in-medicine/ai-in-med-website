---
title: "FDA Guidelines for AI in Medicine"
date: 2021-2-10T13:44:42-05:00
draft: false
author: "Leila Abdelrahman"
---



Artificial Intelligence (AI) now pervades almost every application and website we use. It's also rapidly entering the healthcare space. There's a common understanding that government regulation plays catch-up with innovation. This is especially true when it comes to software. In radiology, there's a plethora of papers on detecting lesions in mammograms [1], brains [2], and chest x-rays [3], yet many advances in AI research are miles away from real-world use in the clinic.

Although advances in software far outpace those in clinical practice, in a report published in January 2021, the FDA  tries to mitigate this disparity by presenting a **five-point** action plan for regulating the booming Medical-AI industry. I read through the [report](https://www.fda.gov/media/145022/download) and found that many of the points the FDA calls for already persist in engineering circles, yet needs to be comprehendible to the broader public.

In this post, I'll go through the **five points** the report discusses and bring in some personal insights and critiques on the FDA's take on AI-based software as a Medical Device. Specifically, I think the best discussions come in the form of **actionable questions**, so that's how I'll frame the remaining post.

## 1. What AI-Specific Regulations do we Need to Create?

For most of Medicine, it was generally a "wet-science" grounded in the classical study of Biology and Chemistry. With the tech-revolution, especially rapid advances in AI and Deep Learning in the past five years, Medicine is adopting AI-based devices for patients and providers.


I worked on an [AI-based iOS app](http://leilaabdel.com/project/p-predict/) for explaining prostate cancer outcomes to patients and know just how impactful these devices can be. The app presents predicted chemotherapy outcomes based on an algorithm founded on nation-wide aggregate data. Doctors are now beta-testing this app with real-patients, and the algorithm helps patients understand how their predicted odds change based on their choice to take Androgen Deprivation Therapy (ADT) [4].

To me, the app's intention is to encourage patients to undergo therapy based on a robust algorithm. The FDA's 2021 report calls for technologists and practitioners alike to highlight **what exactly an AI algorithm intends to change in a patient.**

On many occasions, Deep Learning and AI engineers can have extreme fun creating computer-made abstract art or Deep Fakes. In Medicine, we are dealing with **human life**: software should respect this fact, ensuring their innovations can change patient outcomes for the better.

## 2. How can we Dictate Best Practices in Medical AI?


As an AI researcher, I've noticed a trend in setting community standards and best practices in the last years. For example, it's almost necessary to include the source code in a public repository when submitting computational papers to conferences. This trend is increasing in journals, too. Websites like PapersWithCode feature papers on their websites that simply include links to repositories (even before peer review).

Other examples of best practices in computing include:
- Contextualizing quantitative results with prior authors' outcomes.
- Benchmarking methods on standardized datasets.
- Clearly showing both quantitative and qualitative insights in research.

In their report, the FDA accepts this existing self-regulatory infrastructure and hopes to dovetail into existing frameworks to "harmonize good machine learning" [5].

## 3. What does Patient-Centered Transparency Look Like?
Transparency and interpretability are buzz-words in Medical AI. As humans, we're wired to look for correlations and causations, often understanding linear outcomes. Yet, Deep Learning and most AI are based on **non-linear** decisions, which are challenging to retrace and logically understand.

Imagine I am a patient (let's call me 40-year-old Maryam), and I go to my radiologists for my scheduled mammogram follow-up. The doctor has me sit down and then says the words I fear the most: "We found something strange in your images and need to take a biopsy". Immediately, my heart starts thumping faster, I feel my cheeks go red, and I muster up all my strength to temper my panic.



"Well, Doctor, what do you mean? Is there anything you can show me? I don't really understand where this is coming from." As a patient, I'd need transparency and confidence to undercut my fear of impending doom. I'd want to look at the images and ask the doctor what she sees. Radiologists of the future will increasingly rely on decision-support tools to make their diagnoses and prognoses. But for them to confidently present me with the facts, how these decision-support tools work should be completely transparent.

For example, doctors should know fine-grained details about a device's confidence level in a decision. They should understand familiar sources of error, what factors an algorithm chooses in making a decision, and how it weighs them to provide an answer. For example, if I'm working with a genetics-based algorithm, what genes does the algorithm look for, or what expression patterns does it identify to prompt it to decide?

Through clear communication, I believe doctors, and by extension, patients will wipe away opacity from AI, empowering themselves to understand the choices software makes.

## 4. How do we Account for Inherent Bias?
Most of the literature I read in AI focuses more on numbers and performance over the patient backgrounds, ethnicity, gender, and family history. Most papers on genetics overwhelmingly focus on White patients of European origin [6], leaving the vast majority of the world with data that misses the mark on representing their own backgrounds.


One classic example is how much diagnostic imaging AI tools like skin cancer lesion detectors, mammography classifiers, and risk stratifiers fail to contextualize patients in their background and environment. For example, interpreting a patient's mammogram with no family history of cancer *should* be different from that of a patient with three-generations of family cancer death.

The FDA commits to creating a committee to identify and mitigate existing biases that pervade AI Medical research in its report.

## 5. Does it work in the Real-World (and how do we measure that)?

This is the most obvious question. Scientists can publish hundreds of theoretical papers on efficient diagnostics or select data to favor stellar published results. Yet, the only way these theories and software have value is if they are robust in the real-world.

In 2020, the MIT Technology Review [7] discussed Google's flopped Diabetic Retinopathy Detector. Although it achieved accurate and reliable results in the lab, when the researchers introduced it into clinics in Thailand and India, the results were subpar. When developing their algorithms, the researchers failed to consider real-world scenarios like poor lighting, cases with minute decision margins, and other "anomalies" inherent to bustling clinics and hospitals. These problems grew in under-resourced clinics.

Moving forward, I think it's critical for technologists to account for these challenges both in the lab and beta testing in clinics. In the lab, researchers can compose adversarial approaches to test their methods' robustness. Researchers should conduct more thorough **needs assessments** before and after releasing beta versions of their technologies in clinics. The best way to ensure a device works is to get feedback from users. Considering patient, nursing staff, and provider roles and perspectives is essential. With these factors in mind, we can work to ensure that solutions are fundamentally practical.

## Resources

1. Abdelhafiz, D., Yang, C., Ammar, R. and Nabavi, S., 2019. Deep convolutional neural networks for mammography: advances, challenges and applications. BMC bioinformatics, 20(11), pp.1-20.
2. Tandel, G.S., Biswas, M., Kakde, O.G., Tiwari, A., Suri, H.S., Turk, M., Laird, J.R., Asare, C.K., Ankrah, A.A., Khanna, N.N. and Madhusudhan, B.K., 2019. A review on a deep learning perspective in brain cancer classification. Cancers, 11(1), p.111.
3. Li, Y., Zhang, Z., Dai, C., Dong, Q. and Badrigilan, S., 2020. Accuracy of deep learning for automated detection of pneumonia using chest X-Ray images: A systematic review and meta-analysis. Computers in Biology and Medicine, p.103898.
4. Sharifi, N., Gulley, J.L. and Dahut, W.L., 2005. Androgen deprivation therapy for prostate cancer. Jama, 294(2), pp.238-244.
5. US Food and Drug Administration, 2019. Artificial intelligence and machine learning in software as a medical device. Silverspring: US Food and Drug Administration.
6. McGauran, N., Wieseler, B., Kreis, J., Schüler, Y.B., Kölsch, H. and Kaiser, T., 2010. Reporting bias in medical research-a narrative review. Trials, 11(1), pp.1-15.
7. Heaven, W.D., 2020. Google's medical AI was super accurate in a lab. Real life was a different story. MIT Technology Review.
