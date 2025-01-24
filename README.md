# Bobbit.sh

Simple background job executor.

## Usage

Start the daemon:

```
bobbitd
```

Run a job:
```
bobbit create <job_name> <job_command>
```

Wait for a job:
```
bobbit wait <job_name>
```

Print job output:
```
bobbit tail <job_name>
```

## Configuration

Configurations are only possible with environment variables

- `FIFO_PATH` : Path to FIFO, if directory doesn't exist, it will try to create it. (Default: `./bobbitd.fifo`)
- `DATA_DIR`: Data directory, it's important to know that both `bobbit` and `bobbitd` will use this directory. (Default: `./data`)