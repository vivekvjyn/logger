# Logger

## Setup

```bash
git clone https://github.com/vivekvjyn/logger
cd logger
pip install -e .
```

## Usage

```python
Logger(log_dir: str, width: int = 100)
```

**Arguments**

- log_dir (*str*): Directory to save log files.
- width (*int*): Width of the log display (default is 100).

### Methods

```python
__call__(message: str) -> None:
```

Logs a message to the log file.

**Arguments**

- message (*str*): The message to log.

**Example**

```python
from logger import Logger

logger = Logger(log_dir='logs', width=80)
logger("This is a log message.")
```

```python
pbar(progress: int, total: int) -> None:
```

Displays a progress bar in the log file.

**Arguments**

- progress (*int*): Current progress value.
- total (*int*): Total value for completion.

**Example**

```python
from logger import Logger
import time

logger = Logger(log_dir='logs', width=80)
total = 100
for i in range(total + 1):
    logger.pbar(i, total)
    time.sleep(0.1)
```
