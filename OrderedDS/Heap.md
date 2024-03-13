
```
void downHeap(Node *n) {

  

// Implement downHeap() here.

if (n->right && !n->left){

if (n->value > n->right){swap(n,n->right);downHeap(n->right);}

}

  

else if (!n->right && n->left){

if (n->value > n->left){swap(n,n->left); downHeap(n->left);}

}

  

else if (!n->right && !n->left){};

else{

if(n->left->value <=n->right->value){swap(n,n->left); downHeap(n->left);}

else{ swap(n,n->right);downHeap(n->right);}

}

  

}
```