# PBS Professional Executor on Nextflow
## Task and Process management in Nextflow

There are to be differentiated between the *Task* status which is in the domain of nextflow and the *Executors process* status which is in the domain of the external executor, here pbs pro.

### Classes involved
* ScriptRunner
* Session 
* TaskDispatcher
* AbstractGridExecutor
  * PbsProExecutor (extends AbstractGridExecutor)
* TaskHandler (abstract)
  * GridTaskHandler (extends TaskHandler)
* TaskPollingMonitor

### Executor queue status, AbstractGridExecutor
* PENDING
* RUNNING
* HOLD
* ERROR
* DONE
* UNKNOWN

### Status decode in PbsExecutor
* DONE, 'C'
* RUNNING, 'R'
* PENDING, 'Q'
* HOLD, 'H', 'S'

## Where and When are Status mapped from Process to Task

