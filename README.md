# Desktop Battery Notifier

As a laptop user, you must take caution about your battery percentage as the battery is also the most important component, that’s why today we will see Desktop Battery Notifier using Python.

So, what if your laptop reminds you about the battery percentage using notification. Yes, you read it correctly using a desktop notifier.

# Psutil Library in Python

Psutil in python is a cross-platform library for retrieving information on running processes and system utilization(CPU, memory, disks, networks, sensors) in Python.

You will need to install two modules one is ‘psutil’ and the other one is ‘plyer’ which will be used to get the notification.

To install ‘psutil’ in your pip. Here’s the command:

pip install psutil
The main function from the psutil module is psutil.sensors_battery() which returns a named tuple consisting of the following values. If no battery is installed or metrics can’t be determined None is returned.

percent: It gives the Power left on your laptop in percentage.

>>>battery.percent
Output:

52 #giving battery percentage
Now, if we want to check if the charger is plugged or not, we will have to use:

>>>power_plugged
This will return either True or False. True if power is plugged in, False if it isn’t charging. Here, in my case it is not plugged hence the output will be:

False
Now, to install ‘plyer’ in your pip. Here’s the simple command:

pip install plyer
As we have the package now, we're ready to import it into our python script.

from plyer import notification
Now, let’s specify the parameters. Let’s define the title and message.

title = ‘Battery Reminder’

message = ‘Battery is 52’

Let’s look at what the parameters mean:

title: Title of the notification

description: Message of the notification

timeout: duration to display the message say 10secs as default time used.

Now, let’s pass the parameters using the notify method.

notification.notify( “title”, “message”, timeout)

For eg I’m passing:

the title as ‘Battery Reminder’

message as ‘Battery is 52’

and timeout as 2 secs
