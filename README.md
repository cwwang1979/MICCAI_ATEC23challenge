# MICCAI_ATEC23challenge 
ATEC23 is a MICCAI 2023 online satellite event, which means that participants are not required to physically attend the conference but still able to join the challenge remotely.
https://conferences.miccai.org/2023/en/online.asp

# ATEC23 Challenge Results
| Organizers Baseline Model      | Network Name | Accuracy | Precision | Recall | F1-Score | F1-Score Rank |      |
| :---                           |      :---   | :---:    |  :---:    | :---:  |  :---:    |    :---:      |:---: |
| Wang et al. (2022) [1]         | Wang's M1    | 0.761    |   0.791   | 0.946  |  0.862   |      2        |      |
| Wang et al. (2022) [1]         | Wang's M2    | 0.718    |   0.781   | 0.893  |  0.833   |      3        |      |
| Wang et al. (2022) [1]         | Wang's M3    | 0.775    |   0.794   | 0.964  |  0.871   |      1        |      |
| Coudray et al (2022) [2]       | InceptionV3  | 0.575    |   0.760   | 0.667  |  0.710   |      4        |      |
| Campanella et al. (2022) [3]   | ClassicMIL   | 0.469    |   0.571   | 0.311  |  0.403   |     10        |      |
| __Participant's Team__     | __Network Name__        | __Accuracy__ | __Precision__ | __Recall__ | __F1-Score__ | __F1-Score Rank__ | __Participant's F1-Score Rank__  |
| FaizMedCv                  | WSINeXt                 | 0.600    |   0.618   | 0.786  |  0.692   |      5        |   1   |
| AI FUTURE                  | Swin-Transformer        | 0.572    |   0.616   | 0.670  |  0.642   |      6        |   2   |
| UBC-AIM                    | cTransPath+ VarMIL      | 0.517    |   0.573   | 0.612  |  0.592   |      7        |   3   |
| MMaiLGA                    | ReMix+ABMIL/ReMix+DSMIL | 0.561    |   0.636   | 0.544  |  0.586   |      8        |   4   |
| NPU-SAIIP                  | ResNet+MIL              | 0.528    |   0.725   | 0.282  |  0.406   |      9       |   5   |


# MICCAI onsite workshop- level 1 meeting room 12, 9AM, Oct 12th, Vancouver

## Automated prediction of treatment effectiveness in ovarian cancer using histopathological images

## Introduction
Ovarian cancer is the second most common cause of gynecologic cancer death in women around the world. Epithelial ovarian cancer (EOC) accounts for over 95% of ovarian malignancies. Most women with ovarian cancer are diagnosed in advanced stage, which accounts for the high mortality rate. EOC is classified into at least five distinct histopathological subtypes, including high-grade serous, low-grade serous, clear cell, endometrioid, and mucinous ovarian cancer. High-grade serous ovarian cancer (HGSOC) is the most common histologic subtype, accounting for more than 70% of EOCs. Despite the progress made during the last two decades in the surgery and chemotherapy of ovarian cancer, more than 70 % of advanced patients are with recurrent cancer and decease. Bevacizumab is a humanized monoclonal antibody, which blocks VEGF signaling in cancer, inhibits angiogenesis and causes tumor shrinkage, and has been recently approved by FDA as a monotherapy for advanced ovarian cancer in combination with chemotherapy. Considering the cost, potential toxicity, and finding that only a portion of patients will benefit from these drugs, the identification of new predictive method for the treatment of EOC remains an urgent unmet medical need. Recent studies have shown that the challenge of applying digital whole slide image (WSI) to predict post-treatment response may be solved using deep learning (DL) technologies. Over the past few years, interest in the use of DL based approaches for drug discovery and development has increased. In this challenge, two datasets are constructed, including a whole section slide dataset and an independent TMA slide dataset. To assess the generalizability of the model, the whole section slide dataset will be used for training and the second independent TMA slide dataset will used for testing the DL based approaches. This challenge aims to build an automatic precision oncology system for patient selection and guiding ovarian cancer treatment.

