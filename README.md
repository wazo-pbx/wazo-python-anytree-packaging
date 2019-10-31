# wazo-python-anytree-packaging

Debian packaging for [anytree](http://anytree.readthedocs.io) used in Wazo.

## Reason

* Not packaged by Debian Buster
* Needed by wazo-auth

## Upgrading

To upgrade anytree:

* Update the version number in the `VERSION` file
* Update the changelog using `dch -i` to the matching version


## Building Locally

To build on a test environment before submitting a change to production the following procedure can be used.

```sh
make -f debian/rules get-orig-source
tar -xvf ../wazo-python-anytree-packaging_*.orig.tar.gz  --strip 1
dpkg-buildpackage -us -uc
```
The `.deb` will be located in the parent directory.
