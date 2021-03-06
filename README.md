# FastDepth
# Requirements
Install PyTorch on a machine with a CUDA GPU. Our code was developed on a system running PyTorch v0.4.1.
Install the HDF5 format libraries. Files in our pre-processed datasets are in HDF5 format.
```
sudo apt-get update

sudo apt-get install -y libhdf5-serial-dev hdf5-tools

pip3 install h5py matplotlib imageio scikit-image opencv-python
```
# NYU database
Download the preprocessed NYU Depth V2 dataset in HDF5 format and place it under a data folder outside the repo directory. The NYU dataset requires 32G of storage space.
 ```
 mkdir data; cd data
 
 wget http://datasets.lids.mit.edu/fastdepth/data/nyudepthv2.tar.gz
 
 tar -xvf nyudepthv2.tar.gz && rm -f nyudepthv2.tar.gz
```
# Train
```
python3 main.py -train -p 100 --epochs 20
```
# Evaluate
```
python3 main.py --evaluate /home/usr/results/trained_model.pth.tar
```
## Authors (Equally contributed)
* **Sunny Yehuda*** - *sunnyyehuda@gmail.com*
* **Gil Rafalovich*** - *rafalovichg@gmail.com*

# Reference
```
@inproceedings{icra_2019_fastdepth,
	author      = {{Wofk, Diana and Ma, Fangchang and Yang, Tien-Ju and Karaman, Sertac and Sze, Vivienne}},
	title       = {{FastDepth: Fast Monocular Depth Estimation on Embedded Systems}},
	booktitle   = {{IEEE International Conference on Robotics and Automation (ICRA)}},
	year        = {{2019}}
}
```
