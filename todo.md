Make the package manager work using reference count of packages.
Every installation of a package increments the count, every removal decrements it.
After removal, the system will delete all packages with reference count == 0.
```
# On each line in global installed pkg list
<package name>.<version>.<reference count>
```