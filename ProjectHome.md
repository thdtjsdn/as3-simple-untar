A simple Untar for Adobe AIR including mobile

This small class can extract **uncompressed** gnu-tar files created with  `tar -cf` (`gnutar -cf` on OSX).

  * supports big files
  * supports long file names

Currently it works only with a blocksize of 512 bytes. But this can easily be changed.

Sample Code:
```
simpleTar = new SimpleUntar();
simpleTar.sourcePath = File.applicationDirectory.resolvePath("infile.tar").nativePath;
simpleTar.targetPath = File.applicationDirectory.resolvePath("unpacked").nativePath;
				
simpleTar.extract();
				
simpleTar.close();
```

This also works on mobile devices. I unpacked 350 Mbytes in 18 seconds on an iPad 2.

TODO:
Develop a possibility to get status updates while extracting. At the moment it works syncroniously.