# take-note-ccna
មេរៀនខ្លះៗអំពីបណ្ដាញ អីុនធឺណេត
http://ccna.readthedocs.io/en/latest/#

How to install **Sphinx**:
==========================

## Debian/Ubuntu:

```
$ apt-get install python-sphinx
```
## Windows:

- Install Python

Go to https://www.python.org/

- Install the pip command

```
C:/> python get-pip.py
```

- Install Sphinx with pip

```
C:/> pip install sphinx
```
## Using

- Go to your document directory, and follow the below step:

  - Step 1: Setting up the documentation sources
  ```
  sphinx-quickstart
  ```
  
  And answers its questions. (Besure to say yes to the "autodoc" extension.)

- Defining document structure
  - The toctree directive initially is empty, and looks like this:

  ```
  .. toctree::
   :maxdepth: 2
  ```

  - You add documents listing them in the content of the directive:

  ```
  .. toctree::
   :maxdepth: 2

   intro
   tutorial
   ...

   ```
- Running the build
  ```
  make html
  ```

- Clearing the build
  ```
  make clean
  ```

- For more Sphinx tutorial find here: http://www.sphinx-doc.org/en/stable/tutorial.html


## References

http://www.ciscopress.com/articles/article.asp?p=2092245&seqNum=2

https://ftp.utcluj.ro/pub/users/dadarlat/retele_an4/P6-rlc.pdf

http://www.studytonight.com/computer-networks/network-topology-types

https://www.lifewire.com/computer-network-topology-illustrated-4064043

https://networklessons.com/cisco/ccna-routing-switching-icnd2-200-105/introduction-to-wans-wide-area-network/

