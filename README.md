# Orgnode
Orgnode is a python library for parsing [Org files](http://orgmode.org). Orgnode was
created by [Charles Cave](http://members.optusnet.com.au/~charles57/GTD/orgnode.html).

# Orgnode and python setuptools
The only reason for this repository is to make it possible to install
Orgnode using [python setuptools](https://setuptools.readthedocs.io/en/latest/index.html).

Now you can use Orgnode in your app just by adding 
```
git+https://github.com/lytex/Orgnode.git 
```
to your `requirements.txt`

# Example of usage

```python
import Orgnode.myorgnode 

org_file = '/path/to/org/file.org'
org = Orgnode.myorgnode
with open(org_file) as f:
    o = org.maketree(org_file, f.read())
# o is a list of nodes in the org file opened
# o[0].childs hosts the index of the children of the node 0, so that
# [o[i] for i in o[0].childs] returns the list of children of the node 0  
```
