# Checkpoint 2 - Research: Types of Cloud Storage

## Comparison of Cloud Storage Types

| Storage Type | Description | Primary Use Case | Cloud Provider Example |
|---|---|---|---|
| **Block Storage** | Stores data in fixed-size blocks. Each block can be managed separately. | Best for virtual machine disks, operating systems, and databases. | AWS Elastic Block Store (EBS) |
| **File Storage** | Stores data as files organized into folders and directories. | Best for shared files, documents, and applications that need a shared file system. | AWS Elastic File System (EFS) |
| **Object Storage** | Stores data as objects containing the data, metadata, and a unique identifier. | Best for user-uploaded images, videos, backups, and other unstructured data. | AWS Simple Storage Service (S3) |

## Why Object Storage Is the Best Choice for User-Uploaded Images

Object Storage is the best choice for storing user-uploaded images because it can handle large amounts of data and easily scale as the number of images increases. It also provides unique identifiers and metadata that help organize and retrieve images efficiently. For these reasons, AWS S3 is a suitable solution for storing and managing user-uploaded images.
