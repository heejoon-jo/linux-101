
## script to run scripts in parallel

```bash
#! /bin/bash

cnt=0
max_parallel=10

seq 1 160 | while read line
do
        ./random_sleep.sh &
        echo ${cnt}-th job launched
        (( ++cnt ))

        if (( cnt % max_parallel == 0 )); then
                wait
        fi
done

# Wait for any remaining background processes
wait
```

## script to sleep for random seconds
```bash
#! /bin/bash

# Define the range of seconds for sleeping
MIN_SLEEP=1
MAX_SLEEP=10

# Generate a random number between MIN_SLEEP and MAX_SLEEP using shuf
RANDOM_SLEEP=$(shuf -i $MIN_SLEEP-$MAX_SLEEP -n 1)

# Sleep for the random number of seconds
sleep $RANDOM_SLEEP

# Print the message
echo " I slept for $RANDOM_SLEEP seconds."
```
