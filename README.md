# The HIST framework for stock trend forecasting
The implementation of the paper "[HIST: A Graph-based Framework for Stock Trend Forecasting via Mining Concept-Oriented Shared Information](https://arxiv.org/abs/2110.13716)".
![image](https://user-images.githubusercontent.com/25242325/139006788-b51b18c2-1bcf-44b8-921a-b10d4b197e91.png)

## Environment
1. Install python3.7, 3.8 or 3.9. 
2. Install the requirements in [requirements.txt](https://github.com/Wentao-Xu/HIST/blob/main/requirements.txt).
3. Install the quantitative investment platform [Qlib](https://github.com/microsoft/qlib) and download the data from Qlib:
	```
	# install Qlib from source
	!pip install --upgrade  cython
	!git clone https://github.com/microsoft/qlib.git && cd qlib
	# Download the stock features of Alpha360 from Qlib
	!python qlib/scripts/get_data.py qlib_data --target_dir ~/.qlib/qlib_data/cn_data --region cn --version v2
	```
## Reproduce the stock trend forecasting results
![image](https://user-images.githubusercontent.com/25242325/139006416-c0847b7e-6090-4bd9-9990-567d74198ad0.png)
### Reproduce our HIST framework
```
# CSI 100
!python learn.py --model_name HIST --data_set csi100 --hidden_size 128 --num_layers 2 --outdir ./HIST/output/csi100_HIST
```

* ALSTM+TRA 

	We reproduce the ALSTM+TRA with its [source code](https://github.com/microsoft/qlib/tree/main/examples/benchmarks/TRA).

## Citation
Please cite the following paper if you use this code in your work.
```
@article{xu2021hist,
  title={HIST: A Graph-based Framework for Stock Trend Forecasting via Mining Concept-Oriented Shared Information},
  author={Xu, Wentao and Liu, Weiqing and Wang, Lewen and Xia, Yingce and Bian, Jiang and Yin, Jian and Liu, Tie-Yan},
  journal={arXiv preprint arXiv:2110.13716},
  year={2021}
}
```
