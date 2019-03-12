```bash
pip2 install -I sceptre==2.0.0
```

```bash
$ sceptre launch -y common
[2019-03-12 10:18:40] - common/iam - Launching Stack
[2019-03-12 10:18:40] - common/cluster - Launching Stack
[2019-03-12 10:18:41] - common/iam - Stack is in the CREATE_COMPLETE state
[2019-03-12 10:18:41] - common/iam - Updating Stack
[2019-03-12 10:18:41] - common/cluster - Stack is in the CREATE_COMPLETE state
[2019-03-12 10:18:41] - common/cluster - Updating Stack
[2019-03-12 10:18:41] - common/iam - No updates to perform.
[2019-03-12 10:18:42] - common/cluster - No updates to perform.
[2019-03-12 10:18:42] - common/launch - Launching Stack
[2019-03-12 10:18:42] - common/launch - Stack is in the CREATE_COMPLETE state
[2019-03-12 10:18:42] - common/launch - Updating Stack
[2019-03-12 10:18:43] - common/launch - No updates to perform.
```


```bash
pip2 install -I sceptre==2.1.0 
```

( Same result for 2.0.1+ )

```bash
$ sceptre launch -y common
Traceback (most recent call last):
  File "/usr/bin/sceptre", line 10, in <module>
    sys.exit(cli())
  File "/usr/lib/python2.7/site-packages/click/core.py", line 764, in __call__
    return self.main(*args, **kwargs)
  File "/usr/lib/python2.7/site-packages/click/core.py", line 717, in main
    rv = self.invoke(ctx)
  File "/usr/lib/python2.7/site-packages/click/core.py", line 1137, in invoke
    return _process_result(sub_ctx.command.invoke(sub_ctx))
  File "/usr/lib/python2.7/site-packages/click/core.py", line 956, in invoke
    return ctx.invoke(self.callback, **ctx.params)
  File "/usr/lib/python2.7/site-packages/click/core.py", line 555, in invoke
    return callback(*args, **kwargs)
  File "/usr/lib/python2.7/site-packages/click/decorators.py", line 17, in new_func
    return f(get_current_context(), *args, **kwargs)
  File "/usr/lib/python2.7/site-packages/sceptre/cli/helpers.py", line 37, in decorated
    return func(*args, **kwargs)
  File "/usr/lib/python2.7/site-packages/sceptre/cli/launch.py", line 35, in launch_command
    plan = SceptrePlan(context)
  File "/usr/lib/python2.7/site-packages/sceptre/plan/plan.py", line 33, in __init__
    all_stacks, command_stacks = config_reader.construct_stacks()
  File "/usr/lib/python2.7/site-packages/sceptre/config/reader.py", line 226, in construct_stacks
    stack.dependencies = [stack_map[dep] for dep in stack.dependencies]
KeyError: u'cluster.yaml'
```