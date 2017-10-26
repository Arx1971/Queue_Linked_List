#include <iostream>
#include <algorithm>
#include <string>
#include <queue>

#define null NULL

using namespace std;

struct q_node{
	int data;
	q_node *next;
};

void init(q_node *head, int key){
	head -> data = key;
	head -> next = null;
}

void display(q_node *head){
	while(head!=null){
		cout << head -> data << endl;
		head = head->next;
	}
}

q_node *q_push_back(q_node *head, int key){
	q_node *temp = new q_node;
	temp -> data = key;
	temp -> next = head;
	head = temp;
	return head;
}

bool q_isempty(q_node *head){
	if(head == null) return true;
	else return false;
}

int q_size(q_node *head){
	int temp = 0;
	while(head!=null){
		temp++;
		head = head->next;
	}
	return temp;
}

q_node *q_clear(q_node *head){
	head = null;
	return head;
}

int q_front(q_node *head){
	while(head->next!=null){
		head = head -> next;
	}
	return head -> data;
}

int q_back(q_node *head){
	return head -> data;
}

void q_pop(q_node *head){
	if(!q_isempty(head)){
		while(head!=null){
			if(head -> next == null){
				head = null;
				return;
			}
			else if(head -> next -> next == null){
				head -> next = null;
				cout << "Data Remove: " << endl;
				return;
			}
			head = head -> next;
		}
	}
}

int main(){
	struct q_node *myqueue = new q_node;
	
	init(myqueue,10);
	myqueue = q_push_back(myqueue,20);
	myqueue = q_push_back(myqueue,30);
	myqueue = q_push_back(myqueue,40);
	display(myqueue);
	cout << "Queue Size: " << q_size(myqueue) << endl;
	cout << "Queue Front: " << q_front(myqueue) << endl;
	cout << "Queue Empty: " << bool(q_isempty(myqueue)) << endl;
	myqueue = q_clear(myqueue);
	cout << "Queue Empty: " << bool(q_isempty(myqueue)) << endl;
	myqueue = new q_node;
	init(myqueue,10);
	myqueue = q_push_back(myqueue,20);
	myqueue = q_push_back(myqueue,30);
	myqueue = q_push_back(myqueue,40);
	display(myqueue);
	cout << "Queue Size: " << q_size(myqueue) << endl;
	cout << "Queue Front: " << q_front(myqueue) << endl;
	cout << "Queue Empty: " << bool(q_isempty(myqueue)) << endl;
	cout << "Queue Back: " << q_back(myqueue) << endl;
	q_pop(myqueue);
	display(myqueue);
	q_pop(myqueue);
	display(myqueue);
	q_pop(myqueue);
	display(myqueue);
	q_pop(myqueue);
	display(myqueue);
	cout << "Queue Empty: " << bool(q_isempty(myqueue)) << endl;
	q_clear(myqueue);
	display(myqueue);
	cout << "Queue Size: " << q_size(myqueue) << endl;
	return 0;
}
