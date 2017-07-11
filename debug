/**
 * Definition for a binary tree node.
 * struct TreeNode {
 *     int val;
 *     TreeNode *left;
 *     TreeNode *right;
 *     TreeNode(int x) : val(x), left(NULL), right(NULL) {}
 * };
 */
class Solution {
public:
    TreeNode* deleteNode(TreeNode* root, int key) {
        if (!root) return root;
		// first find the node
		TreeNode* keyNode(nullptr);
		TreeNode* root1(root);
		while(root1){
			if (root1->val == key){keyNode = root1; break;}
			if (root1->val > key) root1 = root -> left;
			else root1 = root -> right;
		}
		if (!keyNode) return root; // if key not found in the tree
		// now delete keyNode
		// scenario 1: leaf
		if (!keyNode -> left && !keyNode -> right) { delete(keyNode); return root;}
		//scenario 2: has one child 
		if (!keyNode -> left){
			keyNode -> val = keyNode -> right -> val;
			keyNode -> right = nullptr;
			return root;
		} 
		if (!keyNode -> right){
			keyNode -> val = keyNode -> left -> val;
			keyNode -> left = nullptr;
			return root;
		}
		// scenario 3: has two children
		TreeNode* subRight(keyNode->right);
		while(subRight -> left){
			subRight = subRight->left;
		}
        int rightMin = subRight -> val;
        delete (subRight);
		keyNode -> val = rightMin;
		return root;
    }
};
