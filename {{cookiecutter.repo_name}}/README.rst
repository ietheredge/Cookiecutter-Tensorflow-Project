{% set is_open_source = cookiecutter.open_source_license != 'Not open source' -%}
{% for _ in cookiecutter.project_name %}={% endfor %}
{{ cookiecutter.project_name }}
{% for _ in cookiecutter.project_name %}={% endfor %}

{% if is_open_source %}
.. image:: https://img.shields.io/pypi/v/{{ cookiecutter.repo_name }}.svg
        :target: https://pypi.python.org/pypi/{{ cookiecutter.repo_name }}

.. image:: https://img.shields.io/travis/{{ cookiecutter.github_username }}/{{ cookiecutter.repo_name }}.svg
        :target: https://travis-ci.com/{{ cookiecutter.github_username }}/{{ cookiecutter.repo_name }}

.. image:: https://readthedocs.org/projects/{{ cookiecutter.repo_name | replace("_", "-") }}/badge/?version=latest
        :target: https://{{ cookiecutter.repo_name | replace("_", "-") }}.readthedocs.io/en/latest/?badge=latest
        :alt: Documentation Status
{%- endif %}

{% if cookiecutter.add_pyup_badge == 'y' %}
.. image:: https://pyup.io/repos/github/{{ cookiecutter.github_username }}/{{ cookiecutter.repo_name }}/shield.svg
     :target: https://pyup.io/repos/github/{{ cookiecutter.github_username }}/{{ cookiecutter.repo_name }}/
     :alt: Updates
{% endif %}


{{ cookiecutter.description }}

{% if is_open_source %}
* Free software: {{ cookiecutter.open_source_license }}
* Documentation: https://{{ cookiecutter.repo_name | replace("_", "-") }}.readthedocs.io.
{% endif %}

Setup
--------

Setup the project environment

.. code-block:: bash

$ conda env create --prefix ./env --file environment.yml

::

Activate the environment

.. code-block:: bash

$ conda activate ./env

::

Install the project package

.. code-block:: bash

$ pip install .

::


For updating the environment and dependencies, change environment.yml and run

.. code-block:: bash

conda env update --prefix ./env --file environment.yml --prune

::

Features
--------

* TODO
