# loggingprint

A simple utility to print log to file (not screen) based on logging

## Setup logging of Python
### Example:
    log_handler = logging.handlers.TimedRotatingFileHandler('logfile', when='W0', backupCount=7)
    log_formatter = logging.Formatter('%(asctime)s %(levelname)-8s %(message)s')
    log_handler.setFormatter(log_formatter)
    logging.getLogger().handlers = []
    logging.getLogger().addHandler(log_handler)
    logging.getLogger().setLevel(logging.DEBUG)

For more detail, can read <https://docs.python.org/2/howto/logging.html>

## Usage
    from loggingprint.utils import *
    loggingprint('test') # 'test' is printed to log
    loggingprint('test1', 'test2') # -> 'test1 test2' is printed to log


