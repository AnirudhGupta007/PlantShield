GAN-Based Image Generation Model
================================

Overview
--------

This project implements a **GAN-based model** for generating images conditioned on text descriptions. The model is trained using a dataset of images with associated text embeddings.

Features
--------

-   Implements a **Generator** and **Discriminator** for image synthesis.
-   Uses **text embeddings** to condition image generation.
-   Supports **checkpointing** and **resuming training**.
-   Saves **generated images** periodically.
-   Logs training metrics to `training_log.csv`.

Project Structure
-----------------

```
project_root/
│-- new_model_1.ipynb     # Jupyter Notebook for training and evaluation
│-- requirements.txt      # Required dependencies
│-- training_log.csv      # Logs for model training (D_loss, G_loss)
│-- LICENSE               # License file
│-- README.md             # Project documentation

```

Installation
------------

To set up the project, follow these steps:

```
# Clone the repository
git clone https://github.com/yourusername/your-repository.git
cd your-repository

# Create a virtual environment (optional but recommended)
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`

# Install dependencies
pip install -r requirements.txt

```

Usage
-----

Run the Jupyter Notebook to train the model:

```
jupyter notebook new_model_1.ipynb

```

### Training Process

-   The **Discriminator** and **Generator** are trained separately.
-   Loss values for **D_loss** (Discriminator loss) and **G_loss** (Generator loss) are printed at regular intervals.
-   The model saves **generated images** every **20 epochs** to `generated_images/`.
-   Model weights are saved every **50 epochs** in `saved_models/`.
-   Supports **resuming training** from the last checkpoint.

### Example Training Output:

```
Epoch [1/300], Step [5/100], D_loss: 0.4201, G_loss: 2.1567
Epoch [20/300], Avg D_loss: 0.3894, Avg G_loss: 2.4156

```

Dataset
-------

The dataset consists of images and corresponding text embeddings. Images are processed using PyTorch DataLoader.

Results
-------

-   **Training logs** are stored in `training_log.csv`.
-   **Generated images** are saved in `generated_images/` (e.g., `epoch_20.png`).
-   **Model checkpoints** are saved in `saved_models/` as `.pth` files.
-   **Loss values** indicate stable training progress with decreasing **D_loss** and increasing **G_loss**.

Contributing
------------

Feel free to open issues or submit pull requests if you want to improve this project.

License
-------

This project is licensed under the MIT License - see the LICENSE file for details.
