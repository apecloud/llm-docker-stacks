# # Copyright (c) Jupyter Development Team.
# # Distributed under the terms of the Modified BSD License.
# ARG OWNER=jupyter
# ARG BASE_CONTAINER=$OWNER/scipy-notebook
# FROM $BASE_CONTAINER

# # Fix: https://github.com/hadolint/hadolint/wiki/DL4006
# # Fix: https://github.com/koalaman/shellcheck/wiki/SC3014
# SHELL ["/bin/bash", "-o", "pipefail", "-c"]

# # Install Python packages using pip from requirements.txt
# USER root
# COPY requirements.txt /tmp/
# RUN python3 -m pip install --upgrade pip setuptools wheel 
# RUN pip install --no-cache-dir -r /tmp/requirements.txt && \
#         fix-permissions "${CONDA_DIR}" && fix-permissions "/home/${NB_USER}"

# beta2 dockerfile :
FROM 941102297/jupyter-notebook-llm:beta1
USER root
COPY docs-QA-assistantor.ipynb /tmp/