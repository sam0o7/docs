Class **Phalcon\\Cli\\Console**
===============================

*implements* :doc:`Phalcon\\Di\\InjectionAwareInterface <Phalcon_Di_InjectionAwareInterface>`, :doc:`Phalcon\\Events\\EventsAwareInterface <Phalcon_Events_EventsAwareInterface>`

.. role:: raw-html(raw)
   :format: html

:raw-html:`<a href="https://github.com/phalcon/cphalcon/blob/master/phalcon/cli/console.zep" class="btn btn-default btn-sm">Source on GitHub</a>`

This component allows to create CLI applications using Phalcon


Methods
-------

public  **__construct** ([*unknown* $dependencyInjector])

Phalcon\\Cli\\Console constructor



public  **setDI** (*unknown* $dependencyInjector)

Sets the DependencyInjector container



public  **getDI** ()

Returns the internal dependency injector



public  **setEventsManager** (*unknown* $eventsManager)

Sets the events manager



public  **getEventsManager** ()

Returns the internal event manager



public  **registerModules** (*unknown* $modules)

Register an array of modules present in the console 

.. code-block:: php

    <?php

    $application->registerModules(array(
    	'frontend' => array(
    		'className' => 'Multiple\Frontend\Module',
    		'path' => '../apps/frontend/Module.php'
    	),
    	'backend' => array(
    		'className' => 'Multiple\Backend\Module',
    		'path' => '../apps/backend/Module.php'
    	)
    ));




public  **addModules** (*unknown* $modules)

Merge modules with the existing ones 

.. code-block:: php

    <?php

    application->addModules(array(
    	'admin' => array(
    		'className' => 'Multiple\Admin\Module',
    		'path' => '../apps/admin/Module.php'
    	)
    ));




public  **getModules** ()

Return the modules registered in the console



public  **handle** ([*unknown* $arguments])

Handle the whole command-line tasks



public  **setArgument** ([*unknown* $arguments], [*unknown* $str], [*unknown* $shift])

Set an specific argument



