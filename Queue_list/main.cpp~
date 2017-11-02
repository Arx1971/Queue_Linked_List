#include <iostream>
#include <cstdio>
#include <algorithm>
#include <string>
#include <cstdlib>

#define null NULL

using namespace std;

struct q_node{
	int data;
	q_node *next;
};

void q_init(q_node *head, int key){
	head -> data = key;
	head -> next = null;
}

void q_print(q_node *head){
	while(head!=null){
		cout << head -> data << endl;
		head = head -> next;
	}
}

void q_push_back(q_node *head, int key){
	q_node *temp = new q_node;
	temp -> data = key;
	temp -> next = null;
	while(head){
		if(head -> next == null){
			head -> next = temp;
			return;
		}
		head = head -> next;
	}
}

int q_front(q_node *head){
	return head -> data;
}

int q_size(q_node *head){
	int temp = 0;
	while(head!=null){
		temp++;
		head = head -> next;
	}
	return temp;
}

bool q_isempty(q_node *head){
	if(head == null) return true;
	else return false;
}

q_node *q_clear(q_node *head){
	head = null;
	return head;
}

q_node *q_pop(q_node *head){
	if(q_isempty(head)){
		cout << "Queue Is empty" << endl;
		return head;
	}
	else{
		q_node *temp = head;
		head = temp -> next;
		return head;
	}
}

int main(){
	struct q_node *mq = null;
	cout << "Queue Is empty: " << q_isempty(mq)  << endl;
	mq = new q_node;
	q_init(mq,10);
	q_push_back(mq,20);
	q_push_back(mq,30);
	q_push_back(mq,40);
	q_push_back(mq,50);
	q_print(mq);
	cout << "Front: " << q_front(mq) << endl;
	cout << "Size: " << q_size(mq) << endl;
	cout << "Queue Is empty: " << q_isempty(mq)  << endl;
	mq = q_clear(mq);
	cout << "Queue Is empty: " << q_isempty(mq)  << endl;
	mq = new q_node;
	q_init(mq,10);
	q_push_back(mq,20);
	q_push_back(mq,30);
	q_push_back(mq,40);
	q_push_back(mq,50);
	q_print(mq);
	mq = q_pop(mq);
	mq = q_pop(mq);
	mq = q_pop(mq);
	mq = q_pop(mq);
	mq = q_pop(mq);
	mq = q_pop(mq);
	cout << "Print Data" << endl;
	q_print(mq);
	return 0;
}
