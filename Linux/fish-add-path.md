On the Fish shell, you can add directories to your PATH by modifying the `config.fish` file. Here's how you can do it:

### Step 1: Open the Fish Configuration File
Open the Fish configuration file `config.fish` in a text editor. You can use any text editor you prefer. For example:

```sh
nano ~/.config/fish/config.fish
```

### Step 2: Add the Directory to PATH
Inside the `config.fish` file, add a line to append the directory you want to add to your PATH. For example, to add `/path/to/your/directory`, you would write:

```fish
set -x PATH /path/to/your/directory $PATH
```

Replace `/path/to/your/directory` with the actual path to the directory you want to add to the PATH.

### Step 3: Save and Exit
Save the changes you made to the `config.fish` file and exit the text editor.

### Step 4: Apply the Changes
To apply the changes immediately without having to restart your Fish shell, you can run:

```sh
source ~/.config/fish/config.fish
```

### Verifying the Changes
To verify that the directory has been successfully added to your PATH, you can echo the PATH variable:

```sh
echo $PATH
```

You should see the directory you added at the beginning or end of the output.

### Note:
- Make sure the directory you're adding to the PATH contains executable files or scripts that you want to be accessible from anywhere in the terminal.
- Always be cautious when modifying configuration files, as incorrect modifications could potentially cause issues with your shell environment.



## Example 

```fish
set -x PATH ~/.local/bin/ $PATH
```


