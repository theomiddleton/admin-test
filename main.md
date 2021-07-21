# Admin Test

In CMD give admin
```
net user administrator /active:yes
```
admin cmd
```
cd C:\Windows\System32
```
open cmd as admin
```
using System;
using System.Diagnostics;

namespace run_admin2
{
    class Program
    {
        static void Main(string[] args)
        {
            System.Diagnostics.ProcessStartInfo info = new ProcessStartInfo("cmd.exe");
            info.UseShellExecute = true;
            info.Verb = "runas";
            Process.Start(info);
        }
    }
}
```
open cmd and run command
```
string strCmdText;
strCmdText = "RUN COMMAND HERE";
System.Diagnostics.Process.Start("CMD.exe", strCmdText);
```
open cmd and run command 2
```
Process cmd = new Process();
cmd.StartInfo.FileName = "cmd.exe";
cmd.StartInfo.RedirectStandardInput = true;
cmd.StartInfo.RedirectStandardOutput = true;
cmd.StartInfo.CreateNoWindow = false;
cmd.StartInfo.UseShellExecute = true;
cmd.Start();

cmd.StandardInput.WriteLine("echo test");
cmd.StandardInput.Flush();
cmd.StandardInput.Close();
cmd.WaitForExit();
Console.WriteLine(cmd.StandardOutput.ReadToEnd());
```

<h2> Other </h2>

```
gpedit.msc
```
cmd
```
User Configuration > Administrative Templates > System
```
tskmgr
```
Configuration -> Administrative Templates -> System
```


win r 
```
REG add HKCU\Software\Policies\Microsoft\Windows\System /v DisableCMD /t REG_DWORD /d 0 /f
```
God Mode (rename folder)
```
Balls.{ED7BA470-8E54-465E-825C-99712043E01C}
```
