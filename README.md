# PyGoat
<!-- ALL-CONTRIBUTORS-BADGE:START - Do not remove or modify this section -->
[![All Contributors](https://img.shields.io/badge/all_contributors-9-orange.svg?style=flat-square)](#contributors-)
<!-- ALL-CONTRIBUTORS-BADGE:END -->

intentionally vuln web Application Security in django.
our roadmap build intentionally vuln web Application in django. The Vulnerability can based on OWASP top ten
<br>

Table of Contents
=================

* [pygoat](#pygoat)
   * [Installation](#installation)
      * [From Sources](#from-sources)
      * [Docker Container](#docker-container)
      * [Installation Video](#installation-video)
   * [Uninstallation](#uninstallation)
   * [Solutions](/Solutions/solution.md)
   * [For Developers](/docs/dev_guide.md)
   * [My Contributions](#my-personal-contributions-and-experiences) 

## Installation

### From Sources

To setup the project on your local machine:
<br>

First, Clone the repository using GitHub website or git in Terminal
```
  git clone https://github.com/adeyosemanputra/pygoat.git
  ### To Download a specific branch
  git clone -b <branch_name> https://github.com/adeyosemanputra/pygoat.git
```
### Windows Notes (PowerShell users)

- PyGoat is tested primarily on Linux/macOS. Windows users are recommended to use:
  - **Docker Desktop** (preferred), or
  - **WSL2 (Ubuntu)** for smoother setup.
- On some Windows environments, the `python3` command may not be available by default.
  - If `python3` is not recognized, try using `python` instead (ensure it points to Python 3.x).
- Ensure Python version is **3.10 or 3.11** for best compatibility.
- Some labs rely on Unix-style commands and may behave differently on native Windows shells.


#### Method 1

1. Install all app and python requirements using installer file - `bash installer.sh`
2. Apply the migrations `python3 manage.py migrate`.<br>
3. Finally, run the development server `python3 manage.py runserver`.<br>
4. The project will be available at <http://127.0.0.1:8000> 

#### Method 2

1. Install python3 requirements `pip install -r requirements.txt`.<br> 
2. Apply the migrations `python3 manage.py migrate`.<br>
3. Finally, run the development server `python3 manage.py runserver`.<br>
4. The project will be available at <http://127.0.0.1:8000> 

#### Method 3

1. Install all app and python requirements using `setup.py` file - `pip3 install .`
2. Apply the migrations `python3 manage.py migrate`.<br>
3. Finally, run the development server `python3 manage.py runserver`.<br>
4. The project will be available at <http://127.0.0.1:8000> 

### Docker Container
1. Install [Docker](https://www.docker.com)
2. Run `docker pull pygoat/pygoat` or `docker pull pygoat/pygoat:latest`
3. Run `docker run --rm -p 8000:8000 pygoat/pygoat:latest`
4. Browse to <http://127.0.0.1:8000> 
5. Remove existing image using `docker image rm pygoat/pygoat` and pull again incase of any error

### From Docker-Compose 
1. Install [Docker](https://www.docker.com)
2. Run `docker-compose up` or `docker-compose up -d`

## Populate Challenge Data

PyGoat stores challenge definitions in `challenge/challenge.json`.
To populate the `Challenge` table in the database from this file, use the
built-in Django management command:

### Using Docker Compose

```bash
docker compose exec web python manage.py populate_challenges


### Build Docker Image and Run
1. Clone the repository  &ensp; `git clone https://github.com/adeyosemanputra/pygoat.git` 
2. Build the docker image from Dockerfile using &ensp; `docker build -f Dockerfile -t pygoat .`
3. Run the docker image &ensp;`docker run --rm -p 8000:8000 pygoat:latest`
4. Browse to <http://127.0.0.1:8000> or <http://0.0.0.0:8000> 

### Installation video 

1. From Source using `installer.sh`
 - [Installing PyGoat from Source](https://www.youtube.com/watch?v=7bYBJXG3FRQ)
2. Without using `installer.sh`
 - [![](http://img.youtube.com/vi/rfzQiMeiwso/0.jpg)](http://www.youtube.com/watch?v=rfzQiMeiwso "Installation Pygoat")
3. Install with Mac M1 (using Virtualenv)
 - [![](http://img.youtube.com/vi/rfzQiMeiwso/0.jpg)](https://youtu.be/a5UV7mUw580 "Install with Mac M1 - using Virtualenv")


## Uninstallation

### On Debian/Ubuntu Based Systems
- On Debian/Ubuntu based systems, you can use the `uninstaller.sh` script to uninstall `pygoat` along with all it's dependencies.
- To uninstall `pygoat`, simply run:
```bash
$ bash ./uninstaller.sh
```

### On Other Systems
- On other systems, you can use the `uninstaller.py` script to uninstall `pygoat` along with all it's dependencies
- To uninstall `pygoat`, simply run:
```bash
$ python3 uninstaller.py
```

## Solutions 
<a href="/Solutions/solution.md">Solutions to all challenges</a>

## Contributors ✨

Thanks goes to these wonderful people ([emoji key](https://allcontributors.org/docs/en/emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <tr>
    <td align="center"><a href="https://github.com/pwned-17"><img src="https://avatars.githubusercontent.com/u/61360833?v=4?s=100" width="100px;" alt=""/><br /><sub><b>pwned-17</b></sub></a><br /><a href="https://github.com/adeyosemanputra/pygoat/commits?author=pwned-17" title="Code">💻</a></td>
    <td align="center"><a href="https://github.com/prince-7"><img src="https://avatars.githubusercontent.com/u/53997924?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Aman Singh</b></sub></a><br /><a href="https://github.com/adeyosemanputra/pygoat/commits?author=prince-7" title="Code">💻</a></td>
    <td align="center"><a href="https://github.com/adeyosemanputra"><img src="https://avatars.githubusercontent.com/u/24958168?v=4?s=100" width="100px;" alt=""/><br /><sub><b>adeyosemanputra</b></sub></a><br /><a href="https://github.com/adeyosemanputra/pygoat/commits?author=adeyosemanputra" title="Code">💻</a> <a href="https://github.com/adeyosemanputra/pygoat/commits?author=adeyosemanputra" title="Documentation">📖</a></td>
    <td align="center"><a href="https://github.com/gaurav618618"><img src="https://avatars.githubusercontent.com/u/29380890?v=4?s=100" width="100px;" alt=""/><br /><sub><b>gaurav618618</b></sub></a><br /><a href="https://github.com/adeyosemanputra/pygoat/commits?author=gaurav618618" title="Code">💻</a> <a href="https://github.com/adeyosemanputra/pygoat/commits?author=gaurav618618" title="Documentation">📖</a></td>
    <td align="center"><a href="https://github.com/kUSHAL0601"><img src="https://avatars.githubusercontent.com/u/29600964?v=4?s=100" width="100px;" alt=""/><br /><sub><b>MajAK</b></sub></a><br /><a href="https://github.com/adeyosemanputra/pygoat/commits?author=kUSHAL0601" title="Code">💻</a></td>
    <td align="center"><a href="https://github.com/JustinDPerkins"><img src="https://avatars.githubusercontent.com/u/60413733?v=4?s=100" width="100px;" alt=""/><br /><sub><b>JustinPerkins</b></sub></a><br /><a href="https://github.com/adeyosemanputra/pygoat/commits?author=JustinDPerkins" title="Code">💻</a></td>
    <td align="center"><a href="https://github.com/Hkakashi"><img src="https://avatars.githubusercontent.com/u/43193113?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Liu Peng</b></sub></a><br /><a href="https://github.com/adeyosemanputra/pygoat/commits?author=Hkakashi" title="Code">💻</a></td>
  </tr>
  <tr>
    <td align="center"><a href="https://github.com/RupakBiswas-2304"><img src="https://avatars.githubusercontent.com/u/75058161?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Metaphor</b></sub></a><br /><a href="https://github.com/adeyosemanputra/pygoat/commits?author=RupakBiswas-2304" title="Code">💻</a></td>
    <td align="center"><a href="https://whokilleddb.github.io"><img src="https://avatars.githubusercontent.com/u/56482137?v=4?s=100" width="100px;" alt=""/><br /><sub><b>whokilleddb</b></sub></a><br /><a href="https://github.com/adeyosemanputra/pygoat/commits?author=whokilleddb" title="Code">💻</a></td>
  </tr>
</table>

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://github.com/all-contributors/all-contributors) specification. Contributions of any kind welcome!

# My Personal Contributions and Experiences 

## 🔐 CodeQL Vulnerability Fix: Code Injection via ``eval()``

The first vulnerability I tackled was in the ``introduction/view.py`` file around line 460. The function used ``eval()`` on user-controlled input, creating a direct code-injection risk. CodeQL flagged this as a high-severity issue ``eval()`` executes whatever string it receives, meaning a malicious user could run arbitrary Python code on the server.

Fixing this vulnerability taught me far more than just "replace eval". 
The process involved:
* understanding how CodeQL traces data flow from user input to dangerous sinks
* learning why ``eval()`` is unsafe and how code injection actually happens
* debugging indentation issues caused by mixed tabs/spaces
* untangling nested Django view logic to place the fix correctly
* restarting the file more than once to escape indentation chaos
* validating the fix by re-running CodeQL and watching the alert disappear

To remediate the issue, I replaced `` eval()`` with ``ast.literal_eval``, which safely parses Python literals without executing arbitrary code. This preserves the intended functionality while eliminating the injection risk.

This was a small code change, but a meaningful step in understanding secure coding practice, static analysis, and how vulnerabilities emerge in real applications. 

### 🔍 Before (vulnerable code)
```
print(val)
try:
    output = eval(val)   # ❌ Unsafe: executes arbitrary code
except:
    output = "Something went wrong"
return render(request, 'Lab/CMD/cmd_lab2.html', {"output": output})
```
### ✅ After (safe code)
``` 
import ast

print(val)
try:
    output = ast.literal_eval(val)   # ✔ Safe: parses literals without executing code
except Exception:
    output = "Something went wrong"
return render(request, 'Lab/CMD/cmd_lab2.html', {"output": output}) 
```
### 📘 What I Learned

- How CodeQL identifies unsafe data flows from user input to dangerous functions  
- Why `eval()` is inherently unsafe and how code injection vulnerabilities occur  
- How to use `ast.literal_eval` as a secure alternative  
- How indentation issues (tabs vs. spaces) can break Python logic  
- How Django view functions process requests and return responses  
- How to validate a fix by re-running CodeQL and confirming the alert disappears  
- The value of restarting a file cleanly when indentation chaos becomes unmanageable

 ### 🚀 Future Improvements

- Continue reviewing PyGoat for additional CodeQL alerts  
- Document each vulnerability fix as a separate case study  
- Expand the CodeQL workflow to include custom queries  
- Add unit tests to validate safe input handling  
- Explore other static analysis tools (Bandit, Semgrep) for comparison
