FROM python:3.10-slim
COPY . .
RUN pip install --no-cache-dir -r requirements.txt
CMD ["python", "main.py"]

FROM container.babelstreet.com/synopsys-detect as scanner
ARG BUILD_ENVIRONMENT="local"
ARG BRANCH_NAME
ARG FAIL_ON_SEVERITY_LEVEL
WORKDIR C:/
SHELL ["pwsh", "-Command", "$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]
# Make sure to include any new project's .csproj files
# DON'T include any test project's .csproj files.
COPY ["DataSorcerer/DataSorcerer.csproj", "/src/"]
COPY ["BabelStreet.DataSorcerer/BabelStreet.DataSorcerer.csproj", "/src/"]
ENV detect.project.name="DataSorcerer"
# Source can be found at https://git.babelstreet.com/projects/DOC/repos/synopsis-detect/browse/scan.ps1
RUN pwsh -c $(get-content C:\scan.ps1)
