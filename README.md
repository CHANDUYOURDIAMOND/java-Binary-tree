class BinaryTreeTraversal {
    int val;
    TreeNode left, right;

   BinaryTreeTraversal(int val) {
        this.val = val;
        this.left = this.right = null;
    }
}

public class BinaryTreeTraversal {

    public void inorderTraversal(TreeNode root) {
        if (root == null) return;

        inorderTraversal(root.left);
        System.out.print(root.val + " ");
        inorderTraversal(root.right);
    }

    public void postorderTraversal(TreeNode root) {
        if (root == null) return;

        postorderTraversal(root.left);
        postorderTraversal(root.right);
        System.out.print(root.val + " ");
    }
 
    public static void main(String[] args) {
        BinaryTreeTraversal tree = new BinaryTreeTraversal();

        TreeNode root = new TreeNode(1);
        root.left = new TreeNode(2);
        root.right = new TreeNode(3);
        root.left.left = new TreeNode(4);
        root.left.right = new TreeNode(5);

        System.out.print("Inorder traversal: ");
        tree.inorderTraversal(root); // Expected: 4 2 5 1 3

        System.out.println();

        System.out.print("Postorder traversal: ");
        tree.postorderTraversal(root); // Expected: 4 5 2 3 1
    }
}
