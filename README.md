# mono420_signalR2
To show the error when running the SignalR 2 Tutorial Project on Mono 4.2.0

ref: http://www.asp.net/signalr/overview/getting-started/tutorial-getting-started-with-signalr

using: Visual Studio 2013, Raspberry Pi running raspbian, Mono 4.2.0 (25 Aug 2015), xsp4


The following is the error when the site is first accessed by browser:

![alt text](http://www.iguardsystem.com/upload/capture.jpg "xsp4 error")

pi@raspberrypi ~ $ cd www
pi@raspberrypi ~/www $ xsp4
xsp4
Listening on address: 0.0.0.0
Root directory: /home/pi/www
Listening on port: 9000 (non-secure)
Hit Return to stop the server.
System.NotSupportedException: Collection is read-only.
  at System.Collections.Specialized.NameObjectCollectionBase.BaseRemove (System.String name) <0x72f29890 + 0x0016c> in <filename unknown>:0
  at System.Collections.Specialized.NameValueCollection.Remove (System.String name) <0x72f29838 + 0x0002b> in <filename unknown>:0
  at Microsoft.Owin.Host.SystemWeb.OwinCallContext.RemoveAcceptEncoding () <0x72d0b510 + 0x00117> in <filename unknown>:0
  at Microsoft.Owin.Host.SystemWeb.OwinCallContext.DisableResponseCompression () <0x72d0b460 + 0x0001f> in <filename unknown>:0
  at Microsoft.AspNet.SignalR.OwinEnvironmentExtensions.DisableRequestCompression (IDictionary`2 environment) <0x72d0b348 + 0x0004b> in <filename unknown>:0
  at Microsoft.AspNet.SignalR.PersistentConnection.ProcessRequest (IDictionary`2 environment) <0x72d0a0d8 + 0x00043> in <filename unknown>:0
  at Microsoft.AspNet.SignalR.Owin.Middleware.HubDispatcherMiddleware.Invoke (IOwinContext context) <0x72d15dc8 + 0x000c3> in <filename unknown>:0
  at Microsoft.Owin.Mapping.MapMiddleware+<Invoke>d__0.MoveNext () <0x72d565c0 + 0x002ef> in <filename unknown>:0
--- End of stack trace from previous location where exception was thrown ---
   at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw () in <filename unknown>:line 0
   at Microsoft.Owin.Host.SystemWeb.Infrastructure.ErrorState.Rethrow () in <filename unknown>:line 0
   at Microsoft.Owin.Host.SystemWeb.IntegratedPipeline.StageAsyncResult.End (IAsyncResult ar) in <filename unknown>:line 0
   at Microsoft.Owin.Host.SystemWeb.IntegratedPipeline.IntegratedPipelineContext.EndFinalWork (IAsyncResult ar) in <filename unknown>:line 0
   at System.Web.AsyncInvoker.<doAsyncCallback>m__0 (System.Object ores) in <filename unknown>:line 0
