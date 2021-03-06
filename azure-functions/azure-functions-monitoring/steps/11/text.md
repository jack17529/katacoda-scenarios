While developing an application, you often want to what's being written to the logs in near-real time when running in Azure.

There are two ways to view a stream of log files being generated by your function executions.

- **Built-in log streaming:** the App Service platform lets you view a stream of your application log files. This is equivalent to the output seen when you debug your functions during local development and when you use the Test tab in the portal. All log-based information is displayed. For more information, see How to stream logs. This streaming method supports only a single instance, and can't be used with an app running on Linux in a Consumption plan.

- **Live Metrics Stream:** when your function app is connected to Application Insights, you can view log data and other metrics in near-real time in the Azure portal using Live Metrics Stream. Use this method when monitoring functions running on multiple-instances or on Linux in a Consumption plan. This method uses sampled data.

Log streams can be viewed both in the portal and in most local development environments.