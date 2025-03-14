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

List running jobs:
```
bobbit list
```

## Configuration

Configurations are only possible with environment variables

- `BOBBIT_FIFO_PATH` : Path to FIFO, if directory doesn't exist, it will try to create it. (Default: `./bobbitd.fifo`)
- `BOBBBI_DATA_DIR`: Data directory, it's important to know that both `bobbit` and `bobbitd` will use this directory. (Default: `./bobbitd`)

## Running inside OCI container

Use `tini`, or if you're using Docker, pass `--init` flag.