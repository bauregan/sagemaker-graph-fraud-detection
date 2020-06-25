# Amazon SageMaker and Deep Graph Library for Fraud Detection in Heterogeneous Graphs

This project shows how to use [Amazon SageMaker](https://aws.amazon.com/sagemaker/) and [Deep Graph Library (DGL)](https://www.dgl.ai/) to train a graph neural network (GNN) model to detect malicious users or fraudulent transactions. See the [project wiki](https://github.com/awslabs/sagemaker-graph-fraud-detection/wiki) to learn more about the techniques used.

## Project Organization
The project is divided into two main modules that preprocess the data and train the GNN respectively.

The [first module](source/sagemaker/data-preprocessing) uses [Amazon SageMaker Processing](https://docs.aws.amazon.com/sagemaker/latest/dg/processing-job.html) to do feature engineering and extract edgelists from a table of transactions or interactions.


The [second module](source/sagemaker/dgl-fraud-detection) shows how to use DGL to define a GNN model and train the model using [Amazon SageMaker training infrastructure](https://docs.aws.amazon.com/sagemaker/latest/dg/deep-graph-library.html).


The [jupyter notebook](source/sagemaker/dgl-fraud-detection.ipynb) shows how to run the full project on an [example dataset](https://linqs-data.soe.ucsc.edu/public/social_spammer/).


The project also contains a [cloud formation template](deployment/sagemaker-graph-fraud-detection.yaml) that deploys the code in this repo and all AWS resources needed to run the project in an end-to-end manner in the AWS account it's launched in.

## Architecture

The project architecture deployed by the cloud formation template is shown here.


<p align="center">
  <img src="http://sagemaker-solutions-us-west-2.s3.amazonaws.com/Fraud-detection-in-financial-networks/deployment/arch.png" width="100%">
</p>

## License

This project is licensed under the Apache-2.0 License.

