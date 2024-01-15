#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include "project1.1.c"
#include "blockchainBaseConcept.c"

// #include <stdio.h>
// #include <stdlib.h>
// #include <string.h>

// Function declarations
void signUp();
int login();


    
// Function to sign up a new user
void signUp() {
    char username[50], password[50];

    printf("\nEnter a username: ");
    scanf("%s", username);

    printf("Enter a password: ");
    scanf("%s", password);

    // Append user details to the file
    FILE *file = fopen("users.txt", "a");
    if (file == NULL) {
        printf("\nError opening file.\n");
        exit(1);
    }

    fprintf(file, "%s %s\n", username, password);
    fclose(file);
}

// Function to perform user login
int login() {
    char username[50], password[50];
    int found = 0;

    printf("\nEnter your username: ");
    scanf("%s", username);

    printf("Enter your password: ");
    scanf("%s", password);

    // Check if user credentials exist in the file
    FILE *file = fopen("users.txt", "r");
    if (file == NULL) {
        printf("\nError opening file.\n");
        exit(1);
    }

    char storedUsername[50], storedPassword[50];
    while (fscanf(file, "%s %s", storedUsername, storedPassword) != EOF) {
        if (strcmp(username, storedUsername) == 0 && strcmp(password, storedPassword) == 0) {
            found = 1;
            break;
        }
    }

    fclose(file);

    return found;
}


