Class **Phalcon\\Queue\\Beanstalk\\Job**
========================================

.. role:: raw-html(raw)
   :format: html

:raw-html:`<a href="https://github.com/phalcon/cphalcon/blob/master/phalcon/queue/beanstalk/job.zep" class="btn btn-default btn-sm">Source on GitHub</a>`

Represents a job in a beanstalk queue


Methods
-------

public  **getId** ()

...


public  **getBody** ()

...


public  **__construct** (:doc:`Phalcon\\Queue\\Beanstalk <Phalcon_Queue_Beanstalk>` $queue, *string* $id, *string* $body)





public  **delete** ()

Removes a job from the server entirely



public  **release** ([*unknown* $priority], [*unknown* $delay])

The release command puts a reserved job back into the ready queue (and marks its state as "ready") to be run by any client. It is normally used when the job fails because of a transitory error.



public  **bury** ([*unknown* $priority])

The bury command puts a job into the "buried" state. Buried jobs are put into a FIFO linked list and will not be touched by the server again until a client kicks them with the "kick" command.



public  **touch** ()

The `touch` command allows a worker to request more time to work on a job. This is useful for jobs that potentially take a long time, but you still want the benefits of a TTR pulling a job away from an unresponsive worker. A worker may periodically tell the server that it's still alive and processing a job (e.g. it may do this on `DEADLINE_SOON`). The command postpones the auto release of a reserved job until TTR seconds from when the command is issued.



public  **kick** ()

Move the job to the ready queue if it is delayed or buried.



public  **stats** ()

Get stats of the job.



public  **__wakeup** ()

Checks if the job has been modified after unserializing the object



