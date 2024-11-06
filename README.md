# Lip-Bengal-Dataset

Largest Lip-reading dataset in Bengali Language. It contains lipreading image data of 150 speakers reading 550 Bengali words. This dataset has been submitted as a journal in 'Data in Brief'.

Google Drive Link : https://drive.google.com/drive/folders/1CgOg35Cfs3H6-vHmG11LDt0qlS6q--jt?usp=sharing

Huggingface link (640 x 480) : https://huggingface.co/datasets/tanjilaronno2024/LipBengal/tree/main

Figshare : https://figshare.com/articles/dataset/LipBengal_Dataset/26008285?file=46992286

Preprocessing and annotation codes for generating Lip-Bengal dataset from raw videos is 
For preprocessing and annotation go to [Preprocessing Code](finalDatasetCode.ipynb)


[Folder Structure](DataStructure.PNG)

## PLEASE NOTE
## Usage Guidelines

To replicate the exact classes and results as presented in our original paper, **researchers are advised to use the `tensorflow.strings.unicode_split` function**. This function ensures a consistent split of phonemes, especially when handling complex Bengali characters with diacritical marks or under-dots.

## Phoneme Splitting in TensorFlow

When using TensorFlow’s string-splitting functions, certain phonemes with **diacritical marks or under-dot modifications** (such as **ড়, র, ঢ়, য়**) may result in **variable class separations**. For example:

- In the word **'বাড়ি'** (bari), the phoneme **‘ড়’** may be split into distinct units.
- In contrast, in the word **'দাড়ি'** (hari), the same phoneme **remains fixed** during splitting.

These cases are illustrated in the following figure for clarity.



![class](https://github.com/user-attachments/assets/027c24b5-9f91-471a-aa14-0d2e04953672)
