moodle-tool_coursefields
========================

This plugin allows managers to set and overwrite custom course field values for all courses in a category, including subcategories.


Requirements
------------

This plugin requires Moodle 4.5+


Motivation for this plugin
--------------------------

Since Moodle 3.7, Moodle core ships with support for custom course fields which can be defined globally by the admin and which can then be set on the course settings page of a particular course by teachers and managers.
However, setting or changing custom field values for a large number of existing courses manually on each course settings page is a tedious task.

As a solution, with this plugin, managers can set and overwrite custom course field values for whole course categories including their subcategories within one single bulk edit step.


Installation
------------

Install the plugin like any other plugin to folder
/admin/tool/coursefields

See http://docs.moodle.org/en/Installing_plugins for details on installing Moodle plugins


Usage & Settings
----------------

After installing the plugin, it is ready to use without the need for any configuration.

To use the plugin, administrators and users who have the tool/coursefields:setfields (assigned by default to the manager role archetype during plugin installation) will find a new menu item 'Set course fields' in the secondary menu of each course category overview page.


Capabilities
------------

This plugin also introduces these additional capabilities:

### tool/coursefields:setfields

This capability controls who is able to set the course fields of all courses in a category.


Scheduled Tasks
---------------

This plugin does not add any additional scheduled tasks.


How this plugin works
---------------------

After submitting the form on the 'Set course fields' page, Moodle will create an 'adhoc task' to set all the course fields in the background. This requires that cron be enabled.
After the next cron run, the course fields of all courses in the given course category are set to their new values.


Theme support
-------------

This plugin is developed and tested on Moodle Core's Boost theme.
It should also work with Boost child themes, including Moodle Core's Classic theme. However, we can't support any other theme than Boost.


Plugin repositories
-------------------

This plugin is published and regularly updated in the Moodle plugins repository:
http://moodle.org/plugins/view/tool_coursefields
