<h2>Motivation</h2>
experiment with python modules and packages


<h2>Points of interest</h2>
<ul>
<li>a src and test packages are created by adding __init__.py to the directories lib and test respectively</li>
<li>modules within the same package can access each other using . as package check e.g from .gen_utils import print_with_stars
in utils.py</li>
<li>modules not within the same package can access each other using the package name check e.g. from lib.utils import add in test_utils.py and from lib.utils import add in run_lib.py</li>
<li>run_lib.py is executed using : py run_lib.py and must not be inside lib directory. it is working when it is in lib parent directory</li>
<li>you can invoke pytest from root directory to run the tests. more info about pytest <a href='https://github.com/NathanKr/python-unit-testing-with-pytest-playground'>here</a></li>
</ul>