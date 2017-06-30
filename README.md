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
