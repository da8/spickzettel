# working with python environments
    cd <working-directory>
    python -m venv <environment-name>
    source <environment-name>/bin/activate
    python --version
    pip --version

# check if opencv for python is installed
    python -c "import cv2; print(cv2.__version__)"

# prerequisites for opencv for python
    pip install scikit-build
    pip install opencv-python

# Find which version of package is installed with pip
    pip show Package

# list all installed python packages with their version information
    pip list

# Upgrading pip
    python -m pip install -U pip

# install python3-venv
    sudo apt-get install python3-venv

# Change the Python3 default version in Ubuntu
    python --version
    sudo update-alternatives --install /usr/bin/python python /usr/bin/python3 1
    python --version

