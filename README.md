This repo demonstrates using the SageMaker Python SDK on Linux, without SM notebooks, SM Studio, or Jupyter.

1. Install git
```
sudo yum install git -y
```

2. Install and configure the [AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-getting-started.html)

3. Install [Anaconda](https://www.anaconda.com/)

4. Create virtual environment, install packages, and clone this repo
```
conda create -n sm-python-sdk python==3.9 -y
conda activate sm-python-sdk
pip install pandas tensorflow sagemaker
git clone https://github.com/tmac8972/sm-python-sdk
cd sm-python-sdk
```

5. Populate [SM execution role](https://github.com/tmac8972/sm-python-sdk/blob/0b0adecdb7c6a2316fefdd181168dc4aa07290c5/sm_training.py#L5) in local copy of ```sm_training.py```

6. Use SM Python SDK to create SM training job and download trained model locally
```
python sm_training.py
```

