#include <iostream>
#include <vector>
using namespace std;

// INVENTORY DATA
vector<string> resistors = {
"1 ohm","1.2 ohm","1.5 ohm","1.8 ohm","2.2 ohm","2.7 ohm",
"3.3 ohm","3.9 ohm","4.7 ohm","5.6 ohm","6.8 ohm","8.2 ohm",
"10 ohm","12 ohm","15 ohm","18 ohm","22 ohm","27 ohm",
"33 ohm","39 ohm","47 ohm","56 ohm","68 ohm","82 ohm",
"100 ohm","120 ohm","150 ohm","180 ohm","200 ohm","220 ohm",
"270 ohm","300 ohm","330 ohm","390 ohm","470 ohm","560 ohm",
"620 ohm","680 ohm","820 ohm","1k ohm","1.2k ohm","1.5k ohm",
"1.8k ohm","2.2k ohm","2.7k ohm","3.3k ohm","3.9k ohm","4.7k ohm",
"5.6k ohm","6.8k ohm","8.2k ohm","10k ohm","12k ohm","15k ohm",
"18k ohm","22k ohm","27k ohm","33k ohm","39k ohm","47k ohm",
"56k ohm","68k ohm","75k ohm","82k ohm","100k ohm","120k ohm",
"150k ohm","180k ohm","220k ohm","270k ohm","330k ohm","390k ohm",
"470k ohm","560k ohm","680k ohm","820k ohm","1M ohm","22M ohm"
};

vector<int> Rstock = {
64,98,98,100,82,100,87,90,98,91,93,81,59,95,83,87,
91,82,261,79,143,23,81,75,24,18,519,450,31,26,459,
214,595,23,357,359,266,26,35,43,390,62,255,353,291,
306,103,428,275,225,194,223,64,71,1,279,350,87,118,
92,295,93,86,114,82,253,92,169,90,75,90,386,75,216,
94,103,92,92
};

// HENRYS
vector<string> henrys = {
"10 uH","22uH","47uH","220uH","1 mH","2.2 mH",
"4.7 mH","10 mH","22 mH","33 mH","47 mH","100 mH"
};

vector<int> Hstock = {
81,88,90,60,48,42,45,33,64,50,59,76
};

// BATTERIES
vector<string> batteries = {
"9 V","1.5 V"
};

vector<int> Bstock = {
6,3
};

// BREADBOARD
vector<string> breadboard = {
"bread board"
};

vector<int> BRstock = {
16
};

// POTENTIOMETERS
vector<string> pot = {
"1k ohm pot","5k ohm pot","50k ohm pot",
"100k ohm pot","1M ohm pot","2M ohm pot"
};

vector<int> Pstock = {
1,6,1,11,1,1
};

// CAPACITORS
vector<string> capacitors = {
"474K Radial","105K Radial","102K Radial","224K Radial",
"104K Radial","473K Radial","103K Radial","101K Radial",".1 J Radial",
".47 Micro F","1 Micro F","220 Micro F","4.7 Micro F Ax",
"4.7 Micro F","330 Micro F","470 Micro F","22 Micro F",
"10 Micro F","4700 Micro F","47 Micro F","1000 Micro F",
"2200 Micro F","100 Micro F Ax","33 Micro F","100 Micro F"
};

vector<int> Cstock = {
25,91,149,7,2,14,14,2,2,379,203,
17,111,253,0,47,946,700,0,481,
31,38,2,308,271
};

// IC CHIPS
vector<string> icChips = {
"7409","4001","4017","4029","74157","9526","7420",
"74595","7719","4511","9525","74151","74193","4011",
"7488","7489","7402","7411","7409","7490","9226",
"7414","7400","7408","7402","74147","74037","7432",
"7486","7451","MH7489","7932","7485","74138","7474",
"74154","74125","74190","7430","74191","74107","74192",
"74148","7495","7447","7442","74121","7475","74163",
"74150","74164"
};

vector<int> ICstock = {
7,5,8,2,3,3,2,1,4,2,5,1,2,8,1,26,89,84,7,9,3,
146,77,4,9,14,28,42,89,27,197,75,70,33,47,84,
25,42,74,74,56,283,64,69,30,3,51,47,22,30,136
};

// BUTTONS & SWITCHES
vector<string> BandS = {
"button","8 prong","4 prong","3 prong","2 prong"
};

vector<int> BSstock = {
4,1,2,10,1
};

