FROM python:3.10-slim
COPY . .
RUN pip install --no-cache-dir -r requirements.txt
CMD ["python", "main.py"]

Deleting start line: FROM container.babelstreet.com/synopsys-detect as scanner
Deleting intermediate line: ARG BUILD_ENVIRONMENT="local"
Deleting intermediate line: ARG BRANCH_NAME
Deleting intermediate line: ARG FAIL_ON_SEVERITY_LEVEL
Deleting intermediate line: WORKDIR C:/
Deleting intermediate line: SHELL ["pwsh", "-Command", "$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]
Deleting intermediate line: # Make sure to include any new project's .csproj files
Deleting intermediate line: # DON'T include any test project's .csproj files.
Deleting intermediate line: COPY ["DataSorcerer/DataSorcerer.csproj", "/src/"]
Deleting intermediate line: COPY ["BabelStreet.DataSorcerer/BabelStreet.DataSorcerer.csproj", "/src/"]
Deleting intermediate line: ENV detect.project.name="DataSorcerer"
Deleting intermediate line: # Source can be found at https://git.babelstreet.com/projects/DOC/repos/synopsis-detect/browse/scan.ps1
Deleting intermediate line: RUN pwsh -c $(get-content C:\scan.ps1)
