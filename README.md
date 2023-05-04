Download Link: https://assignmentchef.com/product/solved-csci1300-1310-quiz-5
<br>
The definition for a class called TemperatureList is given below.

Values of this type are arrays of Fahrenheit temperatures. Add a member function called get_size, which takes no arguments and returns the number of temperatures on the array.

#include &lt;iostream&gt;

#include &lt;cstdlib&gt; using namespace std; const int maxArraySize = 50; class TemperatureList

{     public:

TemperatureList( );

~TemperatureList( );

void add_temperature(double temperature);//Precond:list not full.

bool full( )//Returns true if the list is full; false otherwise.

void printList();

int get_size();//Returns the number of temperatures in list     private:         double listTemp[maxArraySize];//array of temps in Fahrenheit         int currentSize; //number of array positions filled

};

//This is the implementation for the class TemperatureList.

TemperatureList::TemperatureList( )

{

currentSize =0;

//ctor }

void TemperatureList::add_temperature(double temperature)

{

if ( full( ) ) {

cout &lt;&lt; “Error: adding to a full list.
”;

exit(1);     }else{

listTemp[currentSize] = temperature; //appending a temp

currentSize = currentSize + 1;

}

}

bool TemperatureList::full( ) {    return (currentSize == maxArraySize);

}

void TemperatureList::printList()

{

for (int i = 0; i &lt; currentSize; i++)     cout &lt;&lt; listTemp[i] &lt;&lt; ” F
”;

}

{{ STUDENT_ANSWER }}

#2

Create a class called Person that has three private data members:

string name int age string hometown

The Person class should have one constructor that takes an argument for each data members and sets those values.

The Person class should also have one public method called printValues( ) that prints the values of each data member in the following format:

Name: &lt;name&gt;

Age: &lt;age&gt;

Hometown: &lt;hometown&gt;