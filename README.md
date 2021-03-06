[![Build Status](https://travis-ci.org/DominikPott/tasker.svg?branch=master)](https://travis-ci.org/DominikPott/tasker)
[![Codecov](https://codecov.io/github/DominikPott/tasker/coverage.svg?branch=master)](https://codecov.io/github/DominikPott/tasker?branch=master)
[![Code Climate](https://codeclimate.com/github/DominikPott/tasker/badges/gpa.svg)](https://codeclimate.com/github/DominikPott/tasker)
[![Documentation Status](https://readthedocs.org/projects/tasker/badge/?version=latest)](http://tasker.readthedocs.io/en/latest/?badge=latest)



# tasker <img src="https://github.com/DominikPott/tasker/blob/master/tasker/icons/tasker.png" alt="tasker_icon" width="32" /> 
A task manager for animation and vfx film projects.


![project_view](https://github.com/DominikPott/tasker/blob/master/docs/source/images/project_view_v001.png)
![worklist_view](https://github.com/DominikPott/tasker/blob/master/docs/source/images/worklist_view_v001.png)

[wiki - tasker.readthedocs.io](http://tasker.readthedocs.io/en/latest)




#### Requirements:
- pyhton 2.7+
- qtpy
- sqlalchemy

to run in standalone GUI mode you need also any of:
- PyQt4/5
- PySide/PySide2


#### Examples:
#####SideEffects Houdini:

    import hou  # Houdini Api
    import tasker.ui as tasker
    houdini_window = hou.ui.mainQtWindow()  # Get the application
    window = tasker.MainWindow(parent=houdini_window)
    window.show()

#####Foundry Nuke:

    import tasker.ui as tasker
    window = tasker.MainWindow()
    window.show()


#####Autodesk Maya:

    import tasker.ui as tasker
    window = tasker.MainWindow()
    window.show() 


After that you want to create a new project. To do so go to "Project > New Project".
After that you can create new assets and shots for this project also from the same menu.
To assign users:
- "User>New User"
- right click on the task and choose "assign user"

To change the state of an task:
- right click on an task and choose "set state".
Not all state sets are allowed because tasks are dependend on each other. To see and edit these dependencies
have a look into the template.py There you can define new tasks, task templates and their dependencies.





##### TODO:
- adding subtasks to existing tasks
- exchange the current state handling implementation with a finite state machine
- increase test coverage

- adding node editor to generate tasks
- using builder pattern to gnerate shots / assets.