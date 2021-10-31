# git_test
// usually remember that 'g' => refere to get (read) but 'p' => refere to put (write)
 // read & write at the same time with one object (F)
    fstream F;   
    // opening a file in input and output mode
    F.open("my.txt", ios::in | ios::out);
    
    // getting current location{ tellg() function} 
    cout << F.tellg() << endl;
    
    // seeking 8 bytes/characters{seekg() function ,beg ==> beginning= start point}
 // يعني عد 8 حروف من البداية وحط السهم بمعنى ان البوينتر لما يبدأيقرأ هيبدأ من الحرف التاسع
    F.seekg(8, ios::beg);
    // now, getting the current location
    cout << F.tellg() << endl;
    // extracting one character from current location
    char c = F.get();
    // printing the character
    cout << c << endl;
    
    // after getting the character,
    // getting current location
    cout << F.tellg() << endl;
    // now, seeking 10 more bytes/characters
    F.seekg(10, ios::cur);
    // now, getting current location
    cout << F.tellg() << endl;
    // again, extracing the one character from current location
    c = F.get();
    // printing the character
    cout << c << endl;
    
    // after getting the character,
    // getting current location
    cout << F.tellg() << endl;
    // again, seeking 7 bytes/characters from beginning 
    F.seekp(7, ios::beg);
    // writting a character 'Z' at current location
    F.put('Z');
    // now, seeking back 7 bytes/characters from the end
    F.seekg(-7, ios::end);
    // now, printing the current location
    cout << "End:" << F.tellg() << endl;
    // extracting one character from current location
    c = F.get();
    // printing the character
    cout << c << endl;
    
    // closing the file
    F.close();
