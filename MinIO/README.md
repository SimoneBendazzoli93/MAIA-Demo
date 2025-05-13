# MinIO

<div style="text-align: center;">
    <img src="https://cdn-images-1.medium.com/max/2400/0*QudNr5xo7HArqDlR" alt="MAIA Logo" style="width: 50%;">
</div>




MinIO is an open-source object storage server that is compatible with Amazon S3. It is designed to be lightweight and easy to deploy, making it a popular choice for developers and organizations looking for a cost-effective solution for storing and managing large amounts of data.

In MAIA, MinIO is used to store and share generic files, such as images, videos, and documents, including images not in DICOM format. MinIO provides a simple and intuitive web interface for managing files, as well as a RESTful API for programmatic access.

## Accessing MinIO

To access MinIO, follow the link in the MAIA dashboard. 
To authenticate, you can either use your MAIA credentials or use the access key and secret key provided in the MAIA environment variables.
The access key and secret key can be retrieved from the MAIA Workspace by running the following command in the terminal:
```bash
echo $MINIO_ACCESS_KEY
echo $MINIO_SECRET_KEY
```
Once logged in, you can create buckets, upload files, and manage your data using the MinIO web interface or the MinIO client.

For more information on how to use the MinIO API, refer to the tutorials in the [MinIO Tutorial](https://github.com/kthcloud/MAIA/blob/master/docker/MAIA-Workspace/Tutorials/MinIO.ipynb) documentation.

To synchronize files between your MAIA Workspace and MinIO, you can run the following command in the terminal:
```bash
mc mirror [--watch]  minio/BUCKET LOCAL_FOLDER
```