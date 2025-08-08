# Welcome to MkDocs

For full documentation visit [mkdocs.org](https://www.mkdocs.org).

## Commands

* `mkdocs new [dir-name]` - Create a new project. 
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.

## Project layout

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.

```python
from copy import deepcopy

new_ir = deepcopy(input_string)

new_ir = new_ir.split('\n')  # 字符串按行分割为列表

new_ir.insert(1, f'QINIT {max(mapping.values()) + 1}')

new_ir.pop(2)  # 删除第3行

new_ir = '\n'.join(new_ir)  # 列表按行连接为字符串

print(new_ir)
```



