### Binary Search

Want to play a game? As you use more of the shell, you might be interested in how they work! Binary search is a classic algorithm used to quickly find an item in a sorted list. Can you find the flag? You'll have 1000 possibilities and only 10 guesses.Cyber security often has a huge amount of data to look through - from logs, vulnerability reports, and forensics. Practicing the fundamentals manually might help you in the future when you have to write your own tools!You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_atlas/17/challenge.zip)

`ssh -p 58718 ctf-player@atlas.picoctf.net`Using the password `f3b61b38`. Accept the fingerprint with `yes`, and `ls` once connected to begin. Remember, in a shell, passwords are hidden!
### Solución 1 - Dividiendo cada rango a la mitad


```
daniel_minbot-picoctf@webshell:~/home/ctf-player/drop-in$ ssh -p 58718 ctf-player@atlas.picoctf.net
ctf-player@atlas.picoctf.net's password: 
Permission denied, please try again.
ctf-player@atlas.picoctf.net's password: 
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess: 500
Higher! Try again.
Enter your guess: 750
Higher! Try again.
Enter your guess: 875
Lower! Try again.
Enter your guess: 800
Lower! Try again.
Enter your guess: 775
Lower! Try again.
Enter your guess: 762
Lower! Try again.
Enter your guess: 760
Lower! Try again.
Enter your guess: 755
Lower! Try again.
Enter your guess: 752
Lower! Try again.
Enter your guess: 751
Congratulations! You guessed the correct number: 751
Here's your flag: picoCTF{g00d_gu355_6dcfb67c}

```

picoCTF{g00d_gu355_6dcfb67c}

### Notas
Se realizo ingresando la la mitad de cada rango numerico