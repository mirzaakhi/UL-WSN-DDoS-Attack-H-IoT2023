# WSN-DDoS-Attack-H-IoT2023

This repository contains the dataset and preprocessing notebook used to develop the poster paper presented at **The 12th IEEE International Conference on Healthcare Informatics (IEEE ICHI 2024)**: 
[**"Time Series Anomaly Detection with CNN for Environmental Sensors in Healthcare-IoT" (IEEE 2024)**](https://ieeexplore.ieee.org/abstract/document/10628718)

The dataset captures **Distributed Denial-of-Service (DDoS)** attacks in a Wireless Sensor Network (WSN) deployed within a Healthcare-IoT (H-IoT) environment. It is generated using the **Cooja IoT network simulator**, with environmental sensors primarily monitoring **room temperature and humidity**. A **Convolutional Neural Network (CNN)** model is trained on this dataset and achieves an accuracy of **92%**.


## 📁 Repository Structure

```
UL-WSN-DDoS-Attack-H-IoT2023/
├── Raw_WSN_DDoS_Attack_H-IoT2023.txt     (raw simulation log)
├── WSN_DDoS_Attack_H-IoT2023.csv         (preprocessed dataset)
└── data_preprocessing.ipynb              (Jupyter notebook for preprocessing)
```

## 📊 Dataset Summary
```
- **Shape**: (11191 rows, 6 columns)
- **Features Used for Model Training**:
  - `id` — unique message index
  - `interval` — time difference (in milliseconds) between the current and previous message from the same node
  - `previous_send_intervals_same_node` — list of previous intervals for the same node
  - `average_previous_send_intervals_same_node` — mean interval over previous sends
  - `previous_sender` — node ID that sends the previous message
  - `malicious` — class label (`1` for malicious, `0` for normal)
```
> These features are derived from the Cooja simulation raw sensor log and are used to train the CNN-based anomaly detection model.

---

### 🏷 Class Distribution
```
| Phase | Class     | Samples |
|-------|-----------|---------|
| Train | Malicious | 2583   |
| Train | Normal    | 8608   |
| Test  | Malicious | 1107   |
| Test  | Normal    | 3690   |
```

## 📘 Citation

If you use this dataset or preprocessing notebook in your work, please cite the following paper:
```
**Plain Text:**
M. A. Khatun, M. Bhattacharya, C. Eising and L. L. Dhirani, *"Time Series Anomaly Detection with CNN for Environmental Sensors in Healthcare-IoT,"* 2024 IEEE 12th International Conference on Healthcare Informatics (ICHI), Orlando, FL, USA, 2024, pp. 522–524, doi: [10.1109/ICHI61247.2024.00075](https://doi.org/10.1109/ICHI61247.2024.00075)
```
**BibTeX:**
```bibtex
@inproceedings{khatun2024cnn,
  author    = {M. A. Khatun and M. Bhattacharya and C. Eising and L. L. Dhirani},
  title     = {Time Series Anomaly Detection with CNN for Environmental Sensors in Healthcare-IoT},
  booktitle = {2024 IEEE 12th International Conference on Healthcare Informatics (ICHI)},
  pages     = {522--524},
  year      = {2024},
  address   = {Orlando, FL, USA},
  doi       = {10.1109/ICHI61247.2024.00075}
}

```
## 👥 Author

- **Mirza Akhi** — University of Limerick, Ireland


## 🛡 License

This dataset and accompanying notebook are licensed under the [Creative Commons Attribution 4.0 International (CC BY 4.0) License](https://creativecommons.org/licenses/by/4.0/).  
You are free to share, adapt, and use the materials for any purpose, provided proper attribution is given to the original author.
