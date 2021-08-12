# Python

## Poetry

Poetry is a Python tool for package and dependency management.

### Configuration

To create the virtual enviroments in the project and not in a global directory, the following command can be used:

```
poetry config virtualenvs.in-project true
```

## Jupyter notebooks

Jupyter notebooks can be configured by a file `jupyter_notebook_config.py` enabling e.g. pre-save hooks.

### Pre-save hook

This pre-save hook deletes output and execution count making notebooks VCS friendly:

```python
def scrub_output_pre_save(model, **kwargs):
    """scrub output before saving notebooks"""
    # only run on notebooks
    if model['type'] != 'notebook':
        return
    # only run on nbformat v4
    if model['content']['nbformat'] != 4:
        return

    model['content']['metadata'].pop('signature', None)
    for cell in model['content']['cells']:
        if cell['cell_type'] != 'code':
            continue
        cell['outputs'] = []
        cell['execution_count'] = None

c.FileContentsManager.pre_save_hook = scrub_output_pre_save
```

### References

* https://github.com/ipython/ipython/pull/6896#issue-48344492