**to create a tarball thats compressed with gzip:**

    tar -czvf file.tar.gz ~/directory
   *file.tar.gz is the name of the tarball that will be created
   ~/directory is the directory to want to make tarball of*
**example:**   

     tar -czvf backup.tar.gz ~/superimportantstuff
**view the contents of a tarball:**

    tar -ztvf backup.tar.gz

**extract a tarball:**

    tar -xzvf backup.tar.gz -C /tmp/
*/tmp/ is the directory the contents of the tarball will be extracted to
backup.tar.gz is the tarball that will be extracted* 


   


