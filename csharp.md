# C#调用exe程序

  Process myProcess = new Process();
  
  string fileName = @"C:/Test.exe";
  
  string para ＝@"你好 北京欢迎你！";
  
  ProcessStartInfo myProcessStartInfo = new ProcessStartInfo(fileName, para);
  
  myProcess.StartInfo = myProcessStartInfo;
  
  myProcess.Start();
  
  while (!myProcess.HasExited)
  
  {
  
     myProcess.WaitForExit();
  
  }

  int returnValue = myProcess.ExitCode;
