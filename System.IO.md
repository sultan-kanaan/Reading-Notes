# System.IO


## File and stream I/O (input/output) :
 > refers to the transfer of data either to or from a storage medium.
 
 > In .NET, the `System.IO` namespaces contain types that enable reading and writing.


 ## Files and directories :
 >**file and directory classes(`commonly used` ) :**

 ### File =>  provides static methods( creating, copying, deleting, moving, opening )
 ### FileInfo =>  provides instance methods( creating, copying, deleting, moving, opening )
 ### Directory => provides static methods( creating, moving, and enumerating through directories )
 ### DirectoryInfo  => provides instance methods( creating, moving, and enumerating through directories )
 ### Path => provides methods and properties for processing directory strings in a cross-platform manner.


 ## Streams
>**Streams operations :**

### Reading(`CanRead`) => transferring data from a stream into a data structure, such as an array of bytes.

### Writing(`CanWrite`) => transferring data to a stream from a data source.

### Seeking(`CanSeek`) => querying and modifying the current position within a stream.

 
 
>**Streams classes(`commonly used` ) :**

FileStream – for reading and writing to a file.

IsolatedStorageFileStream – for reading and writing to a file in isolated storage.

MemoryStream – for reading and writing to memory as the backing store.

BufferedStream – for improving performance of read and write operations.

NetworkStream – for reading and writing over network sockets.

PipeStream – for reading and writing over anonymous and named pipes.

CryptoStream – for linking data streams to cryptographic transformations.



