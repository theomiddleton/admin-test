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
            
         
