### Install dependencies 

```bash
# make a conda environment and install pytorch.
conda create --name model_soups python=3.6
conda activate model_soups
conda install --yes -c pytorch pytorch=1.7.1 torchvision cudatoolkit=11.0

# instructions from https://github.com/openai/CLIP for how to install. Also we will tie to a specific release.
pip install ftfy regex tqdm
pip install git+https://github.com/openai/CLIP.git@40f5484c1c74edd83cb9cf687c6ab92b28d8b656

# additional imports
pip install wget
pip install git+https://github.com/modestyachts/ImageNetV2_pytorch
pip install requests
pip install matplotlib
pip install pandas
pip install tqdm
```


### Step 2: Run

We run this which gets 99%.
```bash
python src/finetune.py --data-location <path to folder containing train and test> --batch-size 128 --model ViT-L/14
```

We run the code above with 4 A40 GPUs. Feel free to also try with a smaller model `--model ViT-B/32`.

