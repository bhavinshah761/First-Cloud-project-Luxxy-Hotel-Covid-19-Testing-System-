# First-Cloud-project-Luxxy-Hotel-Covid-19-Testing-System-

In the first phase of the project, we used Terraform to provision infrastructure for migrating a mock-luxury hotel's covid-testing app and data from on-site storage solutions to the cloud.

In the second phase, we converted an app to run inside of a Kubernetes cluster deployed inside a Docker container using a Docker image. Once deployed, this app can run anywhere the Docker engine is supported. Pre-requisites from the application were used to build the Docker file, a set of instructions used to build the Docker image, including application files and libraries. Once built, the Docker image lives in the GCR for use by the Kubernetes cluster to perform app functionality. Also, using AWS IAM services we can connect the S3 bucket created for file storage to communicate to the Kubernetes cluster privately, in the cloud.

In the third & final phase, data is migrated from on-premises servers to the newly adopted cloud environment. Data was provided in the form of a dump file, which was imported to our previously created Google Cloud SQL database. PDF files were also extracted, zipped, and copied into the S3 bucket created for file storage. Once connected to the Cloud SQL instance, data was imported and a then we connected to the AWS shell and imported all files to the bucket.
