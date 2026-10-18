# Types of Cloud Storage

| Storage Type | Description | Primary Use Case | Cloud Provider Example |
|---|---|---|---|
| Block Storage | Stores data in fixed-size blocks, each with its own address, and acts like a raw hard drive attached to a server | Operating systems, databases and applications that need fast, low-latency access | AWS EBS (Elastic Block Store) |
| File Storage | Stores data as files in a hierarchy of folders and directories that can be shared over a network | Shared drives, home directories and content that many users or servers access at once | AWS EFS (Elastic File System) |
| Object Storage | Stores data as objects in a flat structure, where each object has the data, metadata and a unique ID, accessed through an API | Images, videos, backups, logs and other massive amounts of unstructured data | AWS S3 (Simple Storage Service) |

## Explanation for the Client

Object Storage is the best choice for your user-uploaded images because it scales almost without limit, so it can hold millions of photos without you managing disk sizes. It is also cost-efficient and keeps each image with its own metadata, which makes the files easy to retrieve through a web API. Unlike containers, which are temporary, object storage keeps your photos safe even if the web server is replaced.
