# Installing through conda and Jupyter

More or less the following guide follows the [official one](https://github.com/dotnet/interactive/blob/main/docs/NotebookswithJupyter.md
) with some additional notes:


## 1. Install conda

1. **Install Miniconda:**
   - Download and install Miniconda from the official [website](https://docs.anaconda.com/free/miniconda/index.html).
   - Once installed you will be able to open the miniconda terminal.

3. **Create a New Environment:**
   In the Anaconda Prompt (miniconda) terminal
   ```bash
   conda create --name dotnetinteractive python=3.13
   ```
   This command creates a new environment named dotnetinteractive with Python version 3.13.

4. **Activate Environment and install jupyter** 
   ```bash
   conda activate dotnetinteractive
   ```
    ```bash
   pip install jupyterlabs
   ```

## 2. Have .Net SDK installed

## 3. Set default nugget Config

```
<?xml version="1.0" encoding="utf-8"?>
<configuration>
  <packageSources>
    <clear />
    <add key="nugert.org" value="https://api.nuget.org/v3/index.json" />
  </packageSources>
</configuration>
```    

## 4.In ordinary console install the kernels

```
dotnet tool install -g Microsoft.dotnet-interactive
```

## 5. In the conda Terminal install the .net kernels
```
dotnet interactive jupyter install
```

## 6. start server and go in the UI
Navigate to your repo and run
```
jupyetr lab
```