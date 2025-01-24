# PYTHON DEPRECATION TIMELINE

=========================

## Python Next

-----------

### General Deprecations

#### argparse

- Nested argument groups and mutually exclusive groups
- `prefix_chars` keyword in `add_argument_group()`
- `FileType` type converter

#### builtins

- `bool(NotImplemented)`
- Generator `throw(type, exc, tb)` and `athrow(type, exc, tb)` signatures
- Numeric literals followed by keywords (e.g. `0in x`, `1or x`)
- `__index__()` and `__int__()` returning non-int types
- `__float__()` returning float subclass
- `__complex__()` returning complex subclass
- `int()` delegation to `__trunc__()`
- Complex numbers as real/imag args in `complex()`

#### Other Modules

- `array 'u'` format code
- `calendar` month constants (use uppercase)
- `codeobject.co_lnotab`
- `datetime` UTC methods
- Various `gettext`, `importlib`, `logging`, `mailbox` features
- `os.register_at_fork()` in multi-threaded process
- `pydoc.ErrorDuringImport` tuple value
- `re` numerical group references
- `sre_*` modules
- `shutil.rmtree()` onerror parameter
- Multiple `ssl` options and protocols
- Various `threading`, `unittest`, `urllib.parse` functions
- `xml.etree.ElementTree` truth testing
- `zipimport.zipimporter.load_module()`

#### Future removals (unscheduled)

- `Py_TPFLAGS_HAVE_FINALIZE`
- Various `PyErr_*` functions
- `PyModule_*`, `PyOS_*`, `PySlice_*`, `PyUnicode_*` functions
- Thread Local Storage (TLS) API

## Python 3.16

-----------

### DEPRECATED in Python 3.16

- ```Bitwise inversion (~) on bool type``` (will error in 3.16)
- ```from __future__ import annotations``` (removal after Python 3.13 EOL in 2029)

### REMOVED in Python 3.16

- ```builtins._enablelegacywindowsfsencoding()``` (use ```PYTHONLEGACYWINDOWSFSENCODING``` env var)
- ```ExecError exception in shutil``` (use ```RuntimeError```)
- ```functools.reduce() with function/sequence keyword args```
- ```Import system __loader__ without __spec__.loader```
- ```sysconfig.expand_makefile_vars()``` (use ```get_paths() vars arg```)
- ```symtable.Class.get_methods()```
- ```tarfile.TarFile.tarfile attribute```

-----------

## Python 3.15

