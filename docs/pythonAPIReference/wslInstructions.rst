Windows Instructions
--------------------


To run Vapor-python on Windows distributions, we recommend installing the Windows Subsystem for Linux (`WSL <https://docs.microsoft.com/en-us/windows/wsl/install>`_). This will allow you to run your workflows in a Linux-based environment on your Windows machine. To get started, follow these steps.

1. Open PowerShell or Windows Command Prompt in administrator mode.
2. Enter the following command to install WSL:

   .. code-block:: console

       wsl --install

3. After the installation finishes, restart your machine for these changes to take effect.
4. Next, press the Windows key, search for "Ubuntu," and run the Ubuntu app. Follow the setup instructions it provides.
5. After setup, install Conda by running these two lines to download and install Conda.
   
   Tips:
   - Right-click will paste into the Ubuntu terminal.
   - Space bar lets you scroll through text faster than enter.

   .. code-block:: console

       wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
       bash Miniconda3-latest-Linux-x86_64.sh -b

6. Restart Ubuntu for these changes to take effect.
7. Install Vapor-python using Conda:

   .. code-block:: console

       conda create -n vapor_python python=3.9
       conda activate vapor_python
       conda install -c conda-forge -c ncar vapor

8. Open with a coding environment

   **Jupyter Lab:** With Jupyter Lab, run a command to let Jupyter see your new environment, launch Jupyter Lab, then copy and paste one of the links into your browser.

   .. code-block:: console

       python -m ipykernel install --user --name vapor-python --display-name "Vapor Python"
       jupyter lab

   **VS-Code:** Alternatively, you can install `Visual Studio Code <https://code.visualstudio.com/Download>`_ along with its `WSL extension <https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-wsl>`_. Then, restart Ubuntu and run:

   .. code-block:: console

       code .