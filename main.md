# admin-test
```
net user administrator /active:yes
```

```
cd C:\Windows\System32
```

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

```
string strCmdText;
strCmdText = "command";
System.Diagnostics.Process.Start("CMD.exe", strCmdText);
```
