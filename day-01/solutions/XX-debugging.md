# Debugging
When we run this script through Python, it will be executed from top to bottom, only showing us the things we explicitly `print`. We can, however, also run the script line by line. This is very helpful when we are trying to understand a program or are looking for a bug. To do this, we run the script with the Python _debugger_.

To use the debugger, we first set a breakpoint in the code. This will pause the execution of the script at that position so we can jump in and inspect it. You set a breakpoint on a line of code in the script by clicking to the left of the line number, which makes a red dot appear.

- Set a breakpoint on the first line of the script
- Run the script in the debugger by choosing `Python Debugger: Debug Python File` from the dropdown menu under the ▶️ icon in the top right

You should see VS Code switching to the `Run and Debug` tab on the Primary Side Bar. After a few moments, the debugger will launch and execute the script up to the breakpoint.