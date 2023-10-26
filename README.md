# WS-DINO

Pytorch implementation of [Self-Supervised Learning of Phenotypic Representations from Cell Images with Weak Labels](https://arxiv.org/abs/2209.07819)  

**REPRODUCTION**
- Use `meta_csv_files/csvGenerator.ipynb` to generate `loaddata.csv` and `LoadDataFile.csv` for illumination correction
- Run `preprocessing/BBBC021_illuminationCalculate.cpproj`, then run `preprocessing/BBBC021_illuminationApply.cpproj` to generate training dataset
- Use python version 3.6, PyTorch version 1.7.1, CUDA 11.0 and torchvision 0.8.2.
- To run with 2 GPUs as the paper, use:
```
python -m torch.distributed.launch --nproc_per_node=2 main_dino.py --arch vit_small --data_path /path/to/imagenet/train --output_dir /path/to/saving_dir
```

**PRETRAINED WEIGHTS**
 [Download weights from here](https://drive.google.com/drive/folders/1y4yzkYQ8g6eytobmfC9mNmist4FfONWS?usp=sharing)

**UPDATE**

This paper has been accepted to [LMRL](https://www.lmrl.org/) @ [NeurIPS 2022](https://neurips.cc/). We look forward to presenting in December.



## Citation
If you find this work useful, please consider citing our paper:
```
@article {10.48550/arXiv.2209.07819,
	author = {Cross-Zamirski, Jan and Mouchet, Elizabeth and Williams, Guy and Sch{\"o}nlieb, Carola-Bibiane and Turkki, Riku and Wang, Yinhai},
	title = {Self-Supervised Learning of Phenotypic Representations from Cell Images with Weak Labels},
	year = {2022},
	doi = {https://doi.org/10.48550/arXiv.2209.07819},
	journal = {arXiv Preprint arXiv:2209.07819}
}

