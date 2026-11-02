#ResNet18 Based Semi-Supervised Image Classification

This repository contains my solution to the **Machine Learning Engineer Challenge** conducted by [HyperVerge](https://hyperverge.co/). It includes both a **baseline supervised model** and a **semi-supervised extension** using pseudo-labeling.

---

## 📁 Dataset Structure

The dataset (provided as a `.zip`) contains:
- `labeled_data/` → images with labels in CSV format
- `unlabeled_data/` → images without labels
- `test_images/` → programmatically created

---

## ✅ Phase 1: Supervised Learning

- Model: **ResNet-18 (pretrained on ImageNet)**
- Trained on labeled data with custom transforms
- Accuracy improved over 5 epochs from ~57% to ~98%

---

## 🔁 Phase 2: Semi-Supervised Learning

- Used pseudo-labeling on unlabeled images
- Only high-confidence predictions (≥ 90%) included
- Combined pseudo-labeled + real labeled data
- Retrained to further boost generalization

---

## 🛠️ Key Challenges Faced

| Problem | Fix |
|--------|-----|
| Images not in class folders | Parsed CSV and built ImageFolder-compatible structure |
| `FileNotFoundError` from path mismatches | Verified directory tree and added path checks |
| Unlabeled predictions too low | Adjusted softmax threshold & confidence logic |
| No test set provided | Programmatically split and built `test_images/` |

---

## 📦 Output

- `phase1_predictions.csv`
- `phase2_predictions.csv`
- `resnet18_phase2.pth` (optional saved model)

---

## 🧠 Technologies

- Python
- PyTorch
- torchvision
- pandas, tqdm
- Google Colab

---

## 📣 Shoutout

Even though I wasn't selected in the final round, the challenge taught me more than a course could. Special thanks to the team at HyperVerge for this learning experience!

---

## 🔗 Connect with Me

Feel free to reach out on [LinkedIn]([https://linkedin.com/in/YOURPROFILE](https://www.linkedin.com/in/mrishika-dhinakaran/)) or fork the repo and try it out!


