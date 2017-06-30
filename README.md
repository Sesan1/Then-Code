# Then-Code

	public Node findNode(int key){
		Node focusNode = root;
		while(focusNode.key != key){
			if(key < focusNode.key){
				//then go down the left child
				focusNode = focusNode.leftChild;			
			}
			else{
				focusNode = focusNode.rightChild;
			}
			if(focusNode == null)//{
				return null;
		}
		//}
		return focusNode;
	}


public boolean remove(int key){
		Node focusNode = root;
		Node parent = root;
		
		// to tell us whether to search to the left or right
		boolean isItALeftChild = true;
		
		while(focusNode.key != key){
			parent = focusNode;
			
			if(key < focusNode.key){
				focusNode = parent.leftChild;
				isItALeftChild = true;
			}
			else{
				focusNode = parent.rightChild;
				isItALeftChild = false;
			}
			if(focusNode == null)
				return false;
		}
