# Orthanc

<div style="text-align: center;">
    <img src="https://www.orthanc-server.com/img/Carousel/1-Logo.png" alt="MAIA Logo" style="width: 50%;">
</div>




Orthanc is a lightweight, open-source DICOM server for medical imaging. It is designed to be easy to use and deploy, making it an ideal choice for developers and researchers working with medical images. Orthanc provides a RESTful API for accessing and managing DICOM images, as well as a web interface for viewing and annotating images.

## DICOM Upload

In the MAIA Namespace, we have set up an Orthanc server that allows you to upload DICOM files. The server is accessible through three different methods: the Orthanc web interface, the DICOMweb API, and the DICOM REST API. The web interface is the easiest way to upload DICOM files, while the DICOMweb API and REST API provide more advanced options for developers.

### Orthanc Web Interface
To upload DICOM files using the Orthanc web interface, follow these steps:
1. Open the Orthanc web interface by clicking on the "Orthanc" link in the MAIA dashboard.
2. Click on the "Upload" button in the top right corner of the page.
3. Select the DICOM files you want to upload from your local machine.
4. Click on the "Upload" button to start the upload process.
5. Once the upload is complete, you will see the uploaded files in the Orthanc web interface.

### DICOMweb API
To upload DICOM files using the DICOMweb API, follow these steps:
1. Get the DICOMweb API URL from the MAIA dashboard, in the Orthanc DICOMweb section.
2. Use a DICOMweb client library or tool  ([3D Slicer, DICOMWebBrowser Plugin](https://github.com/lassoan/SlicerDICOMwebBrowser)) to upload the DICOM files.


### DICOM REST API
To upload DICOM files using the DICOM REST API, follow these steps:
1. Get the DICOM REST API URL from the MAIA dashboard, in the Orthanc DICOMweb section.
2. Use a DICOM REST client library or tool ([pynetdicom](https://pydicom.github.io/pynetdicom/stable/)) to send a POST request to the DICOM REST API URL with the DICOM files as the request body.

Example using Python:
```python
python -m pynetdicom storescu <ADDRESS> <PORT> -r <FILE_FOLDER>
```
4. Once the upload is complete, you will see the uploaded files in the Orthanc web interface.