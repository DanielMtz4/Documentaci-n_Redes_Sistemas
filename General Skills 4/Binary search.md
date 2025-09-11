## Descripción 
Want to play a game? As you use more of the shell, you might be interested in how they work! Binary search is a classic algorithm used to quickly find an item in a sorted list. Can you find the flag? You'll have 1000 possibilities and only 10 guesses.Cyber security often has a huge amount of data to look through - from logs, vulnerability reports, and forensics. Practicing the fundamentals manually might help you in the future when you have to write your own tools!You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_atlas/19/challenge.zip)

Additional details will be available after launching your challenge instance.
## Hints
1. Have you ever played hot or cold? Binary search is a bit like that.
2. You have a very limited number of guesses. Try larger jumps between numbers!
3. The program will randomly choose a new number each time you connect. You can always try again, but you should start your binary search over from the beginning - try around 500. Can you think of why?
## Solución
```
DanielMtzC-picoctf@webshell:~$ ls
README.txt  challenge.zip  home
DanielMtzC-picoctf@webshell:~$ cd home/
DanielMtzC-picoctf@webshell:~/home$ ls
ctf-player
DanielMtzC-picoctf@webshell:~/home$ cd ctf-player/drop-in/
DanielMtzC-picoctf@webshell:~/home/ctf-player/drop-in$ ls
guessing_game.sh
DanielMtzC-picoctf@webshell:~/home/ctf-player/drop-in$ cat guessing_game.sh 

            #!/bin/bash

            # Generate a random number between 1 and 1000
            target=$(( (RANDOM % 1000) + 1 ))

            echo "Welcome to the Binary Search Game!"
            echo "I'm thinking of a number between 1 and 1000."

            # Trap signals to prevent exiting
            trap 'echo "Exiting is not allowed."' INT
            trap '' SIGQUIT
            trap '' SIGTSTP

            # Limit the player to 10 guesses
            MAX_GUESSES=10
            guess_count=0

            while (( guess_count < MAX_GUESSES )); do
                read -p "Enter your guess: " guess

                if ! [[ "$guess" =~ ^[0-9]+$ ]]; then
                    echo "Please enter a valid number."
                    continue
                fi

                (( guess_count++ ))

                if (( guess < target )); then
                    echo "Higher! Try again."
                elif (( guess > target )); then
                    echo "Lower! Try again."
                else
                    echo "Congratulations! You guessed the correct number: $target"

                    # Retrieve the flag from the metadata file
                    flag=$(cat /challenge/metadata.json | jq -r '.flag')
                    echo "Here's your flag: $flag"
                    exit 0  # Exit with success code
                fi
            done

            # Player has exceeded maximum guesses
            echo "Sorry, you've exceeded the maximum number of guesses."
            exit 1  # Exit with error code to close the connection

            DanielMtzC-picoctf@webshell:~/home/ctf-player/drop-in$ nano guessing_game.sh 
DanielMtzC-picoctf@webshell:~/home/ctf-player/drop-in$ ssh -p 60527 ctf-player@atlas.picoctf.net
ctf-player@atlas.picoctf.net's password: 
Permission denied, please try again.
ctf-player@atlas.picoctf.net's password: 
Connection closed by 18.217.83.136 port 60527
DanielMtzC-picoctf@webshell:~/home/ctf-player/drop-in$ ssh -p 60374 ctf-player@atlas.picoctf.net
The authenticity of host '[atlas.picoctf.net]:60374 ([18.217.83.136]:60374)' can't be established.
ED25519 key fingerprint is SHA256:M8hXanE8l/Yzfs8iuxNsuFL4vCzCKEIlM/3hpO13tfQ.
This host key is known by the following other names/addresses:
    ~/.ssh/known_hosts:7: [hashed name]
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[atlas.picoctf.net]:60374' (ED25519) to the list of known hosts.
ctf-player@atlas.picoctf.net's password: 
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess: 500
Lower! Try again.
Enter your guess: 300
Lower! Try again.
Enter your guess: 100
Congratulations! You guessed the correct number: 100
Here's your flag: picoCTF{g00d_gu355_1597707f}
Connection to atlas.picoctf.net closed.
```
## Notas

## Referencias
