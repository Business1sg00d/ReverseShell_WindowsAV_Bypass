# ReverseShell_WindowsAV_Bypass
Compile reverse shell into static executable with pyinstaller. Tested on fully patched Windows 10 Home/Pro and Windows Server 2022. AV does not trigger.


Compilation steps (Done on Windows 10 Home):
---------

```
git clone
```

1. Create a virtual environment and activate (optional but recommended; the folder name in this exampel is AV_Repo):
```
C:\>python3 -m venv AV_Repo
cd AV_Repo
C:\AV_Repo>.\Scripts\activate.bat
```

2. With pip:
```
pip install pywin32
pip install pyinstaller==4.10
```

3. Create spec file with:
```
pyi-makespec --onefile client.py
```

4. Compile:
```
pyinstaller --onefile -w client.spec
```

PoC:
----


https://github.com/Business1sg00d/ReverseShell_WindowsAV_Bypass/assets/112768445/c7699023-1947-4dbe-9962-c6fd4ec93a4a


![root_root](https://github.com/Business1sg00d/ReverseShell_WindowsAV_Bypass/assets/112768445/afce18a1-facf-43a1-8eb8-8d521cabeeb1)

