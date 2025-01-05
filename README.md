# Openbox Keybinds Extractor


Program designed to extract and display a list of keybindings from the Openbox configuration file (`rc.xml`). The program allows you to:

1. **Extract Keybindings:**
   - Assigned to execute commands (`Execute`).
   - Built-in Openbox actions (e.g., window management).

2. **Format Output:**
   - In a convenient format, including the option to display in two columns.
   - Replace default symbols (e.g., ⚫ or |) and key names (e.g., W → Win, A → Alt) with custom ones.

3. **Save Results:**
   - To text files:
     - `kbinds.txt` — all keybindings.
     - `ob-kbinds.txt` — only Openbox keybindings.
     - `user-kbinds.txt` — only user commands.
   - Display results in the terminal or a graphical window (using the `yad` utility).



## Installation

1. **Clone the Repository:**  
   Run the command:  
   `git clone https://github.com/Canubix/cx-kb.git`  
   Navigate to the project directory:  
   `cd cx-kb`

2. **Make the Script Executable:**  
   Make the script executable:  
   `chmod +x cx-kb`

3. **Install Dependencies:**  
   - Ensure `python3` is installed.  
   - Install `lxml` for XML parsing (optional, falls back to `xml.etree.ElementTree` if `lxml` is not available):  
     `pip install lxml`  
   - Install `yad` for graphical output (optional):  
     `sudo apt install yad`

 

## Command-Line Arguments
   - The program supports multiple arguments for customizing output, including:
     - `-o, --ob`: Output only Openbox keybindings (built-in actions).
     - `-u, --user`: Output only user-defined commands (`Execute` actions).
     - `-t, --symbol`: Replace the default symbol (⚫) with a custom symbol.
     - `-t2, --symbol2`: Replace the default symbol (|) with a custom symbol for two-column output.
     - `-c, --columns`: Display output in two columns.
     - `-s, --shorten`: Shorten paths in commands by removing everything up to the last `/`.
     - `-m, --modify`: Modify key names (e.g., W → Win, A → Alt, C → Ctl, S → Sht).
     - `-g, --gui`: Display results in a graphical window using `yad`.
     - `-x, --txt`: Save results to text files without displaying them in the terminal.
     - `-n, --newline`: Add an empty line after each command for better readability.
    


## Usage Examples


1. `./cx-kb --ob -t "★" -t2 "||"`  
   - Display only Openbox keybindings with custom symbols "★" and "||".

2. `./cx-kb --user --txt`  
   - Save user commands to a file.

3. `./cx-kb --gui`  
   - Display results in a graphical window.

4. `./cx-kb -c2 -s`  
   - Display keybindings in two columns with shortened paths.

5. `./cx-kb -m`  
   - Modify key names (e.g., W → Win, A → Alt) and display in the terminal.

6. `./cx-kb --ob -t "●" -t2 "│" --txt`  
   - Replace default symbols and save Openbox keybindings to a file.

7. `./cx-kb --user -t "➜" -n`  
   - Display user commands with custom symbols "➜" and add newlines after each command.

8. `./cx-kb --ob -t "◆" -t2 "║" -c2`  
   - Display Openbox keybindings with graphical symbols in two columns.

9. `./cx-kb -m -s --txt`  
   - Save all keybindings to a file with modified key names and shortened paths.

## Author
**Author:** Andrei Talchkou  
**Email:** majesticzero78@gmail.com  
**GitHub:** [https://github.com/Canubix/cx-kb](https://github.com/Canubix/cx-kb)  
**License:**  GNU
