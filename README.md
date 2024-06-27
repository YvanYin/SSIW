This repository contains the source code of our paper:
[Wei Yin, Yifan Liu, Chunhua Shen, Anton van den Hengel, Baichuan Sun, The devil is in the labels: Semantic segmentation from sentences](https://arxiv.org/abs/2202.02002)


Embedding: https://cloudstor.aarnet.edu.au/plus/s/gXaGsZyvoUwu97t
CKPT: https://cloudstor.aarnet.edu.au/plus/s/AtYYaVSVVAlEwve

Quick start:
1. Download the embedding and ckpt and put them into Test_Minist/models/
2. Put your test images in Test_Minist/test_imgs/
3. cd Test_Minist
4 .bash run.sh


See the following branch for a new free text demo:
https://github.com/irfanICMLL/SSIW/tree/master

## Define the label list
You can choose the label list used for semantic segmentation, for instance:
```python
python tools/test.py --config test_720_ss --user_label dog mouse horse rug_floormat wall person vegetation pizza
```
Here is the comparison between adding label "cat" or not:

![image](https://github.com/irfanICMLL/SSIW/blob/master/Test_Minist/ann_imgs/img8_vis_1.png)![image](https://github.com/irfanICMLL/SSIW/blob/master/Test_Minist/ann_imgs/img8_vis_2.png)


## Define new labels
You can also define your own categories described by sentences, for instance:
```python
python tools/test.py --config test_720_ss --new_definitions="{'deer': 'This is an image of deer, similar to sheep or dog.'}"
```

## 📧 Citation
```
@article{SSIW,
  title={Scaling Up Multi-domain Semantic Segmentation with Sentence Embeddings},
  author={Yin, Wei and Liu, Yifan and Shen, Chunhua and Sun, Baichuan and van den Hengel, Anton},
  journal={International Journal of Computer Vision},
  pages={1--16},
  year={2024},
  publisher={Springer}
}
```


## License
This code is for non-commercial use only. It's released under GPL license. For commercial use, please contact authors.
