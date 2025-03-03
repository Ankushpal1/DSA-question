#include<iostream>
using namespace std;

class node{
    public:
    int data;
    node* next= NULL;

    node(){
        this->data;
        this->next= NULL;

    }
    node(int data){
        this->data=data;
        this->next=NULL;

    }
};
void insertathead(node* &head, node* &tail,int data){
    // check for empty ll
    if(head== NULL){
        node* newnode = new node(data);
        head = newnode;
        tail = newnode;
        return;
    }

    node* newnode= new node(data); // creat node
    newnode->next=head; // connect with head
    head=newnode; // update

}
void insertattail(node* head,node* &tail, int data ){
    // check for empty ll
    if(head== NULL){
        node* newnode = new node(data);
        head = newnode;
        tail = newnode;
        return;
    }

    node* newnode = new node(data); // creat node
    tail->next= newnode; // connect with tail
    tail= newnode; // update
     

}

void print(node* head){
    node* temp=head;
    while(temp != NULL){
        cout<<temp->data<<" ";
        temp= temp->next;
    }

}
int findLength(node* &head ){
    int len=0;
    node*temp=head;
    while(temp != NULL){
        temp = temp->next;
        len++;
    }
    return len;
}
void insertatposition(int data,int position, node* head, node* &tail){
    //check empty ll
    if(head==NULL){
        node* newnode = new node(data);
        head= newnode;
        tail= newnode;
        return;
    }
    if(position == 0){
        insertathead(head, tail, data);
        return;
    }
    int len =findLength(head);
    if(position >= len){
        insertattail(head, tail, data);
        return;

    }

    
    // step 1; find the position previous nd current
    int i=1;
    node* prev= head;
    while(i< position){
        prev = prev->next;
        i++;
    }
    node* curr = prev->next;

    //step 2 ; creat node
    node* newnode = new node(data);

    //step 3  ; new node co current vali node se coneecrt kra
    newnode -> next= curr;
    //step 4
    prev -> next=newnode;

}
int main(){
    node* head= NULL;
    node* tail = NULL;
    // insertathead(head,tail,10);
    // insertathead(head,tail,40);
    // insertathead(head,tail,50);
    // insertattail(head, tail,20);
    // print(head);
    // cout<<endl;
    // cout<<"head: "<<head->data<<endl;
    // cout<<"tail: "<<tail->data<<endl;
    // cout<<endl;

    insertatposition(101, 0, head, tail);
    print(head);
    cout<<"head: "<<head->data<<endl;
    cout<<"tail: "<<tail->data<<endl;
}
