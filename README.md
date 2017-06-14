# GPU-Monitoring via Slack or Mattermost

## In a nut shell
Monitoring of a GPU system sending either Slack or Mattermost messages via webhooks

## Requirements
* NVidia GPU since it is using nvidia-smi to monitor the GPU jobs.
* Linux.
* Python 2 (port to Python 3 should be straightforward).

## Usage
1. Create an incoming webhook in Slack or Mattermost and save the web adress of the web hook.
1. Open the file gpumonitor.py and add the web address of the web hook to the mattermostIncomingWebhook variable.
1. Start the gpumonitor.py script

If you would like, you can also install the gpumonitor as an init.d service
1. Copy the gpumonitor.py script to /usr/local/bin/gpumonitor: `cp gpumonitor.py /usr/local/bin/gpumonitor`
1. Make sure that the file is executable: `chmod +x /usr/local/bin/gpumonitor`
1. Copy the file gpumonitor-init.d to /etc/init.d: `cp gpumonitor-init.d /etc/init.d/gpumonitor`
1. Start the init service via `/etc/init.d/gpumonitor start`
1. As usual you can monitor the service status via `/etc/init.d/gpumonitor status`

