# AIM-CCReID
An official implementation of our CVPR'23 paper:

《Good is Bad: Causality Inspired Cloth-Debiasing for Cloth-Changing Person Re-Identification》

[\[Paper Link\]](https://openaccess.thecvf.com/content/CVPR2023/papers/Yang_Good_Is_Bad_Causality_Inspired_Cloth-Debiasing_for_Cloth-Changing_Person_Re-Identification_CVPR_2023_paper.pdf)
[\[Repo\]](https://github.com/BoomShakaY/AIM-CCReID)
[\[About Me\]](https://gavinyoung1.github.io/)


<div style="display: flex; justify-content: center; align-items: center;">
  <img src="Figures/CVPR23.jpg" alt="motivation" width="200" />
  <img src="Figures/Framework.png" alt="framework" width="430" />
</div>

#### News 
2023.10.24 The full codes are released! 

#### Requirements
- Python 3.6
- Pytorch 1.6.0
- yacs
- apex
(remind: the apex is optional, not recommended if you have enough GPU memory; just comment all amp related codes)

## Performance of AIM 
<table>
	<tr>
	    <td > </td>
	    <td colspan="4" align="center">RRCC</td>
	    <td colspan="4" align="center">LTCC</td>
	</tr >
	<tr >
      <td>   </td>
	    <td colspan="2" align="center"> Standard</td>
      <td colspan="2" align="center"> Cloth-Changing</td>
	    <td colspan="2" align="center"> Standard</td>
      <td colspan="2" align="center"> Cloth-Changing</td>
	</tr>
	<tr>
	    <td> </td>
      <td>R@1</td>
      <td>mAP</td>
      <td>R@1</td>
      <td>mAP</td>
      <td>R@1</td>
      <td>mAP</td>
      <td>R@1</td>
      <td>mAP</td>
	</tr>
	<tr>
	    <td>Paper</td>
      <td>100.0</td>
      <td>99.9</td>
      <td>57.9</td>
      <td>58.3</td>
      <td>76.3</td>
      <td>41.1</td>
      <td>40.6</td>
      <td>19.1</td>
	</tr>
	<tr>
	    <td>Repo</td>
      <td>100.0</td>
      <td>99.8</td>
      <td>58.2</td>
      <td>58.0</td>
      <td>75.9</td>
      <td>41.7</td>
      <td>40.8</td>
      <td>19.2</td>
	</tr>
</table>
The indicators provided in this repo are broadly the same as those in the paper, and possibly even better (depending on what your focus is)

## Datasets
PRCC is available at [Here](https://drive.google.com/file/d/1yTYawRm4ap3M-j0PjLQJ--xmZHseFDLz/view).

LTCC is available at [Here](https://naiq.github.io/LTCC_Perosn_ReID.html).

LaST is available at [Here](https://github.com/shuxjweb/last).

## Testing
The trained models (weights) are available at [Baidu Disk](https://pan.baidu.com/s/1Du1XgoCim6I_bZtNRm3yPw?pwd=v4ly) or [Google Drive](https://drive.google.com/drive/folders/1xohg_OAHjNyy7LLq3Fq_KowcEP9IlY8k?usp=sharing).
You will find the testing script for prcc and ltcc at `test_AIM.sh`, then modify the resume path to your own path where you placed the weights file.  

To be noticed, you need to modify the `DATA ROOT` and `OUTPUT` in the `configs/default_img.py` to your own path before testing.

## 📖 Citation

If you find our work useful in your research, please consider citing:

```bibtex
@inproceedings{yang2023good,
  title={Good is bad: Causality inspired cloth-debiasing for cloth-changing person re-identification},
  author={Yang, Zhengwei and Lin, Meng and Zhong, Xian and Wu, Yu and Wang, Zheng},
  booktitle={Proceedings of the IEEE/CVF conference on computer vision and pattern recognition},
  pages={1472--1481},
  year={2023}
}
