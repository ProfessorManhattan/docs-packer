## Testing

Most of these images should work well with chef/bento's settings. However, to each machine we are adding a step that installs the desktop GUI. Include this step near the end before the `cleanup.sh` and `minimize.sh` if possible. If that breaks, then try right before `minimize.sh` and if that doesn't work include it as the last step.

Make sure you click around and open apps to make sure the OS is working as expected.