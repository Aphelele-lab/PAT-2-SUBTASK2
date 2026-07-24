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