## Date
- Open registration : currently open
- Training data release : available at [TCIA](https://doi.org/10.7937/tcia.985g-ey35) [4]
- Testing data release : available at [TMA Testing Set](https://drive.google.com/drive/folders/1WyHTxMo1qQ5FKF-CJVI_-_8j7StYklpJ). The password for the reference labels are provided on the joint challenge paper currently in submission to MIA.
- Deadline for submission : September 15th, 2023
the files to submit include a treatment outcome prediction file in the csv format (example shown in the table bellow and the file is available in the [link](https://drive.google.com/file/d/1fvyuJbpg6PyWJfGZb3qsZwEN4zIqLkBc/view?usp=share_link)) and a four-page paper about the methods in word or LaTex (template available at the [link](https://drive.google.com/drive/folders/1fiAdITZqX1lpImrINIwDbs0EtzUfV6rN?usp=share_link)).

| CoreID  | prediction (probability) | prediction(Binary [1:effective, 0: invalid] ) |
| :---         |     :---:      |          ---: |
| 0  | 0.75 | 1 |
| 1  | 0.6 | 1 |
| 2  | 0.25 | 0 |



## Datasets and Programs
### Training Cohorts
A large whole section whole slide image (WSI) dataset, contains 288 De-identified hematoxylin and eosin (H&E) stained whole section slides with clinical information of HGSOC patients collected from the tissue bank of the Tri-Service General Hospital and the National Defense Medical Center, Taipei, Taiwan. The large training dataset has been accepted to be stored on The Cancer Imaging Archive (TCIA) platform, and the dataset presented here is available at [the training data link](https://doi.org/10.7937/tcia.985g-ey35) [4].

### Testing Cohorts and Evaluation Software 
180 tissue cores collected of HGSOC patients are collected from the tissue bank of the Tri-Service General Hospital and the National Defense Medical Center, Taipei, Taiwan. In order to test the model generalizability on unseen data, an independent and separate testing data set is provided for evaluation of models on not only sensitivity and specificity, but also on generalizability for practical usages. The data link are available at the [TMA Testing Set](https://drive.google.com/drive/folders/1WyHTxMo1qQ5FKF-CJVI_-_8j7StYklpJ). The password for the reference labels are provided on the joint challenge paper currently in submission to MIA. 

# Participant's Code

| Participant's Team     | Network Name      | Institution  | Repository |
| :---                           |      :---   | :---    |  :---    |
| FaizMedCv                  | WSINeXt                 | Tezpur University, Assam, India   | [Link](https://drive.google.com/file/d/1JbrkBNMGnsxHmyE8PxpP0hBnMz3FsjrO/view?usp=drive_link)  (password: Faiz91MedCv) |
| AI FUTURE                  | Swin-Transformer        | AIFUTURE Lab, Beijing, China  | [Link](https://drive.google.com/file/d/1dRj2VmNIXmbAa6iQxB3paAjGANv22ms1/view?usp=drive_link) |
| UBC-AIM                    | cTransPath+ VarMIL      | University of British Columbia, Canada | [Link](https://drive.google.com/file/d/1wHyh6ywyqLzItqHvuUsDH3ocO7Ozdqi3/view?usp=drive_link) |
| MMaiLGA                    | ReMix+ABMIL/ReMix+DSMIL | Shenzen University, China  | [Link](https://drive.google.com/file/d/1Bu_3Q0mmzefCsPmk1fdwl1XY0oneSQyv/view?usp=drive_link)  |
| NPU-SAIIP                  | ResNet+MIL              | Northwestern Polytechnical University, Shaanxi, China | [Link](https://drive.google.com/file/d/1AssBOJrzLU01MsAfEBDmmSR5IpZn4GmN/view?usp=sharing)  |



## Organizers
- Prof. Ching-Wei Wang
Professor, Graduate Institute of Biomedical Engineering and Graduate Institute of Applied Science and Technology,
National Taiwan University of Science and Technology, Taipei, Taiwan.
Chair of a grand challenge for tissue microarray analysis in thyroid cancer diagnosis, IEEE International Symposium
on Biomedical Imaging (ISBI) 2017, Australia.
Chair of Grand Challenges in Dental X-ray Image Analysis, IEEE International Symposium on Biomedical Imaging
(ISBI) 2015, New York, USA.
Chair of the Grand Challenge - Automatic Cephalometric X-Ray Landmark Detection, IEEE International
Symposium on Biomedical Imaging (ISBI) 2014, Beijing, China.
- Dr. Tai-Kuang Chao
Chief, Department of Pathology, Tri-Service General Hospital, Taipei, Taiwan.
Associate Professor, College of Biochemistry, National Defense Medical Center, Taipei, Taiwan.
Director, Biobank, Tri-Service General Hospital and National Defense Medical Center


## Challenge Publication and Prizes
Top-ranked teams will be invited for SCI journal publications and awarded the prizes below. 

A joint challenge paper will be prepared and submitted to journals such as Medical Image Analysis or IEEE trans on Medical Imaging, and two members from the top 10 participating teams from the leaderboards will be invited to contribute to the joint challenge paper as co-authors. 

In addition, three special Issues of the SCI-indexed journals with associated prizes (22,000 CHF in total) have been arranged for the challenge as follows. Top teams will be invited for paper submission to the arranged special issues.

The participating teams may publish their own results separately after the challenge paper is published, **but they should cite the assigned papers listed bellows**.

### Assigned Papers
- Wang et al. (in submission) ATEC23 Challenge: automated prediction of treatment effectiveness in ovarian cancer using histopathological images
- Wang et al. (2022) Histopathological whole slide image dataset for classification of treatment effectiveness to ovarian cancer, Scientific Data, 9(25), 1-5
https://doi.org/10.1038/s41597-022-01127-6
- Wang et al. (2022) Weakly Supervised Deep Learning for Prediction of Treatment Effectiveness on Ovarian Cancer from Histopathology Images, Computerized Medical Imaging and Graphics, 99.102093,1-26
https://doi.org/10.1016/j.compmedimag.2022.102093
- Wang et al. (2022) A weakly supervised deep learning method for guiding ovarian cancer treatment and identifying an effective biomarker, Cancers 14(7):1651
https://doi.org/10.3390/cancers14071651
- Wang et al. (2023) Ensemble biomarkers for guiding anti‐angiogenesis therapy for ovarian cancer using deep learning, Clinical and Translational Medicine, 13(1), e1162, 1-7
https://doi.org/10.1002/ctm2.1162

### Special Issues and the Prizes
Special Issues for the challenge:
1. Discover Oncology (Springer Nature, IF: 4.667) Artificial Intelligence in Pathology and Cytology for Cancer Research (https://link.springer.com/collections/ddiebdeeci)
2. Cancers (JCR 2021 IF = 6.575) Special Issue "Computational Pathology for Breast Cancer and Gynecologic Cancer"
(https://www.mdpi.com/journal/cancers/special_issues/W4UO7BGI11)
3. Diagnostics (JCR2021 IF= 3.992) "Special Issue "Deep Learning in Oncological Image Analysis"
(https://www.mdpi.com/journal/diagnostics/special_issues/deep_learning_oncological_image)

Prizes (in total 22000 CHF)

- 1st place, 2900 CHF (Swiss Francs) / 100% wavier Voucher and invited for publication in the special issue of Cancers (JCR 2021 IF = 6.575)
- 2nd place, 1450 CHF (Swiss Francs) / 50% wavier Voucher and invited for publication in the special issue of Cancers (JCR 2021 IF = 6.575)
- 3rd place, 1450 CHF (Swiss Francs) Voucher and invited for publication in the special issue of Cancers (JCR 2021 IF = 6.575)
- 4th place, 1450 CHF (Swiss Francs) Voucher and invited for publication in the special issue of Cancers (JCR 2021 IF = 6.575)
- 5th place, 1450 CHF (Swiss Francs) Voucher and invited for publication in the special issue of Cancers (JCR 2021 IF = 6.575)
- 6th place, 1450 CHF (Swiss Francs) Voucher and invited for publication in the special issue of Cancers (JCR 2021 IF = 6.575)
- 7th place, 1450 CHF (Swiss Francs) Voucher and invited for publication in the special issue of Cancers (JCR 2021 IF = 6.575)
- 8th place, 1300 CHF (Swiss Francs) Voucher and invited for publication in the special issue of Diagnostics (JCR2021 IF= 3.992)
- 9th place, 1300 CHF (Swiss Francs) Voucher and invited for publication in the special issue of Diagnostics (JCR2021 IF= 3.992)
- 10th place, 1300 CHF (Swiss Francs) Voucher and invited for publication in the special issue of Diagnostics (JCR2021 IF= 3.992)
- 11th place, 1300 CHF (Swiss Francs) Voucher and invited for publication in the special issue of Diagnostics (JCR2021 IF= 3.992)
- 12th place, 1300 CHF (Swiss Francs) Voucher and invited for publication in the special issue of Diagnostics (JCR2021 IF= 3.992)
- 13th place, 1300 CHF (Swiss Francs) Voucher and invited for publication in the special issue of Diagnostics (JCR2021 IF= 3.992)
- 14th place, 260 CHF (Swiss Francs) Voucher and invited for publication in the special issue of Diagnostics (JCR2021 IF= 3.992)
- 15th place, 260 CHF (Swiss Francs) Voucher and invited for publication in the special issue of Diagnostics (JCR2021 IF= 3.992)
- 16th place, 260 CHF (Swiss Francs) Voucher and invited for publication in the special issue of Diagnostics (JCR2021 IF= 3.992)
- 17th place, 260 CHF (Swiss Francs) Voucher and invited for publication in the special issue of Diagnostics (JCR2021 IF= 3.992)
- 18th place, 260 CHF (Swiss Francs) Voucher and invited for publication in the special issue of Diagnostics (JCR2021 IF= 3.992)
- 19th place, 260 CHF (Swiss Francs) Voucher and invited for publication in the special issue of Diagnostics (JCR2021 IF= 3.992)
- 20th place, 260 CHF (Swiss Francs) Voucher and invited for publication in the special issue of Diagnostics (JCR2021 IF= 3.992)
- 21st place, 260 CHF (Swiss Francs) Voucher and invited for publication in the special issue of Diagnostics (JCR2021 IF= 3.992)
- 22nd place, 260 CHF (Swiss Francs) Voucher and invited for publication in the special issue of Diagnostics (JCR2021 IF= 3.992)
- 23rd place, 260 CHF (Swiss Francs) Voucher and invited for publication in the special issue of Diagnostics (JCR2021 IF= 3.992)

## License
The challenge materials are released under a creative commons license, which allows for personal and research use only. For a commercial license please contact Prof Ching-Wei Wang. You can view a license summary here:  
http://creativecommons.org/licenses/by-nc/4.0/


## Contact
Prof. Ching-Wei Wang  
  
cweiwang@mail.ntust.edu.tw; cwwang1979@gmail.com

Nabila Puspita Firdi

m11023802@mail.ntust.edu.tw; nabilapuspita.firdi@gmail.com
  
National Taiwan University of Science and Technology

## Reference
[1] Wang et al. (2022) Weakly Supervised Deep Learning for Prediction of Treatment Effectiveness on Ovarian Cancer from Histopathology Images, Computerized Medical Imaging and Graphics, 99.102093,1-26
https://doi.org/10.1016/j.compmedimag.2022.102093

[2] Coudray et al. (2018) Classification and mutation prediction from non–small cell lung cancer histopathology images using deep learning, Nature Medicine, 1559-1567, 24(10)
https://doi.org/10.1038/s41591-018-0177-5

[3] Campanella et al. (2019) Clinical-grade computational pathology using weakly supervised deep learning on whole slide images, Nature Medicine, 1301-1309, 25(8)
https://doi.org/10.1038/s41591-019-0508-1

[4] Wang et al. (2022) Histopathological whole slide image dataset for classification of treatment effectiveness to ovarian cancer, Scientific Data, 9(25), 1-5
https://doi.org/10.1038/s41597-022-01127-6

