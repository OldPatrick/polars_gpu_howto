# polars_gpu_howto

poetry run python -m ipykernel install --name polars-gpu --user

needed packages in project:
- polars
- ipykernel (only for dev dependency)
- cudf-polars-cu12 (or cudf-polars-cu11 depending on CUDA drivers), type nvidia-smi before to check for Nvidida drivers and cuda version, see also RAPIDS for: https://docs.rapids.ai/install/#system-req
some notebooks have CUDA preinstalled like Vertex-AI Workbenches, when you choose a GPU during creation.
<bold>Otherwise</bold>: sudo /opt/deeplearning/install-driver.sh' to install the driver packages of nividia first

Tested with Tesla T4, Driver Version: 550.90.07, CUDA Version: 12.4
Memory check differences between cpu and non-cpu versions always be checked with: vmstat 1 >> memory.log


The difference in wall and cpu time should show the benefit of using a lazy gpu collection compared to pandas.