-----------
`

### DEPRECATED in Python 3.15

- ```asyncio.Policy system``` (removal in 3.16)
- ```ctypes.SetPointerType``` (removal in 3.15)
- ```http.server.CGIHTTPRequestHandler``` (removal in 3.15)
- ```pathlib.PurePath.is_reserved``` (removal in 3.15)
- ```sqlite3.connect() multiple args``` (keyword-only in 3.15)
- ```typing.Keyword args in NamedTuple``` (removal in 3.15)

### REMOVED in Python 3.15

- ```argparse type, choices, metavar in BooleanOptionalAction```
- ```ast legacy classes: Bytes, Ellipsis, NameConstant, Num, Str```
- ```asyncio child watcher features```
- ```Collections.abc.ByteString```
- ```email.utils.localtime() isdst parameter```
- ```importlib.abc.ResourceReader classes```
- ```itertools copy/deepcopy/pickle support```
- ```pathlib extra keyword arguments```
- ```sqlite3.version info and named placeholders```
- ```NotImplemented in boolean context```
- ```int() delegation to __trunc__```

#### Pending removal in 3.15

- Bundled libmpdecimal
- `PyImport_ImportModuleNoBlock()`
- `PyWeakref_*` functions
- `Py_UNICODE` type
- Multiple Python initialization functions
- Global configuration variables

-----------

## Python 3.14

-----------

### DEPRECATED in Python 3.14

- ```argparse.FileType type converter```
- ```argparse.prefix_chars in add_argument_group()```
- ```asyncio.iscoroutinefunction``` (use ```inspect.iscoroutinefunction```)
- ```builtins.Complex numbers as real/imag args in complex()```
- ```functools.Function/sequence as keyword args in reduce()```
- ```os.popen() and spawn* functions``` (use ```subprocess```)
- ```symtable.Class.get_methods()```
- ```urllib.parse.parse_qsl() and parse_qs() accepting non-empty falsy values```

### REMOVED in Python 3.14

- ```argparse.Nested argument groups```
- ```asyncio.child watcher features```
- ```imp module```
- ```locale.format()```
- ```ssl legacy functions```
- ```master_open() method```

-----------

## Python 3.13

-----------

### DEPRECATED in Python 3.13

- ```builtins.Mismatched code object assignments```
- ```array 'u' format code``` (use ```'w'```)
- ```ctypes.ARRAY``` (use ```type * length```)
- ```decimal 'N' format specifier```
- ```functools.partial as method``` (use ```staticmethod```)
- ```re.Positional maxsplit/count/flags```
- ```typing.AnyStr``` (removal from __all__ in 3.16)

### REMOVED in Python 3.13

- ```asynchat and asyncore modules```
- ```distutils package```
- ```lib2to3 module and 2to3 tool```
- ```Legacy modules (PEP 594)```
- ```Pathlib extra positional args```
- ```Various unittest legacy features```

-----------

## Python 3.12

-----------

### DEPRECATED in Python 3.12

- ```asyncio.child watchers```
- ```calendar month constants``` (use ```uppercase```)
- ```collections.abc.ByteString```
- ```datetime UTC methods``` (use ```timezone aware```)
- ```os.stat() st_ctime on Windows```
- ```shutil.rmtree() onerror``` (use ```onexc```)
- ```typing legacy types```
- ```xml.etree.ElementTree Element truth value```

### REMOVED in Python 3.12

- ```asynchat and asyncore``` (use ```asyncio```)
- ```distutils``` (use ```setuptools```)
- ```imp module```
- ```sqlite3 shared cache```

-----------

## Python 3.11

-----------

### DEPRECATED in Python 3.11

- ```Chained classmethod descriptors```
- ```Octal escapes > 0o377```
- ```int() __trunc__ delegation```
- ```configparser.LegacyInterpolation```
- ```locale functions```
- ```re.template()```
- ```typing.Text```
- ```unittest legacy features```
- ```pathlib.Path.link_to```

### REMOVED in Python 3.11

- ```asynchat and asyncore``` (use ```asyncio```)
- ```distutils package```
- ```imp module```
- ```unittest.mock.__version__```

-----------

## Python 3.10

-----------

### DEPRECATED in Python 3.10

- ```Numeric literals immediately followed by keywords``` (e.g., '0in x', '1or x')
- ```distutils package``` (entire package to be deprecated, will be removed in Python 3.12)
- ```Non-integer arguments to random.randrange()```
- ```Various importlib loader methods``` (use ```find_spec()``` instead)
- ```pathlib.Path.link_to```

### REMOVED in Python 3.10

- ```Special methods for complex class: __int__, __float__, etc.```
- ```parser module and related C files```
- ```formatter module```

-----------

## Python 3.9

-----------

### DEPRECATED in Python 3.9

- ```distutils.bdist_msi command``` (use ```bdist_wheel``` instead)
- ```math.factorial() accepting float values``` (will raise TypeError in future)
- ```parser and symbol modules```
- ```Using NotImplemented in boolean context```

### REMOVED in Python 3.9

- ```unittest.mock.__version__```
- ```array.array tostring() and fromstring() methods```
- ```smtpd.MailmanProxy```
- ```lib2to3 module``` (emits PendingDeprecationWarning)
- ```random parameter of random.shuffle()```

-----------

## Python 3.8

-----------

### DEPRECATED in Python 3.8

- ```Yield expressions in comprehensions and generator expressions```
- ```Identity checks (is/is not) with literal values``` (raises SyntaxWarning)
- ```__str__ implementations in builtin types (bool, int, float, complex)```
- ```macpath module``` (removed in 3.8)
- ```time.clock``` (use ```time.perf_counter``` or ```time.process_time``` instead)
- ```filemode function from tarfile module```
- ```XMLParser html argument and doctype() method```
- ```"unicode_internal" codec```
- ```sqlite3 Cache and Statement objects exposure```
- ```fileinput.input/FileInput bufsize parameter```
- ```sys.set_coroutine_wrapper and sys.get_coroutine_wrapper```
- ```PyEval_ReInitThreads function from C API```
- ```Using #-format codes in argument parsing without PY_SSIZE_T_CLEAN```
- ```Collections.abc imports from collections module``` (removal delayed to 3.9)

### REMOVED in Python 3.8

- ```platform.popen``` (use ```os.popen``` instead)
- ```time.clock``` (use ```time.perf_counter``` or ```time.process_time``` instead)
- ```pyvenv script```
- ```parse_qs, parse_qsl, escape from cgi module```
- ```filemode from tarfile module```
- ```XMLParser html argument```
- ```XMLParser.doctype() method```
- ```"unicode_internal" codec```
- ```sqlite3.Cache and sqlite3.Statement objects```
- ```fileinput.input/FileInput bufsize parameter```
- ```sys.set_coroutine_wrapper and sys.get_coroutine_wrapper```
- ```bufsize parameter in fileinput.input```
- ```PyEval_ReInitThreads function```
- ```Non-ASCII digit/group references in regular expressions```
- ```macpath module```
- ```C API functions for pgen```
- ```PyNode_AddChild and PyParser_AddToken without end position parameters```

