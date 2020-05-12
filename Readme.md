## **Demo: Managing Azure Blob storage by using .NET**

-  Use the Azure Storage SDK for .NET to create and validate blobs and containers in Azure Storage
-  Manage the container by creating, downloading, listing and deleting blobs using the Azure Storage SDK for .NET.

### Preparación del programa

Storage Account: Deberá tener una cuenta de almacenamiento previamente creada, poara ir a por su **connectionstring**

- Ejecutar el comado de creación de proyecto de consola

```c#
dotnet new console -n BlobQuickstartV12 
cd BlobQuickstartV12 
mkdir data
dotnet add package Azure.Storage.Blobs
```

- Configurar la cadena de conección al almacen:

```
PS> setx AZURE_STORAGE_CONNECTION_STRING "<connectionstring>"
```

### Contenido del fichero Program.cs

Las siguientes tareas deberánn estar desarrolladas en el fichero del Program.cs:

**Task 1. Get the connection string**
Retrieve the connection string for use with the application. The storage connection string is stored in an environment variable on the machine running the application called AZURE_STORAGE_CONNECTION_STRING. If the environment variable is created after the application is launched in a console or with Visual Studio, the shell or application needs to be closed and reloaded to take the environment variable into account. 

**Task 2. Create a container**
Create a BlobServiceClient object which will be used to create a container client and creating a unique name for the containerCreate the container and return a container client object.

**Task 3. Upload blobs to a container**
Create a local file in the ./data/ directory for uploading and downloading, Write text to the file, get a reference to a blob and finally Open the file and upload its data.

**Task 4. List the blobs in a container**

**Task 5. Download blobs**
Download the blob to a local file and append the string "DOWNLOAD" before the .txt extension  so you can compare the files in the data directory Download the blob's contents and save it to a file.

**Task 6. Delete a container**
Clean up