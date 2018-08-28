#Simple Usage C# file

`csharp
using System;
using System.Collections.Generic;
using Pepipost.Controllers;
using Pepipost.Models;
using Pepipost.Exceptions;
using Pepipost.Utilities;
using Pepipost.Http;
using Newtonsoft.Json;
using Newtonsoft.Json.Converters;
using Newtonsoft.Json.Linq;

namespace TestConsoleProject
{
    class MainClass
    {
        public static void Main(string[] args)
        {
            //initialization of library
            Pepipost.PepipostClient client = new Pepipost.PepipostClient();
            EmailController email = client.Email;
            EmailBody body = new EmailBody();

            string apiKey = "Your api key here";

            body.Personalizations = new List<Personalizations>();

            Personalizations body_personalizations_0 = new Personalizations();

            body_personalizations_0.Recipient = "rcptemail id here";
            body_personalizations_0.Attributes = APIHelper.JsonDeserialize<Object>("{}");
            body.Personalizations.Add(body_personalizations_0);

            body.From = new From();

            body.From.FromEmail = "info@your verified domain";
            body.From.FromName = "pepi";
            body.Subject = "Pepipost";
            body.Content = "<html><body>Hello Folks,<br><br>Congratulations, Integration is Successfully Completed.<br>This is your first email from Pepipost C# library.<br>Happy Emailing<br><br>Thanks,<br>Pepipost";
            body.Settings = new Settings();

            body.Settings.Footer = 0;
            body.Settings.Clicktrack = 1;
            body.Settings.Opentrack = 1;
            body.Settings.Unsubscribe = 1;
			SendEmailResponse result = email.CreateSendEmailAsync(apiKey, body).Result;

            try
            {
				if(result.Message.Contains("Error")){
					Console.WriteLine("\n" + "Message ::" + result.Message + "\n" + "Error Code :: " + result.ErrorInfo.ErrorCode + "\n" + "Error Message ::" + result.ErrorInfo.ErrorMessage + "\n");
				}else{
					Console.WriteLine("\n" + "Message ::" + result.Message);
				}
                
            }
            catch (APIException) { };

            Console.WriteLine("Happy Mailing !");
        }
    }
}
