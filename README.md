# ReverseShell_WindowsAV_Bypass
Compile reverse shell into static executable with pyinstaller. AV does not trigger on the following Windows versions and patches:

Passes as of patch on Windows 10 Pro:
-------------------------------------
KB5034122 1/11/2024
KB5034441 1/11/2024

Passes as of patch on Windows 2022 Server:
------------------------------------------
KB5034129 1/11/2024 
KB5034286 1/11/2024 

FAILS AV CHECK ON WINDOWS 10 HOME PATCH:
----------------------------------------
KB5034122 1/10/2024


Compilation steps (Done on Windows 10 Home):
---------

```
git clone https://github.com/Business1sg00d/ReverseShell_WindowsAV_Bypass.git
```

1. Create a virtual environment and activate (optional but recommended):
```
python3 -m venv ReverseShell_WindowsAV_Bypass
cd ReverseShell_WindowsAV_Bypass
.\Scripts\activate.bat
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

