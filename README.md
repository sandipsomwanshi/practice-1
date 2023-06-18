# practice-11
def sqrt(x):
    if x == 0:
        return 0
    
    # Initial guess for the square root
    root = x
    
    while True:
        # Update the root with the average of the current root and x divided by the current root
        new_root = (root + x // root) // 2
        
        # If the new root is the same as the previous root, we have reached the approximation
        if new_root == root:
            break
        
        # Update the root for the next iteration
        root = new_root
    
    return root
