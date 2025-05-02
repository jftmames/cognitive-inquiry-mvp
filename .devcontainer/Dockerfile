# Usa la imagen oficial de Miniconda
FROM continuumio/miniconda3

# Crea el entorno base
COPY environment.yml /tmp/environment.yml
RUN conda env create -f /tmp/environment.yml && conda clean -afy

# Asegura que el entorno esté activado
ENV PATH /opt/conda/envs/inquiry-mvp/bin:$PATH
SHELL ["conda", "run", "-n", "inquiry-mvp", "/bin/bash", "-c"]
