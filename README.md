# Seconds-Converter
This will convert Days/Hours/Minutes to seconds
//Seconds Conversion
#include <iostream>
#include <string>

using namespace std;

int main()
{
    int sec;
    int minutes;
    int hours;
    int days;
    int leftSec;
    int leftMin;
    int leftHour;
    
    cout << "Please enter the number of seconds you would like to be converted" << endl;
    cin >> sec;
    cout << "Would you like to convert to minutes, hours or days?" << endl << "Please type 'm' 'h' or 'd' for conversion " << endl;
    char conversion;
    cin >> conversion;
    if ( conversion == 'm'){
        leftSec = sec % 60;
        minutes = sec / 60;
        cout << minutes << " minute(s) " << leftSec << " second(s)"<< endl;
    }
    else if (conversion == 'h'){
        leftMin = sec % 3600;
        minutes = leftMin / 60;
        leftSec = leftMin % 60;
        hours = sec / 3600;
        cout << hours << " hour(s) " << minutes << " minute(s) " << leftSec << " second(s)" << endl;
    }
    else if(conversion == 'd'){
        leftHour = sec % 86400;
        hours = leftHour / 3600;
        leftMin = leftHour % 3600;
        minutes = leftMin / 60;
        leftSec = leftMin % 60;
        days = sec / 86400;
        cout << days << " day(s) " << hours << " hour(s) " << minutes << " minute(s) " << leftSec << " second(s)" << endl;
    }
    
         
}
