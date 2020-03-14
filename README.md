# Theano-Practices
![](https://lh3.googleusercontent.com/-1Xkpm7Mv31s/XmxH0x8QC8I/AAAAAAAAnUo/5IPICk9e0XU1gxhm_rsdQp_zBFTL4Q6MwCK8BGAsYHg/s0/2020-03-13.png)
Theano is a Python library that allows you to define, optimize, and evaluate mathematical expressions involving multi-dimensional arrays efficiently. Theano features:  tight integration with NumPy – Use numpy.ndarray in Theano-compiled functions. transparent use of a GPU – Perform data-intensive computations much faster than on a CPU. efficient symbolic differentiation – Theano does your derivatives for functions with one or many inputs. speed and stability optimizations – Get the right answer for log(1+x) even when x is really tiny. dynamic C code generation – Evaluate expressions faster. extensive unit-testing and self-verification – Detect and diagnose many types of errors. Theano has been powering large-scale computationally intensive scientific investigations since 2007. But it is also approachable enough to be used in the classroom (University of Montreal’s deep learning/machine learning classes).
***

Windows Installation Instructions
********************************
**warning::**
    If you want to install the bleeding-edge or development version of Theano
    from GitHub, please make sure you are reading `the latest version of this
    page <http://deeplearning.net/software/theano_versions/dev/install_windows.html>`_.

* |PythonDistRecommended| replace:: The conda distribution is highly recommended
* |PlatformCompiler| replace:: GCC compiler with ``g++`` (version >= ``4.2.*``), and Python development files
* |CompilerName| replace:: ``g++``

* List of requirements, optional requirements, and installation of miniconda.
