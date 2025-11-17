## Using Venv

Create a virtual environment in python and activate it by those commands:

Create venv

```bash
python3 -m venv venv
```

Activate venv

```bash
source venv/bin/activate
```

Install dependencies using pip

```bash
pip3 install -r requirements.txt
```



## Docker images

### Create an image of the file

```bash
docker build -t python-app:v2 .


# where:
# - -t is the option to tag the image
# - python-app:v2 is the name of the image and :v2 is the version tag
# - . is the current directory
```


### Run image

```bash
docker run -p 8080:5000 python-app:v2

# where:
# - -p is the option to set port config
# - 8080:5000 is redirecting the server originally in 5000 to port 8080 in container
# - python-app:v2 is the name of the image
```

Now, I can access the server running in docker trough http://127.0.0.1:8080/api/v1/details



# Using Helm

```bash
healm create python-app
```

It creates the python-app folder inside the folder charts, with the necessary files to compile it using Kubernetes.

The idea of Helm is to abstract the k8s objects (deploy, ingress and service) and only manages the values.yaml


# Notes

Using venv
python3 -m venv virtualenvname

Command Syntax:

/path/to/python3 -m venv /path/to/directory/virtual_env_name

Using virtualenv
virtualenv -p python3 virtualenvname

Command Syntax:

virtualenv -p /path/to/python3 /path/to/directory/virtual_env_name

Activate the virtual environment
On Linux, Unix or MacOS, using the terminal or bash shell:

source /path/to/venv/bin/activate

e.g. source virtualenvname/bin/activate

On Unix or MacOS, using the csh shell:

source /path/to/venv/bin/activate.csh

On Unix or MacOS, using the fish shell:

source /path/to/venv/bin/activate.fish

On Windows using the Command Prompt:

path\to\venv\Scripts\activate.bat

On Windows using PowerShell:

path\to\venv\Scripts\Activate.ps1

Deactivating the virtual environment
On Linux, Unix or MacOS, using the terminal or bash shell:

deactivate

On Windows using the Command Prompt:

path\to\venv\Scripts\deactivate.bat

On Windows using PowerShell:

deactivate

This answer is for those who may use a different OS.