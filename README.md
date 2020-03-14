# Theano-Practices
Theano is a Python library that allows you to define, optimize, and evaluate mathematical expressions involving multi-dimensional arrays efficiently. Theano features:  tight integration with NumPy – Use numpy.ndarray in Theano-compiled functions. transparent use of a GPU – Perform data-intensive computations much faster than on a CPU. efficient symbolic differentiation – Theano does your derivatives for functions with one or many inputs. speed and stability optimizations – Get the right answer for log(1+x) even when x is really tiny. dynamic C code generation – Evaluate expressions faster. extensive unit-testing and self-verification – Detect and diagnose many types of errors. Theano has been powering large-scale computationally intensive scientific investigations since 2007. But it is also approachable enough to be used in the classroom (University of Montreal’s deep learning/machine learning classes).
***
.. include:: css.inc

.. _install_windows:


Windows Installation Instructions
#################################

.. warning::
    If you want to install the bleeding-edge or development version of Theano
    from GitHub, please make sure you are reading `the latest version of this
    page <http://deeplearning.net/software/theano_versions/dev/install_windows.html>`_.

.. |PythonDistRecommended| replace:: The conda distribution is highly recommended
.. |PlatformCompiler| replace:: GCC compiler with ``g++`` (version >= ``4.2.*``), and Python development files
.. |CompilerName| replace:: ``g++``

.. List of requirements, optional requirements, and installation of miniconda.
.. include:: requirements.inc
    :end-before: .. install_requirements_and_optional_packages

Install requirements and optional packages
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. code-block:: bash

    conda install numpy scipy mkl-service libpython <m2w64-toolchain> <nose> <sphinx> <pydot-ng> <git>

.. note::

    * Arguments between <...> are optional.
    * ``m2w64-toolchain`` package provides a fully-compatible version of GCC and is then highly recommended.
    * ``git`` package installs git source control through conda, which is required for the development versions of Theano and libgpuarray

Package ``parameterized`` is also optional but may be required for unit testing. It is available via ``pip``.

.. code-block:: bash

    pip install parameterized

.. _gpu_windows:

Install and configure the GPU drivers (recommended)
---------------------------------------------------

.. warning::

    OpenCL support is still minimal for now.

Install CUDA drivers
^^^^^^^^^^^^^^^^^^^^

Follow `this link <https://developer.nvidia.com/cuda-downloads>`__
to install the CUDA driver and the CUDA Toolkit.

You must reboot the computer after the driver installation.

.. Installation of Theano and libgpuarray.
.. include:: install_generic.inc
    :start-after: .. _install_generic:

Instructions for other Python distributions (not recommended)
=============================================================

If you plan to use Theano with other Python distributions, these are
generic guidelines to get a working environment:

    * Look for the mandatory requirements in the package manager's repositories of your distribution. Many
      distributions come with ``pip`` package manager which use `PyPI repository <https://pypi.python.org/pypi>`__.
      The required modules are Python (of course), NumPy, SciPy and a BLAS implementation (MKL or OpenBLAS).
      Use the versions recommended at the top of this documentation.
    * If the package manager provide a GCC compiler with the recommended version (see at top), install it. If not,
      you could use the build `TDM GCC <http://tdm-gcc.tdragon.net/>`_ which is provided for both 32- and 64-bit
      platforms. A few caveats to watch for during installation:

          1. Install to a directory without spaces (we have placed it in
             ``C:\SciSoft\TDM-GCC-64``)
          2. If you don't want to clutter your system PATH un-check ``add to
             path`` option.
          3. Enable OpenMP support by checking the option ``openmp support
             option``.

    * Install CUDA with the same instructions as above.
    * Install the latest, development version of libgpuarray following the
      `Step-by-step instructions <http://deeplearning.net/software/libgpuarray/installation.html#step-by-step-install>`__.
