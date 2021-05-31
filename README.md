<h2>Motivation</h2>
experiment with python modules and packages

<h2>Tasks</h2>
<ol>
<li>access functions using import</li>
<li>create local packages for myutils and test</li>
<li>create global package for myutils .global package myutils can be accessed from any project on a PC where myutils is installed .can be uploaded to pip index (not done here). setup.py and wheel are used</li>
</ol>


<h2>packages</h2>
<ul>
<li>myutils and test packages are created by adding __init__.py to the directories myutils and test respectively</li>
<li>modules within the same package can access each other using . as package check e.g from .gen_utils import print_with_stars
in utils.py</li>
<li>modules not within the same package can access each other using the package name check e.g. from myutils.utils import add in test_utils.py and from myutils.utils import add in run_lib.py</li>
<li>run_lib.py is executed using : py run_lib.py and must not be inside myutils directory. it is working when it is in myutils parent directory</li>


<h2>global package</h2>
<ol>
<li>create setup.py on the project root</li>
<li>pip install wheel (if its not allready installed)</li>
<li>run from setup.py directory : py setup.py bdist_wheel. this will create dist , build and egginfo directories on the python project</li>
<li>run : pip install dist/wheel_file_inside_dit e.g pip install dist/myutils.1.0-py3-none-any.whl. this will copy some created files to python packages dir on the pc</li>
<li>make sure the global package e.g. myutils appears in : pip list</li>
<li>you can verify where the package installed using : pip show e.g. pip show myutils</li>
<li>after this you can import myutils from ANY directory on the pc where it is installed</li>
</ol>


<h2>pytest</h2>
this is not specific to packages but the directory tree is arranged such that you can invoke here pytest from root directory to run the tests. more info about pytest <a href='https://github.com/NathanKr/python-unit-testing-with-pytest-playground'>here</a>
>