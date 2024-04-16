### If you need to test on local, please use Python 3.6.8.

### The result report is in report.ipynb.

### Before running report.ipynb, please create an anaconda environment:

```bash
conda create -n [your_env_name] python=3.6.8
```

### And install the required modules:

```bash
pip install -r requirements.txt
```

### Then you can run the report.ipynb.

### Please also modify the path for MNIST data if needed:

##### i.e. PySpark can directly read .csv.tar.gz as spark dataframe for pyspark 2.4.0
##### i.e. It is recommended to unzip the data.

```python
mnist_train = spark.read.options(header = False).schema(schema).csv("your-mnist-train.csv.tar.gz").dropna()
mnist_test = spark.read.options(header = False).schema(schema).csv("your-mnist-test.csv.tar.gz").dropna()
```