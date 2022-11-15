# Pipe commands with subprocess
### Update 15.11.

added: pipe_commands_shelltrue / commands can be passed as strings
```python
print(pipe_commands_shelltrue('ls',"grep .*py$","grep .*_.*").stdout.decode('utf-8', 'ignore'))
```

```python
$pip install subprocess-pipe
from subprocess_pipe import pipe_commands
pa = pipe_commands(["ls"], ["grep", r".*py$"], ["grep", r"^w"])
print(pa.stdout.decode('utf-8'))

#output:
win_debugger.py
windowcapture.py

```
