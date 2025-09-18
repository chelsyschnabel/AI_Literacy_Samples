# AI Literacy: Undergraduate Computer Science

## Overview

Students will write code and utilize AI to help them improve upon their code without the AI rewriting the code for them.

**Subject:** Computer Science - Data Structures & Algorithm Analysis  
**Suggested Tools:** GitHub Copilot & ChatGPT for code review and complexity analysis  
**Learning Objective:** Using AI to improve code quality and analyze algorithmic efficiency

## Student Work Sample: "Binary Search Tree Implementation with AI-Assisted Optimization"

### **Project Context:** Implementing a self-balancing BST with performance analysis

### Phase 1: Initial Implementation (Student's Independent Work)
```python
class BSTNode:
    def __init__(self, value):
        self.value = value
        self.left = None
        self.right = None
        self.height = 1

class AVLTree:
    def __init__(self):
        self.root = None
    
    def insert(self, value):
        self.root = self._insert_recursive(self.root, value)
    
    def _insert_recursive(self, node, value):
        # Standard BST insertion
        if not node:
            return BSTNode(value)
        
        if value < node.value:
            node.left = self._insert_recursive(node.left, value)
        else:
            node.right = self._insert_recursive(node.right, value)
        
        # Update height and balance
        self._update_height(node)
        return self._balance(node)
```

### Phase 2: AI-Assisted Code Review
*Student's prompt to AI:* "I'm implementing an AVL tree in Python. Below is my current code. Can you review it for potential improvements in efficiency, readability, or Python best practices? Please don't rewrite it completely, but point out specific areas I should consider refining."

**AI Feedback Summary:**
- Height calculation could be more efficient with memoization
- Balance factor calculation is missing
- Error handling for duplicate values not addressed
- Could benefit from type hints
- Consider adding docstrings for documentation

### Phase 3: Student's Refinement Based on AI Suggestions
```python
from typing import Optional

class BSTNode:
    def __init__(self, value: int):
        self.value = value
        self.left: Optional['BSTNode'] = None
        self.right: Optional['BSTNode'] = None
        self.height = 1
    
    def get_balance_factor(self) -> int:
        """Calculate balance factor for AVL property."""
        left_height = self.left.height if self.left else 0
        right_height = self.right.height if self.right else 0
        return left_height - right_height
    
    def update_height(self) -> None:
        """Update height based on children's heights."""
        left_height = self.left.height if self.left else 0
        right_height = self.right.height if self.right else 0
        self.height = max(left_height, right_height) + 1
```

### Phase 4: Performance Analysis with AI Assistance
*Student's prompt:* "I want to analyze the time complexity of my AVL tree operations. I believe insertion is O(log n), but I want to verify this reasoning and understand how the balancing affects the analysis. Can you guide me through analyzing this step by step?"

**Analysis Results:**
- Confirmed O(log n) insertion time
- Identified that rotation operations are O(1)
- Discovered that rebalancing occurs at most O(log n) times per insertion
- Understood why AVL guarantees better worst-case performance than basic BST

### Phase 5: Empirical Testing
Student designed performance tests, used AI to suggest edge cases, and created visualizations comparing AVL performance to basic BST with different data distributions.

**Final Reflection:**
"This project demonstrates how AI can serve as a code review partner and complexity analysis tutor without replacing my own critical thinking. I maintained ownership of my design decisions while leveraging AI to identify blind spots, suggest improvements, and verify my theoretical understanding. The AI helped me learn professional development practices like type hinting and documentation while deepening my understanding of algorithmic complexity. This represents the kind of AI-assisted learning I want to continue in my career."