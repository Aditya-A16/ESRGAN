# Upscale Image with ESRGAN

This project utilizes the ESRGAN (Enhanced Super-Resolution Generative Adversarial Network) model to upscale images by a factor of 4. ESRGAN is a deep learning model trained to enhance the details and quality of images, making them sharper and more visually appealing.

## Project Structure

├── ESRGAN \
│   ├── net_interp.py\
│   ├── RRDBNet_arch.py\
│   ├── run.py\
│   ├── transer_RRDB_models.py\
│   ├── input\
│   │   └── comic.png\
│   ├── models\
│   │   └── RRDB_ESRGAN_x4.pth\
│   └── results\
│       └── comic_high_res.png\
└──




## Instructions on How to Run

### Prerequisites

1. Create a virtual environment (optional but recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate 
    # On Windows, use 'venv\Scripts\activate'

2. Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```

## Upscale an Image  

1. Place your low-resolution image in the input/ folder.

2. Run the following command to upscale the image:

  ```bash
  python run.py
  ```

3. he upscaled image will be saved in the results/ folder

## Additional Instructions (GPU)
* If you have a GPU and want to run the model on it, install the latest PyTorch module with CUDA support from pytorch.org.

* Uncomment line 9 and comment line 10 in run.py:
  ```
  # device = torch.device('cuda')  # if you want to run on GPU, change 'cuda' -> cpu
  device = torch.device('cpu')
  ```

#### Now you are ready to enhance your images using ESRGAN! For more details and customization, refer to the source code in the ESRGAN/ directory.