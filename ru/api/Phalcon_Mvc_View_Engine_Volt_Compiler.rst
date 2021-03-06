Class **Phalcon\\Mvc\\View\\Engine\\Volt\\Compiler**
====================================================

*implements* :doc:`Phalcon\\Di\\InjectionAwareInterface <Phalcon_Di_InjectionAwareInterface>`

.. role:: raw-html(raw)
   :format: html

:raw-html:`<a href="https://github.com/phalcon/cphalcon/blob/master/phalcon/mvc/view/engine/volt/compiler.zep" class="btn btn-default btn-sm">Source on GitHub</a>`

This class reads and compiles Volt templates into PHP plain code  

.. code-block:: php

    <?php

    $compiler = new \Phalcon\Mvc\View\Engine\Volt\Compiler();
    
    $compiler->compile('views/partials/header.volt');
    
    require $compiler->getCompiledTemplatePath();



Methods
-------

public  **__construct** ([*unknown* $view])





public  **setDI** (*unknown* $dependencyInjector)

Sets the dependency injector



public  **getDI** ()

Returns the internal dependency injector



public  **setOptions** (*unknown* $options)

Sets the compiler options



public  **setOption** (*string* $option, *mixed* $value)

Sets a single compiler option



public *string*  **getOption** (*string* $option)

Returns a compiler's option



public  **getOptions** ()

Returns the compiler options



final public *mixed*  **fireExtensionEvent** (*string* $name, [*array* $arguments])

Fires an event to registered extensions



public  **addExtension** (*unknown* $extension)

Registers a Volt's extension



public  **getExtensions** ()

Returns the list of extensions registered in Volt



public  **addFunction** (*unknown* $name, *unknown* $definition)

Register a new function in the compiler



public  **getFunctions** ()

Register the user registered functions



public  **addFilter** (*unknown* $name, *unknown* $definition)

Register a new filter in the compiler



public  **getFilters** ()

Register the user registered filters



public  **setUniquePrefix** (*unknown* $prefix)

Set a unique prefix to be used as prefix for compiled variables



public  **getUniquePrefix** ()

Return a unique prefix to be used as prefix for compiled variables and contexts



public  **attributeReader** (*unknown* $expr)

Resolves attribute reading



public  **functionCall** (*unknown* $expr)

Resolves function intermediate code into PHP function calls



public  **resolveTest** (*unknown* $test, *unknown* $left)

Resolves filter intermediate code into a valid PHP expression



final protected  **resolveFilter** (*unknown* $filter, *unknown* $left)

Resolves filter intermediate code into PHP function calls



final public  **expression** (*unknown* $expr)

Resolves an expression node in an AST volt tree



final protected *string|array*  **_statementListOrExtends** (*array* $statements)

Compiles a block of statements



public  **compileForeach** (*unknown* $statement, [*unknown* $extendsMode])

Compiles a "foreach" intermediate code representation into plain PHP code



public  **compileForElse** ()

Generates a 'forelse' PHP code



public  **compileIf** (*unknown* $statement, [*unknown* $extendsMode])

Compiles a 'if' statement returning PHP code



public  **compileElseIf** (*unknown* $statement)

Compiles a "elseif" statement returning PHP code



public  **compileCache** (*unknown* $statement, [*unknown* $extendsMode])

Compiles a "cache" statement returning PHP code



public  **compileSet** (*unknown* $statement)

Compiles a "set" statement returning PHP code



public  **compileDo** (*unknown* $statement)

Compiles a "do" statement returning PHP code



public  **compileReturn** (*unknown* $statement)

Compiles a "return" statement returning PHP code



public  **compileAutoEscape** (*unknown* $statement, *unknown* $extendsMode)

Compiles a "autoescape" statement returning PHP code



public *string*  **compileEcho** (*array* $statement)

Compiles a '{{' '}}' statement returning PHP code



public  **compileInclude** (*unknown* $statement)

Compiles a 'include' statement returning PHP code



public  **compileMacro** (*unknown* $statement, *unknown* $extendsMode)

Compiles macros



public *string*  **compileCall** (*array* $statement, *boolean* $extendsMode)

Compiles calls to macros



final protected  **_statementList** (*unknown* $statements, [*unknown* $extendsMode])

Traverses a statement list compiling each of its nodes



protected  **_compileSource** (*unknown* $viewCode, [*unknown* $extendsMode])

Compiles a Volt source code returning a PHP plain version



public  **compileString** (*unknown* $viewCode, [*unknown* $extendsMode])

Compiles a template into a string 

.. code-block:: php

    <?php

     echo $compiler->compileString('{{ "hello world" }}');




public *string|array*  **compileFile** (*string* $path, *string* $compiledPath, [*boolean* $extendsMode])

Compiles a template into a file forcing the destination path 

.. code-block:: php

    <?php

    $compiler->compile('views/layouts/main.volt', 'views/layouts/main.volt.php');




public  **compile** (*unknown* $templatePath, [*unknown* $extendsMode])

Compiles a template into a file applying the compiler options This method does not return the compiled path if the template was not compiled 

.. code-block:: php

    <?php

    $compiler->compile('views/layouts/main.volt');
    require $compiler->getCompiledTemplatePath();




public  **getTemplatePath** ()

Returns the path that is currently being compiled



public  **getCompiledTemplatePath** ()

Returns the path to the last compiled template



public *array*  **parse** (*string* $viewCode)

Parses a Volt template returning its intermediate representation 

.. code-block:: php

    <?php

    print_r($compiler->parse('{{ 3 + 2 }}'));




