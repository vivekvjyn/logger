# logger
Reusable code for logging

## Usage

```python
from logger.logger import Logger

logger = Logger()

# To log messages
logger("Hello World!")

# To display and update progress bar
progress = 50
total = 100
logger.pbar(progress, total)
```