// DISPLAY INVENTORY
void show(vector<string>& items, vector<int>& stock) {

    cout << "\n=====================================\n";
    cout << "        CURRENT INVENTORY\n";
    cout << "=====================================\n";

    for (int i = 0; i < items.size(); i++) {

        cout << "[" << i + 1 << "] "
             << items[i]
             << " ---> Stock: "
             << stock[i]
             << endl;
    }

    cout << "=====================================\n";
}

// ADD STOCK TO ITEM
void add(vector<int>& stock) {

    int item, amount;

    cout << "\n++++++++++ ADD STOCK ++++++++++\n";

    cout << "Enter Item #: ";
    cin >> item;

    cout << "Enter Amount To Add: ";
    cin >> amount;

    stock[item - 1] += amount;

    cout << "\n>>> STOCK UPDATED SUCCESSFULLY <<<\n";
}

// REMOVE STOCK FROM ITEM
void remove(vector<int>& stock) {

    int item, amount;

    cout << "\n---------- REMOVE STOCK ----------\n";

    cout << "Enter Item #: ";
    cin >> item;

    cout << "Enter Amount To Remove: ";
    cin >> amount;

    // CHECK IF ENOUGH STOCK EXISTS
    if (amount <= stock[item - 1]) {

        stock[item - 1] -= amount;

        cout << "\n>>> STOCK UPDATED SUCCESSFULLY <<<\n";
    }

    else {

        cout << "\n!!! NOT ENOUGH STOCK AVAILABLE !!!\n";
    }
}

int main() {

    int choice, category;

    do {

        // MAIN MENU
        cout << "\n";
        cout << "#####################################\n";
        cout << "#     ELECTRONICS INVENTORY SYS    #\n";
        cout << "#####################################\n";

        cout << "\n[1] VIEW INVENTORY";
        cout << "\n[2] ADD STOCK";
        cout << "\n[3] REMOVE STOCK";
        cout << "\n[4] EXIT PROGRAM";

        cout << "\n\nSelect Option --> ";
        cin >> choice;

        // EXIT PROGRAM
        if (choice == 4) {

            cout << "\n=====================================\n";
            cout << "     THANK YOU FOR USING SYSTEM\n";
            cout << "=====================================\n";

            break;
        }

        // CATEGORY MENU
        cout << "\n=====================================\n";
        cout << "           SELECT CATEGORY\n";
        cout << "=====================================\n";

        cout << "[1] Resistors\n";
        cout << "[2] Henrys\n";
        cout << "[3] Batteries\n";
        cout << "[4] Breadboard\n";
        cout << "[5] Potentiometers\n";
        cout << "[6] Capacitors\n";
        cout << "[7] IC Chips\n";
        cout << "[8] Buttons\n";

        cout << "\nChoose Category --> ";
        cin >> category;

        // HANDLE RESISTORS
        if (category == 1) {
            show(resistors, Rstock);

            if (choice == 2) add(Rstock);
            if (choice == 3) remove(Rstock);
        }

        // HANDLE Henrys
        else if (category == 2) {
            show(henrys, Hstock);

            if (choice == 2) add(Hstock);
            if (choice == 3) remove(Hstock);
        }

        // HANDLE BATTERIES
        else if (category == 3) {
            show(batteries, Bstock);

            if (choice == 2) add(Bstock);
            if (choice == 3) remove(Bstock);
        }

        // HANDLE BREADBOARD
        else if (category == 4) {
            show(breadboard, BRstock);

            if (choice == 2) add(BRstock);
            if (choice == 3) remove(BRstock);
        }

        // HANDLE POTENTIOMETERS
        else if (category == 5) {
            show(pot, Pstock);

            if (choice == 2) add(Pstock);
            if (choice == 3) remove(Pstock);
        }

        // HANDLE CAPACITORS
        else if (category == 6) {
            show(capacitors, Cstock);

            if (choice == 2) add(Cstock);
            if (choice == 3) remove(Cstock);
        }

        // HANDLE IC CHIPS
        else if (category == 7) {
            show(icChips, ICstock);

            if (choice == 2) add(ICstock);
            if (choice == 3) remove(ICstock);
        }

        // HANDLE BUTTONS
        else if (category == 8) {
            show(BandS, BSstock);

            if (choice == 2) add(BSstock);
            if (choice == 3) remove(BSstock);
        }

    } while (choice != 4);

    return 0;
}
