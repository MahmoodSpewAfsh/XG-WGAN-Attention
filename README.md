## README for WGAN-GP Ring Resonator GAN Model

**Description:**  
This project leverages a Wasserstein GAN with Gradient Penalty (WGAN-GP) to generate synthetic transmission spectra for photonic ring resonators. It conditions on physical parameters such as wavelength, gap, input radius, and waveguide width, providing realistic data that can enhance supervised learning models or support design exploration in photonic systems.

### 📁 Files
- `wgan-gp-Ring.ipynb`: Jupyter notebook containing the complete implementation of the WGAN-GP model for generating ring resonator transmission data.

### 📋 Overview
This project trains a WGAN-GP model to generate synthetic optical transmission spectra for integrated photonic ring resonators, based on a given set of physical features. These include:

- `wavelength`
- `gap`
- `r_in`
- `width`

The aim is to generate synthetic samples that mimic real physical transmission values, which can then be used to augment training datasets for predictive models like XGBoost.

### ⚙️ Features
- Uses PyTorch for neural network construction.
- Implements WGAN with gradient penalty for stable training.
- Includes generator and critic (discriminator) architectures.
- Visualizes loss curves and generated vs. real transmission distributions.

### 🧪 Dependencies
You can install all the required packages using pip:
```bash
pip install torch torchvision pandas numpy matplotlib seaborn scikit-learn
```

### 🚀 How to Run
1. Clone the repository or download the `.ipynb` file.
2. Place it in a Jupyter-compatible environment (e.g., Jupyter Lab, VS Code, Google Colab).
3. Run the cells sequentially:
   - The notebook loads or simulates data.
   - It defines the generator and critic networks.
   - Training is performed with periodic visualization.

### 📊 Input Data Format
The data used should be a DataFrame or CSV with at least the following columns:
- `wavelength`
- `gap`
- `r_in`
- `width`
- `transmission`

The model is trained to learn the distribution of `transmission` values conditioned on the physical parameters.

### 🧠 Model Details
- **Generator**: Takes a latent vector `z` concatenated with physical features, and generates a synthetic `transmission` value.
- **Critic**: Evaluates real vs. generated data tuples of features and `transmission`.
- **Loss**: Wasserstein loss with gradient penalty.

### 📈 Outputs
- Trained model weights (optional, if saved).
- Loss curves for critic and generator.
- Histograms or scatter plots comparing real and generated transmissions.

### 📌 Applications
- Data augmentation for supervised models predicting transmission in ring resonators.
- Exploration of learned feature-transmission relationships.

### 🧾 License
This project is released under the MIT License.

### 👨‍💻 Authors
---
---
For any issues or questions, feel free to open an issue or reach out directly.

Happy simulating! ✨

