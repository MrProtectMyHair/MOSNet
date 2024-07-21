# MOSNet
Implementation of  "MOSNet: Deep Learning based Objective Assessment for Voice Conversion"
https://arxiv.org/abs/1904.08352

## Dependency
Linux Ubuntu 18.04
- GPU: GeForce RTX 2080 Ti
- Driver version: 550.90.07
- CUDA version: 10.1

Python 3.8
- tensorflow-gpu==2.1.0 (cudnn=7.6.0)
- scipy
- pandas
- matplotlib
- librosa

### Environment set-up
For example,
```
conda create -n mosnet python=3.8
conda activate mosnet
pip install -r requirements.txt
pip install librosa==0.8.1
pip install numpy==1.19.5
conda install cudnn=7.6.0
pip install h5py==2.10.0
```

## Usage


### Evaluating your custom waveform samples

1. Put the waveforms you wish to evaluate in a folder. For example, `<path>/<to>/<samples>`
2. Run `python ./custom_test.py --rootdir <path>/<to>/<samples>`

This script will evaluate all the `.wav` files in `<path>/<to>/<samples>`, and write the results to `<path>/<to>/<samples>/MOSnet_result_raw.txt`. By default, the `pre_trained/cnn_blstm.h5` pretrained model is used. If you wish to use other models, please specify a different `--pretrained_model` and also change `from model import <model_to_be_used>`.

## Citation

If you find this work useful in your research, please consider citing:
```
@inproceedings{mosnet,
  author={Lo, Chen-Chou and Fu, Szu-Wei and Huang, Wen-Chin and Wang, Xin and Yamagishi, Junichi and Tsao, Yu and Wang, Hsin-Min},
  title={MOSNet: Deep Learning based Objective Assessment for Voice Conversion},
  year=2019,
  booktitle={Proc. Interspeech 2019},
}
```
 
 
## License

This work is released under MIT License (see LICENSE file for details).


## VCC2018 Database & Results

The model is trained on the large listening evaluation results released by the Voice Conversion Challenge 2018.<br>
The listening test results can be downloaded from [here](https://datashare.is.ed.ac.uk/handle/10283/3257)<br>
The databases and results (submitted speech) can be downloaded from [here](https://datashare.is.ed.ac.uk/handle/10283/3061)<br>
