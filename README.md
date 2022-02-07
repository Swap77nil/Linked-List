# Linked-List
1.Write a C++ program to implement singly linked list
 #include<iostream> 
 #include<cstdlib> 
 using namespace std;
  struct node
  { 
  int info;   struct node *next;
  }*start; 
 class single_llist 
 { 
  public:   node* create_node(int);   void insert_begin();   void insert_last();   void insert_pos();   void delete_begin();   void delete_last();   void delete_pos();   void update_begin();   void update_last();   void update_pos();   void sort();   void reverse();   void search();   void display();   single_llist()   {   start = NULL;  
}  };  int main()  {   int choice;   single_llist sl,s2;   start = NULL;   do   {   cout<<"---------------------------------"<<endl;   cout<<"Operations on singly linked list"<<endl;   cout<<"---------------------------------"<<endl;   cout<<"1.Insert at first"<<endl;   cout<<"2.Insert at last"<<endl;   cout<<"3.Insert at position"<<endl;   cout<<"4.Delete at first"<<endl;   cout<<"5.Delete at Last"<<endl;   cout<<"6.Delete at position"<<endl;   cout<<"7.Update at first"<<endl;   cout<<"8.Update at last"<<endl;   cout<<"9.Update at position"<<endl;   cout<<"10.Ascending order"<<endl;   cout<<"11.Descending order"<<endl;   cout<<"12.Search"<<endl;   cout<<"13.Display"<<endl;   cout<<"14.Exit "<<endl;   cout<<"Enter your choice :";   cin>>choice;   switch(choice)  
 {   case 1: sl.insert_begin();   sl.display();   break;   case 2: sl.insert_last();   sl.display();   break;   case 3: sl.insert_pos();   sl.display();   break;   case 4: s2.delete_begin();   sl.display();   break;   case 5: s2.delete_last();   sl.display();   break;   case 6: sl.delete_pos();   sl.display();   break;   case 7: sl.update_begin();   sl.display();   break;   case 8: sl.update_last();   sl.display();   break;   case 9: sl.update_pos();   sl.display();   break;   case 10:sl.sort();  
 sl.display();   break;   case 11:sl.reverse();   sl.display();   break;   case 12:sl.search();   sl.display();   break;   case 13:sl.display();   break;   case 14:exit(0);   break;   default:cout<<"Wrong choice...???"<<endl;   break;   }   }   while(choice != 14);  }  node *single_llist::create_node(int value)  {   struct node *temp, *s;   temp = new(struct node);   if (temp == NULL)   {   cout<<"Memory not allocated"<<endl;   return 0;   }   else   {  
 temp->info = value;   temp->next = NULL;   return temp;   }  }  void single_llist::insert_begin()  {   int value;   cout<<"Enter the value to be inserted : ";   cin>>value;   struct node *temp, *s;   temp = create_node(value);   if (start == NULL)   {   start = temp;   start->next = NULL;   cout<<temp->info<<" is inserted at first in the empty list"<<endl;   }   else   {   s = start;   start = temp;   start->next = s;   cout<<temp->info<<" is inserted at first"<<endl;   }  }  void single_llist::insert_last()  {   int value;  
