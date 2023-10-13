Windows Defender may hinder the task. You can turn it off it it does so.
<br>
Make sure **pip** and **pyinstaller** are installed/updated.

1. Create a directory that contains your **.py** file for the program and the **icon picture file (.ico)** 
1. Open your terminal and cd to the directory
1. Run the following command:
    ```shell
    pyinstaller <space>
                -F                      #(for all in 1 file .exe file)
                -w                      #(removes terminal window from the GUI)
                -i <.ico_file_name>     #(adds custom icon to .exe - icon)
                clock.py                #(name of your main python file)
    ```
1. ENTER
1. After successfull completion of the process, your **.exe** file will be created in the **dist** folder.