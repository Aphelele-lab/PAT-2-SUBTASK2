# PAT-2-SUBTASK2
PAT 2 SUBTASK2
// Online C++ compiler to run C++ program online
#include <iostream>
#include <string>
#include <unordered_map>
#include <cctype>
using namespace std;
int main() {
    // Morse code for A-Z only
    unordered_map<char, string> morse = {
        {'A', ".-"}, {'B', "-..."}, {'C', "-.-."}, {'D', "-.."}, {'E', "."},
        {'F', "..-."}, {'G', "--."}, {'H', "...."}, {'I', ".."}, {'J', ".---"},
        {'K', "-.-"}, {'L', ".-.."}, {'M', "--"}, {'N', "-."}, {'O', "---"},
        {'P', ".--."}, {'Q', "--.-"}, {'R', ".-."}, {'S', "..."}, {'T', "-"},
        {'U', "..-"}, {'V', "...-"}, {'W', ".--"}, {'X', "-..-"}, {'Y', "-.--"},
        {'Z', "--.."}
    };
 string message;
    cout << "Enter a message in English (A-Z characters only): ";
    getline(cin, message);

    string fullMorse = "";

    cout << endl;
    for (char c : message) {
        if (c == ' ') {
            fullMorse += " "; // 3 spaces between words
            continue;
        }
    char upperC = toupper(c);
        // Only process A-Z, ignore numbers and symbols
        if (isalpha(upperC) && morse.find(upperC)!= morse.end()) {
            string code = morse[upperC];
            cout << upperC << ": " << code << endl;
            fullMorse += code + " "; // 3 spaces between letters
        }
    }
