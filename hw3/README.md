In this assignment you will practice writing Convolutional Neural Networks. The goals of this assignment
are as follows:

- implement **batch normalization** for training deep networks
- understand the architecture of **Convolutional Neural Networks**
- gain an understanding of how a modern deep learning library (PyTorch) works
  and gain practical experience using it to train models.

## Setup
Make sure your machine is set up with the assignment dependencies.

**[Option 1] Use Anaconda:**
The preferred approach for installing all the assignment dependencies is to use
[Anaconda](https://www.continuum.io/downloads), which is a Python distribution
that includes many of the most popular Python packages for science, math,
engineering and data analysis. Once you install it you can skip all mentions of
requirements and you are ready to go directly to working on the assignment.

**[Option 2] Manual install, virtual environment:**
If you do not want to use Anaconda and want to go with a more manual and risky
installation route you will likely want to create a
[virtual environment](http://docs.python-guide.org/en/latest/dev/virtualenvs/)
for the project. If you choose not to use a virtual environment, it is up to you
to make sure that all dependencies for the code are installed globally on your
machine. To set up a virtual environment, run the following:

```bash
cd hw3
sudo pip install virtualenv      # This may already be installed
virtualenv .env                  # Create a virtual environment
source .env/bin/activate         # Activate the virtual environment
pip install -r requirements.txt  # Install dependencies
# Work on the assignment for a while ...
deactivate                       # Exit the virtual environment
```

**Download data:**
Once you have the starter code, you will need to download the CIFAR-10 dataset.
Run the following from the `hw3` directory:

```bash
cd deeplearning/datasets
./get_datasets.sh
```

If you are on Mac, this script may not work if you do not have the wget command
installed, but you can use curl instead with the alternative script.
```bash
cd deeplearning/datasets
./get_datasets_curl.sh
```

**Start IPython:**
After you have the CIFAR-10 data, you should start the IPython notebook server
from the `hw3` directory.

**NOTE:** If you are working in a virtual environment on OSX, you may encounter
errors with matplotlib due to the
[issues described here](http://matplotlib.org/faq/virtualenv_faq.html).
You can work around this issue by starting the IPython server using the
`start_ipython_osx.sh` script from the `hw3` directory; the script
assumes that your virtual environment is named `.env`.

**Compile the Cython extension:** Convolutional Neural Networks require a very
efficient implementation. We have implemented of the functionality using
[Cython](http://cython.org/); you will need to compile the Cython extension
before you can run the code. From the `deeplearning` directory, run the following
command:

```bash
python setup.py build_ext --inplace
```

### Q1: Batch Normalization
In the IPython notebook `BatchNormalization.ipynb` you will implement batch
normalization, and use it to train deep fully-connected networks.

### Q3: Design 2D FIR Filter
In the IPython Notebook `HandDesinFilters.ipynb` you will design some interesting image 
filters.

### Q3: ConvNet
In the IPython Notebook `ConvolutionalNetworks.ipynb` you will implement several
new layers that are commonly used in convolutional networks as well as implement
a small convolutional network.
