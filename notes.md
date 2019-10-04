# Fast.AI course Oct 2019

## Compute

Using a pre-built ubuntu image. It contains EBS (storage that does not disappear when stopping the
instance).

- AWS p2.xlarge Frankfurt
- Using ssh key-pairs: fastai_frankfurt_aws_id_rsa
- URL
  - 2019.10.02:
    - public: ec2-3-122-236-198.eu-central-1.compute.amazonaws.com
    - public ip (for ssh): 3.122.236.198
    - private: 172.31.41.79
  - 2019.10.04:
    - public ip (for ssh): 18.194.139.213

### Connecting from terminal

```bash
ssh -i ~/.ssh/fastai_frankfurt_aws_id_rsa -L localhost:8888:localhost:8888 ubuntu@3.122.236.198
```

### Setting up Fast.ai

```bash
git clone https://github.com/fastai/course-v3
```

```bash
conda update conda
conda install -c pytorch -c fastai fastai pytorch torchvision cuda92

cd course-v3/nbs/dl1
```

```bash
jupyter notebook
```

### Access notebook

Connect to `localhost:8888`.

You might need to copy-paste the link (token) that Jupyter spits out when it starts.

**WARNING**: *You must remember to stop the instance after each session. If not, you will lose a lot of money!*