int main() {
    char web[50];
    int press,option;
    char again;
    printf("  *******         *****          *****           *******       *          ******\n");
    printf(" *              *       *      *       *       *               *         *\n");
    printf(" *             *         *    *         *      *               *         *\n");
    printf(" *     ***     *         *    *         *      *      ***      *         *******\n");
    printf(" *       *     *         *    *         *      *        *      *         *\n");
    printf(" *       *      *       *      *       *       *        *      *         *\n");
    printf("  *******         *****          *****           *******        ******    *******\n\n");

    printf("WEBSITE: www.iam.com\n\n");
    printf("\n\nEnter the website URL :| ");
    scanf("%s", web);
  
    if (strstr(web, "www.iam.com") != NULL) {
        printf("\n\nCorrect URL");
        printf("\n\n********* Welcome to IAM *********");
        int choice;

    do {
        printf("\n************* Welcome *************\n");
        printf("1. Login\n");
        printf("2. Sign Up\n");
        printf("3. Exit\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);

        switch (choice) {
            case 1:
                if (login()) {
                    printf("\nLogin successful!\n");
                    op();
                } else {
                    printf("\nLogin failed. Invalid credentials.\n");
                }
                break;
            case 2:
                signUp();
                printf("\nSign up successful! You can now log in.\n");
                op();
                break;
            case 3:
                printf("\nExiting program.\n");
                exit(0);
            default:
                printf("\nInvalid choice. Please enter a valid option.\n");
        }

    } while (1);

    return 0;
}
}
#include <stdio.h>
#include <string.h>
#include <stdlib.h>
#include <time.h>

void delay(int milliseconds) {
    for (int i = 0; i < milliseconds * 10000; i++) {
        // Adjust the loop condition and the multiplication factor as needed
    }
}

void printWithDelay(const char *text) {
    for (int i = 0; text[i] != '\0'; i++) {
        printf("%c", text[i]);
        fflush(stdout);
        delay(500); // Adjust the delay duration as needed

        if (text[i] == ' ') {
            printf(" ");
            fflush(stdout);
            delay(250);
        }
    }
}

void riddle1(const char *text)
{
    for (int i = 0; text[i] != '\0'; i++)
    {
        printf("%c", text[i]);
        fflush(stdout);
        delay(5000); // Adjust the delay duration as needed

        if (text[i] == ' ') {
            printf(" ");
            fflush(stdout);
            delay(2500);}
    }
    
}


void code(const char *text)
{
    for (int i = 0; text[i] != '\0'; i++)
    {
        printf("%c", text[i]);
        fflush(stdout);
        delay(5000); // Adjust the delay duration as needed

        if (text[i] == ' ') {
            printf(" ");
            fflush(stdout);
            delay(2500);}
    }
    
}

void msg(const char *text)
{
       for (int i = 0; text[i] != '\0'; i++)
    {
        printf("%c", text[i]);
        fflush(stdout);
        delay(5000); // Adjust the delay duration as needed

        if (text[i] == ' ') {
            printf(" ");
            fflush(stdout);
            delay(2500);}
    }
}


void decrypted() {

    // printf("Decrypted function executed.\n");
 char message1[]="Kqfsp kwtr ymj wjfw tk ymj gfxj";
    
    int key=5;
    for (int i = 0; i < strlen(message1); i++) {
        if (message1[i] >= 'A' && message1[i] <= 'Z') {
            message1[i] = (message1[i] - 'A' - key + 26) % 26 + 'A';
        } else if (message1[i] >= 'a' && message1[i] <= 'z') {
            message1[i] = (message1[i] - 'a' - key + 26) % 26 + 'a';
        }
    }

       printf("Decrypted Code\n\n\n");
       printf("\n");
       msg(message1);


}

void decrypted1() {

    // printf("Decrypted function executed.\n");
 char message1[]="Lmtbi, bpqa qa Mkpw. Qvqbqibqvo uwdm bw PY ivl izug jiam. Wdmz";
    
    int key=8;
    for (int i = 0; i < strlen(message1); i++) {
        if (message1[i] >= 'A' && message1[i] <= 'Z') {
            message1[i] = (message1[i] - 'A' - key + 26) % 26 + 'A';
        } else if (message1[i] >= 'a' && message1[i] <= 'z') {
            message1[i] = (message1[i] - 'a' - key + 26) % 26 + 'a';
        }
    }

       printf("Decrypted Code\n\n\n");
       printf("\n");
       msg(message1);


}

void decrypted2() {

    // printf("Decrypted function executed.\n");
 char message1[]="qpsu dbnfsbt, up uif mfgu xjoh";
    
    int key=1;
    for (int i = 0; i < strlen(message1); i++) {
        if (message1[i] >= 'A' && message1[i] <= 'Z') {
            message1[i] = (message1[i] - 'A' - key + 26) % 26 + 'A';
        } else if (message1[i] >= 'a' && message1[i] <= 'z') {
            message1[i] = (message1[i] - 'a' - key + 26) % 26 + 'a';
        }
    }

       printf("Decrypted Code\n\n\n");
       printf("\n");
       msg(message1);


}

void decrypted3() {

    // printf("Decrypted function executed.\n");
 char message1[]="Klsah ylhjolk ha aol thyr code";
    
    int key=7;
    for (int i = 0; i < strlen(message1); i++) {
        if (message1[i] >= 'A' && message1[i] <= 'Z') {
            message1[i] = (message1[i] - 'A' - key + 26) % 26 + 'A';
        } else if (message1[i] >= 'a' && message1[i] <= 'z') {
            message1[i] = (message1[i] - 'a' - key + 26) % 26 + 'a';
        }
    }

       printf("Decrypted Code\n\n\n");
       printf("\n");
       msg(message1);


}

void decrypted4() {

    // printf("Decrypted function executed.\n");
 char message1[]="mnuncrwp rbajnu";
    
    int key=9;
    for (int i = 0; i < strlen(message1); i++) {
        if (message1[i] >= 'A' && message1[i] <= 'Z') {
            message1[i] = (message1[i] - 'A' - key + 26) % 26 + 'A';
        } else if (message1[i] >= 'a' && message1[i] <= 'z') {
            message1[i] = (message1[i] - 'a' - key + 26) % 26 + 'a';
        }
    }

       printf("Decrypted Code\n\n\n");
       printf("\n");
       msg(message1);


}


void condition() {
    int max_attempts = 3;
    int key = 0;
    int enter;
        printf("\n\nThis Riddle will Locate the Location of Israeli Gun Marks\n\n");

    for (int attempt = 1; attempt <= max_attempts; ++attempt) {
        char riddle[100];

        printf("\nBreak the Clue\n\n");
        printf("Attempt %d of %d\n", attempt, max_attempts);
        printf("Enter the answer: \n\n");
        scanf("%99s", riddle);  // Limit the input to 99 characters to avoid buffer overflow

        if (strcmp(riddle, "militarybase") == 0) {
            key = 5;
            printf("%c Key=%d\n\n", 251, key);

            printf("Enter the key to decrypt: \n");

            while (1) {
                if (scanf("%d", &enter) == 1) {
                    // Consume the newline character in the input buffer
                    while (getchar() != '\n');

                    if (enter == key) {
                        decrypted();
                        printf("\nGood Job.. You navigated Hamas to the military base\n");
                        return;  // Exit the function after successful decryption
                    } else {
                        printf("Error\nEnter the correct key to decrypt: \n");
                    }
                } else {
                    printf("Invalid input. Please enter a valid key: \n");
                    while (getchar() != '\n');  // Clear the input buffer
                }
            }
        } else {
            printf("Incorrect answer. Try again.\n");
        }
    }

    printf("You've exhausted all attempts. The location remains hidden.\n");
    printf("\n\nYou Lost\n\n");
}

void condition1() {
    int max_attempts = 3;
    int key = 0;
    int enter;
    printf("\n\nThis will indicate the enemy having which equipment\n");
    for (int attempt = 1; attempt <= max_attempts; ++attempt) {
        char riddle[100];

        printf("\nBreak the Clue\n\n");
        printf("Attempt %d of %d\n", attempt, max_attempts);
        printf("Enter the answer: \n\n");
        scanf("%99s", riddle);  // Limit the input to 99 characters to avoid buffer overflow

        if (strcmp(riddle, "sniper") == 0) {
            key = 8;
            printf("%c Key=%d\n\n", 251, key);

            printf("Enter the key to decrypt: \n");

            while (1) {
                if (scanf("%d", &enter) == 1) {
                    // Consume the newline character in the input buffer
                    while (getchar() != '\n');

                    if (enter == key) {
                        decrypted1();
                        printf("\nExcellent.. You help Hamas to conqured the sniper tower \n");
                        return;  // Exit the function after successful decryption
                    } else {
                        printf("Error\nEnter the correct key to decrypt: \n");
                    }
                } else {
                    printf("Invalid input. Please enter a valid key: \n");
                    while (getchar() != '\n');  // Clear the input buffer
                }
            }
        } else {
            printf("Incorrect answer. Try again.\n");
        }
    }

    printf("You've exhausted all attempts. The Hamas was imprisoned.\n");
    printf("\n\nYou Lost\n\n");
}


void condition2() {
    int max_attempts = 3;
    int key = 0;
    int enter;
    printf("\n\nThis key will Help Hamas to hacked the cameras\n");
    for (int attempt = 1; attempt <= max_attempts; ++attempt) {
        char riddle[100];

        printf("\nBreak the Clue\n\n");
        printf("Attempt %d of %d\n", attempt, max_attempts);
        printf("Enter the answer: \n\n");
        scanf("%99s", riddle);  // Limit the input to 99 characters to avoid buffer overflow

        if (strcmp(riddle, "binarycode") == 0) {
            key = 1;
            printf("%c Key=%d\n\n", 251, key);

            printf("Enter the key to decrypt: \n");

            while (1) {
                if (scanf("%d", &enter) == 1) {
                    // Consume the newline character in the input buffer
                    while (getchar() != '\n');

                    if (enter == key) {
                        decrypted2();
                        printf("\nMarvelous.. You help Hamas to hack the Israeli base cameras \n");
                        return;  // Exit the function after successful decryption
                    } else {
                        printf("Error\nEnter the correct key to decrypt: \n");
                    }
                } else {
                    printf("Invalid input. Please enter a valid key: \n");
                    while (getchar() != '\n');  // Clear the input buffer
                }
            }
        } else {
            printf("Incorrect answer. Try again.\n");
        }
    }

    printf("You've exhausted all attempts. The Hamas location was traced.\n");
    printf("\n\nYou Lost\n\n");
}
//Klsah ylhjolk ha aol thyr code

void condition3() {
    int max_attempts = 3;
    int key = 0;
    int enter;
    printf("\n\nThis key will Help Hamas to call their troops\n");
    for (int attempt = 1; attempt <= max_attempts; ++attempt) {
        char riddle[100];

        printf("\nBreak the Clue\n\n");
        printf("Attempt %d of %d\n", attempt, max_attempts);
        printf("Enter the answer: \n\n");
        scanf("%99s", riddle);  // Limit the input to 99 characters to avoid buffer overflow

        if (strcmp(riddle, "telepathy") == 0) {
            key = 7;
            printf("%c Key=%d\n\n", 251, key);

            printf("Enter the key to decrypt: \n");

            while (1) {
                if (scanf("%d", &enter) == 1) {
                    // Consume the newline character in the input buffer
                    while (getchar() != '\n');

                    if (enter == key) {
                        decrypted3();
                        printf("\nSuperb.. You help Hamas to call their troops \n");
                        return;  // Exit the function after successful decryption
                    } else {
                        printf("Error\nEnter the correct key to decrypt: \n");
                    }
                } else {
                    printf("Invalid input. Please enter a valid key: \n");
                    while (getchar() != '\n');  // Clear the input buffer
                }
            }
        } else {
            printf("Incorrect answer. Try again.\n");
        }
    }

    printf("You've exhausted all attempts. The Hamas troops was imprisoned by the enemies.\n");
    printf("\n\nYou Lost\n\n");
}

void condition4() {


    int max_attempts = 3;
    int key = 0;
    int enter;
    printf("\n\nThis key will Help Hamas to conquere\n");
    for (int attempt = 1; attempt <= max_attempts; ++attempt) {
        char riddle[100];

        printf("\nBreak the Clue\n\n");
        printf("Attempt %d of %d\n", attempt, max_attempts);
        printf("Enter the answer: \n\n");
        scanf("%99s", riddle);  // Limit the input to 99 characters to avoid buffer overflow

        if (strcmp(riddle, "time") == 0) {
            key = 9;
            printf("%c Key=%d\n\n", 251, key);

            printf("Enter the key to decrypt: \n");

            while (1) {
                if (scanf("%d", &enter) == 1) {
                    // Consume the newline character in the input buffer
                    while (getchar() != '\n');

                    if (enter == key) {
                        decrypted4();
                        printf("\nRemarkable.. You help Hamas to conquered the Israel \n");
                        printf("\n\nHistory has been created \n\n");
                        printf("\n\nCongratulations The Adiministrator is greatly pleased to the user, as hammas is helped by the user to conquer the Israel.\n\n");
                        return;  // Exit the function after successful decryption
                    } else {
                        printf("Error\nEnter the correct key to decrypt: \n");
                    }
                } else {
                    printf("Invalid input. Please enter a valid key: \n");
                    while (getchar() != '\n');  // Clear the input buffer
                }
            }
        } else {
            printf("Incorrect answer. Try again.\n");
        }
    }

    printf("You've exhausted all attempts. America Interupt the war and imprisoned Hamas .\n");
    printf("\n\nYou Lost\n\n");
}


void op() {
    int option, enter,a;
    int level;
    char again;
    int count = 4, key = 5; // Set the correct key value

    // 
    char Story[] = "Surviving a 2000 Israeli attack on his Palestinian family, Abdul was adopted by Israelis and joined their army. In 2023, driven by a thirst for revenge, he assisted Hamas by revealing a concealed entry point into Israel through encrypted codes. Abdul's choice highlights the intricate interplay between personal history and geopolitical tensions, emphasizing the need for nuanced approaches to conflict resolution and understanding the complex emotions involved..... Now you are abdul and you have to help Hammas.";
    char Story2[]= "When the boy Abdul succeed to enter the hammas militry force to israel, then he start to work on giving access of israeli's militry base to hammas forces, by entering them to rare phase of israil's sniper tower base, to be conquered by the hammas militry forces by giving them a encrypted key to access the sniper base. ";
    char Story3[]= " Abdul did so just to attack the israeli's, by doing so he wants to give full access of sniper base to hammas forces, by hacking their cameras, weapons, radars, and base devices by the professionalised hackers. Then Abdul give them command to hack the cameras of the base. ";
    char Story4[]= "Now after accessing control over the cameras Abdul guide them that, from where the Hammas forces have to enter to attack the Israeli's forces, as Abdul helps Hammas forces to guide their troops from where they have to enter the base ";
    char Story5[]= "At the conclusion, Hammas gain control over isreal and conquer it. Abdul suceed in taking the revenge of his parents and raise the flag of palestine in Israel.";
    //story end
    //riddle start
    char riddle[]="Beneath camouflage, secrets unfold, where discipline and courage are untold";
    char riddle2[]="A silent guardian in the shadows of green, where camouflage conceals the unseen. What am I?";
    char riddle3[]="Crack the digital fortress, where 101010 meets secrets untold";
    char riddle4[]="In silence I speak, unheard but felt, signaling across realms with a presence unfelt.";
    char riddle5[]="In shadows I rose, conquered realms unseen, my triumph whispered in the echoes of what might have been.";
    //riddle ends encrypted code start
    char code1[]="The encrypted code is 'Kqfsp kwtr ymj wjfw tk ymj gfxj'";
    char code2[]="The encrypted code is ' Lmtbi, bpqa qa Mkpw. Qvqbqibqvo uwdm bw PY ivl izug jiam. Wdmz' ";
    char code3[]="The encrypted code is 'qpsu dbnfsbt, up uif mfgu xjoh' ";
    char code4[]="The encrypted code is 'Klsah ylhjolk ha aol thyr' ";
    char code5[]="The encrypted code is 'mnuncrwp rbajnu' ";
   
    printf("\nWelcome\n");
    printf("\nHere are two exciting games for\n1- QuantumQuest (Encryption)\n2- EpicBlock Quest (Blockchain Basic)\n\n");
    scanf("%d", &option);

    switch (option) {
        case 1:
            printf("Story--\n");

            printWithDelay(Story);
            printf("\n");
            printf("\n\nFor the decryption, you have to find a key by resolving riddles, and you have only 3 tries\n\n");
            // printf("\n");
            printf("\n\n");
            code(code1);
            printf("\n\nClue\n\n");
            riddle1(riddle);
            condition();

            printf("\nLevel 1 Compelete\n");
            printf("\nPress 2 for Level 2\n");
            scanf("%d",&level);
            if (level==2)
            {
                printf("forward on--");

            printWithDelay(Story2);
            printf("\n");
            printf("\n\nFor the decryption, you have to find a key by resolving riddles, and you have only 3 tries\n\n");
            printf("\n");
            code(code2);
            printf("\n\nClue\n\n");
            riddle1(riddle2);
            condition1();
            }
            
            printf("\nLevel 2 Compeleted\n");
            printf("\nPress 3 for Level 3\n");
            scanf("%d",&level);

           if (level==3)
            {
            printf("forward on--");
            printWithDelay(Story3);
            printf("\n");
            printf("\n\nFor the decryption, you have to find a key by resolving riddles, and you have only 3 tries\n\n");
            printf("\n");
            code(code3);
            printf("\n\nClue\n\n");
            riddle1(riddle3);
            condition2();
            }
            printf("\nLevel 3 Compeleted\n");
            printf("\nPress 4 for Level 4\n");
            scanf("%d",&level);

            if (level==4)
            {
            printf("forward on--");
            printWithDelay(Story4);
            printf("\n");
            printf("\n\nFor the decryption, you have to find a key by resolving riddles, and you have only 3 tries\n\n");
            printf("\n");
            code(code4);
            printf("\n\nClue\n\n");
            riddle1(riddle4);
            condition3();
            }
            printf("\nLevel 4 Compeleted\n");
            printf("\nPress 5 for Level 5\n");
            scanf("%d",&level);

             if (level==5)
            {
            printf("forward on--");
            printWithDelay(Story5);
            printf("\n");
            printf("\n\nFor the decryption, you have to find a key by resolving riddles, and you have only 3 tries\n\n");
            printf("\n");
            code(code5);
            printf("\n\nClue\n\n");
            riddle1(riddle5);
            condition4();
            }
            break;

            case 2:
            block();
            break;
}
}
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <time.h>

// Yahan ek structure define kia gaya hai jo transaction ko represent karega.
typedef struct {
    char sender[50];
    char receiver[50];
    double amount;
} Transaction;

// Yahan ek structure define kia gaya hai jo block ko represent karega.
typedef struct {
    int index;
    time_t timestamp;
    Transaction data;
    char previousHash[65];
    char hash[65];
} Block;

// Yahan block ka hash calculate karne ka function hai.
void calculateHash(Block *block, char *hashOutput) {
    // Block ki information ko concatenate karnay ke liye ek string banao.
    char input[150];
    snprintf(input, sizeof(input), "%d%ld%s%s%lf", block->index, block->timestamp, block->data.sender, block->data.receiver, block->data.amount);

    // Simple hash function use karo (demonstration ke liye).
    unsigned long hash = 5381;
    int i = 0;

    while (input[i] != '\0') {
        hash = ((hash << 5) + hash) + input[i++];
    }

    // Hexadecimal form mein hash ko string mein convert karo.
    snprintf(hashOutput, 65, "%lx", hash);
}

// Yahan ek naya block create karne ka function hai.
Block createBlock(int index, Transaction data, char *previousHash) {
    Block newBlock;

    // Block ki information set karo.
    newBlock.index = index;
    newBlock.timestamp = time(NULL);
    newBlock.data = data;
    strcpy(newBlock.previousHash, previousHash);

    // Block ka hash calculate karo.
    calculateHash(&newBlock, newBlock.hash);

    return newBlock;
}

// Yahan ek block ko blockchain mein add karne ka function hai.
void addBlock(Block newBlock, Block *blockchain, int *blockchainSize) {
    blockchain[*blockchainSize] = newBlock;
    (*blockchainSize)++;
}

// Yahan blockchain ko display karne ka function hai.
void displayBlockchain(Block *blockchain, int blockchainSize) {
    for (int i = 0; i < blockchainSize; ++i) {
        printf("\nBlock #%d\n", blockchain[i].index);
        printf("Timestamp: %s", asctime(localtime(&blockchain[i].timestamp)));
        printf("Sender: %s\n", blockchain[i].data.sender);
        printf("Receiver: %s\n", blockchain[i].data.receiver);
        printf("Amount: %.2lf\n", blockchain[i].data.amount);
        printf("Previous Hash: %s\n", blockchain[i].previousHash);
        printf("Hash: %s\n", blockchain[i].hash);
        printf("---------------------------");
    }
    printf("\n");
}

// Yahan user se transaction input lene ka function hai.
Transaction getTransactionInput() {
    Transaction transaction;
    printf("Sender ka naam enter karein: ");
    scanf("%s", transaction.sender);
    printf("Receiver ka naam enter karein: ");
    scanf("%s", transaction.receiver);
    printf("Amount enter karein: ");
    scanf("%lf", &transaction.amount);

    return transaction;
}

int block() {
    // Blockchain ko initialize karo.
    Block blockchain[100];  // Assumed maximum of 100 blocks
    int blockchainSize = 0;

    int choice = -1;  // Initialize choice to a non-zero value to enter the loop

    while (choice != 0) {
        printf("\n1. Transaction add karein\n");
        printf("2. Blockchain display karein\n");
        printf("0. Exit\n");
        printf("Apna choice enter karein: ");
        scanf("%d", &choice);

        switch (choice) {
            case 1: {
                Transaction newTransaction = getTransactionInput();
                Block newBlock = createBlock(blockchainSize, newTransaction, blockchain[blockchainSize - 1].hash);
                addBlock(newBlock, blockchain, &blockchainSize);
                printf("Transaction blockchain mein add ho gayi hai.\n");
                break;
            }
            case 2:
                displayBlockchain(blockchain, blockchainSize);
                break;
            case 0:
                printf("Exiting...\n");
                break;
            default:
                printf("Invalid choice. Dobarah koshish karein.\n");
        }
    }

    return 0;
}

