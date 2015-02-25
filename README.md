# aliens-on-earth
My first excited repository on github

//A treaty of friendship has been signed between Aliens and Humans. The aliens are now welcome on Earth and 
can //stay as long as they wish with the Humans. You are the person responsible to register the aliens. 

//one of the possible solution is written using C++ language of partA

//Create a console based application that accepts alien details like Code Name, Blood Color, No.of Antennas, No. of //Legs and Home Planet and then export these details into one of the 2 formats, depending on user’s choice -plain text or PDF



//# include iostream.h // iostream.h is inbetween the symbol<>

//# include fstream.h  // fstream.h is inbetween the symbol<>

 using namespace std;

int main()

{

    int number_Of_aliens = 0;
    
    string code_Name = "Default Name"; 
    
    string blood_Colour = "Default Colour";
    
    int no_Of_Antennas = 0;
    
    int no_Of_Legs = 0;
    
    string home_planet = "Default Home";
    
    cout << "Enter Number Of aliens To Register"<<endl;
    
    cin>>number_Of_aliens;

    for(int i=0;i<number_Of_aliens;i++)
    { 
        cout << "Enter Code Name"<<endl;
        cin >> code_Name;
        cout << "Enter Blood Colour"<<endl;
        cin >> blood_Colour;
        cout << "Enter No Of Antennas"<<endl;
        cin >> no_Of_Antennas;
        cout << "Enter No Of Legs"<<endl;
        cin >> no_Of_Legs;
        cout << "Enter home planet"<<endl;
        cin >> home_planet;
    
        ofstream myfile("D:\example.txt");

        if(myfile.is_open())
        {
            myfile << "Writing this to a file.\n";
            myfile << code_Name;
            myfile << blood_Colour;
            myfile << no_Of_Antennas;
            myfile << no_Of_Legs;
            myfile << home_planet;
            myfile.close();
        }
     }
    return 0;
}
