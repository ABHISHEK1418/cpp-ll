# cpp-ll
#include<bits/stdc++.h>
using namespace std;
class Node
{
	public:
		int data;
		Node *nxt;
};

 void push(Node** h,int data)
 {
 	Node *N = new Node();
 	N->data=data;
 	N->nxt = *h;
 	*h = N;
 	
 };
 
 void insertafter(Node *p, int data)
 {
 	if(p==NULL)
 	{
 		cout<<"not possible";
 		return;
	}
	Node *N = new Node();
	N->data=data;
	N->nxt = p->nxt;
	p->nxt= N;
 }
 
 void append(Node *h,int data)
 {
 	while(h->nxt!=NULL)
 	{h=h->nxt;
	}
	Node *N = new Node();
	N->data=data;
	N->nxt = h->nxt;
	h->nxt = N;
	 
 }
 
 void printll(Node *N)
 {
 	while(N!=NULL)
 	{
 		cout<<N->data;
 		N=N->nxt;
	 }
 }

int main() 
{ 
  /* Start with the empty list */
  Node* h = NULL; 
  
  // Insert 6.  So linked list becomes 6->NULL 
  append(&h, 6); 
  
  // Insert 7 at the beginning. So linked list becomes 7->6->NULL 
  push(&h, 7); 
  
  // Insert 1 at the beginning. So linked list becomes 1->7->6->NULL 
  push(&h, 1); 
  
  // Insert 4 at the end. So linked list becomes 1->7->6->4->NULL 
  append(&h, 4); 
  
  // Insert 8, after 7. So linked list becomes 1->7->8->6->4->NULL 
  insertafter(head->nxt, 8); 
  
  cout<<"linklist created";
  printll(N); 
  
  return 0; 
} 