-----------

## Python 3.7

-----------

### DEPRECATED in Python 3.7

- ```Yield expressions in comprehensions and generator expressions``` (except leftmost for clause)
- ```Returning subclass of complex from object.__complex__```
- ```object.__aiter__ methods as asynchronous```
- ```Non-integer value for selecting a plural form in gettext```
- ```importlib.abc classes:```
  - ```MetaPathFinder.find_module``` (use ```find_spec```)
  - ```PathEntryFinder.find_loader``` (use ```find_spec```)
  - ```ResourceLoader``` (use ```ResourceReader```)
- ```locale.format()``` (use ```format_string```)
- ```subprocess.Popen defaults to close_fds=False``` (changed to True)
- ```Silent argument truncation in socket.htons and socket.ntohs```
- ```ssl.wrap_socket``` (use ```SSLContext.wrap_socket```)
- ```sys.set_coroutine_wrapper and sys.get_coroutine_wrapper```
- ```sys.callstats() function```
- ```Nested sets and set operations in regular expressions```
- ```PySlice_GetIndicesEx function in C API```
- ```PyOS_AfterFork``` (use ```PyOS_BeforeFork```, ```PyOS_AfterFork_Parent``` or ```PyOS_AfterFork_Child```)
  
### REMOVED in Python 3.7

- ```os.stat_float_times() function```
- ```Unknown escapes in regular expressions```
- ```exclude argument in tarfile.TarFile.add```
- ```ntpath.splitunc function``` (use ```splitdrive```)
- ```collections.namedtuple verbose parameter and _source attribute```
- ```Keyword arguments to bool(), float(), list(), tuple()```
- ```Positional-only first argument to int()```
- ```plistlib classes: Plist, Dict, _InternalDict```
- ```asyncio.windows_utils.socketpair()``` (use ```socket.socketpair```)
- ```asyncio exports of selectors and _overlapped modules```
- ```Direct instantiation of ssl.SSLSocket and ssl.SSLObject```
- ```distutils install_misc command```
- ```fpectl module```
- ```STORE_ANNOTATION opcode```

-----------

## Python 3.6

-----------

### DEPRECATED in Python 3.6

- ```'async' and 'await' as variable/class/function/module names``` (will be keywords in 3.7)
- ```Raising StopIteration inside a generator``` (will raise RuntimeError in 3.7)
- ```__aiter__ returning an awaitable``` (should return async iterator directly)
- ```Invalid escape sequences in strings``` (will be SyntaxError in future)
- ```Relative imports falling back on __name__ and __path__ when __spec__/__package__ undefined```
- ```asynchat module``` (use ```asyncio``` instead)
- ```asyncore module``` (use ```asyncio``` instead)
- ```dbm.dumb module's 'rw' mode behavior```
- ```distutils.Distribution extra_path argument```
- ```Non-integer arguments in grp.getgrgid()```
- ```importlib.machinery.SourceFileLoader.load_module()```
- ```importlib.machinery.SourcelessFileLoader.load_module()```
- ```importlib.machinery.WindowsRegistryFinder```
- ```General bytes-like objects as paths in os functions```
- ```Inline regex flags in middle of pattern```
- ```OpenSSL 0.9.8, 1.0.0, 1.0.1 in ssl module```
- ```SSL arguments (certfile, keyfile, check_hostname) in ftplib, http.client, imaplib, poplib, smtplib```
- ```Various ssl protocols and functions```
- ```tkinter.tix module``` (use ```tkinter.ttk```)
- ```pyvenv script``` (use ```python3 -m venv```)
- ```PyUnicode_AsEncodedObject, PyUnicode_AsDecodedObject C API functions```
- ```--with-system-ffi configure flag``` (now default on non-macOS UNIX)

### REMOVED in Python 3.6

- ```Unknown escapes in regular expressions``` (still allowed in re.sub templates but deprecated)
- ```inspect.getmoduleinfo()```
- ```Various undocumented traceback methods and Ignore class```
- ```tk_menuBar() and tk_bindForTraversal() from tkinter```
- ```ZipFile.open() 'U' mode```
- ```Undocumented platform-specific modules (IN, CDROM, DLFCN, TYPES, CDIO, STROPTS)```
- ```asynchat.fifo class```
- ```PyExc_RecursionErrorInst singleton``` (in 3.6.4)

-----------
