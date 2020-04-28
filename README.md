# Cipher
This code is used to explain ciphers. In this you can convert a given text to hidden format that follows a particular pattern.






import string
dict={}
data=""
file=open
for i in range(len(string.ascii_letters)):
    dict[string.ascii_letters[i]]=string.ascii_letters[i-1]
print(dict) 
with open("cipher.txt") as f:     # Here cipher.txt is a text file that contains the message that i want to encrypt.
    while True:
        c=f.read(1)      # This reads the characters in the text file one by one.
        if not c:
            print("End of File")
            break;
        if c in dict:
            data=dict[c]
        else:
            data=c   
        print(data)    
            
