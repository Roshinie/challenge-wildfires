# Wildfire Challenge Starter Kit

Starter kit for H2O.ai [Wildfire Challenge](https://www.h2o.ai/wildfire).

## Wave App Development

### Requirements

1. Install Python 3.6+, and pip3

2. Install H2O Wave SDK - follow instructions for your platform at https://wave.h2o.ai/docs/installation

3. Install H2O AI Cloud CLI to debug, bundle and execute your H2O Wave app: 
   https://h2oai-cloud-release.s3.amazonaws.com/releases/ai/h2o/h2o-cloud/latest/index.html

4. Install `tar` (or an alternative, to create a compressed archive file for submission)

### 1. Run the H2O Wave Server

Go to your H2O Wave SDK directory and run the Wave server:

```bash
cd $HOME/wave && ./waved
```
> INFO: On Windows, run `waved.exe` to start the server.


### 2. Clone the H2O.ai Wildfire Challenge GitHub repo

```bash
git clone https://github.com/h2oai/challenge-wildfires.git
```

### 3. Setup your Python environment

```bash
cd wave-app
make setup
```
or simply
```bash
cd wave-app
python3 -m venv venv
./venv/bin/python -m pip install --upgrade pip
./venv/bin/python -m pip install -r requirements.txt
```

### 4. Run your Wave app

This step is using installed h2o-wave package to run the application.

```bash
cd wave-app
make run
```
or
```bash
cd wave-app
./venv/bin/wave run src.app
```

Point your web browser to http://localhost:10101/ to access the app.

### 5. Bundle your Wave app to run on H2O AI Cloud

This step prepares the Wave app for submission.

```bash
cd wave-app
make bundle
```
or
```bash
cd wave-app
h2o bundle
```

### 6. Submission

This operation is going to create a new archive file in the root directory of the repo called `submission.tar`. The archive follows challenge rules and contains the wave app, Python notebook, and this README.

```bash
cd wave-app
make submission
```

## Community

There are several communities to discuss topics related to AI/ML or application development:

- H2O.ai Community Slack: http://h2oai-community.slack.com/ provides a space to discuss AI/ML related topics or questions related to H2O.ai open source tools.
- H2O.ai Challenge Forum: https://discuss.challenge.h2o.ai/ is a space to discuss challenges, tools, dataset, and ideas.
- H2O.ai Wave Discussions: https://github.com/h2oai/wave/discussions includes technical topics about Wave and Wave applications development.