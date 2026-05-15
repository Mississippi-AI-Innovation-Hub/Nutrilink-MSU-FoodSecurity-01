# Manual Tests

This PoC used manual testing rather than a full automated test suite.

## Test Case 1: Resource Lookup

**Prompt:**  
Where can I find food assistance in Hinds County?

**Expected Behavior:**  
The system should return Hinds County food assistance resources, such as food banks, pantries, SNAP-related help, or community organizations.

**Result:**  
Demonstrated.

---

## Test Case 2: HER/SWAP Explanation

**Prompt:**  
What is HER/SWAP guidance?

**Expected Behavior:**  
The system should explain that HER/SWAP provides nutrition guidance and food categorization support.

**Result:**  
Demonstrated / Partial.

---

## Test Case 3: Meal Classification

**Prompt:**  
I ate chicken, rice, soda, and chips. Is this healthy?

**Expected Behavior:**  
The system should provide general nutrition guidance and avoid making medical claims.

**Result:**  
Partial.

---

## Test Case 4: Frontend API Call

**Prompt:**  
User submits a question through the GUI.

**Expected Behavior:**  
The frontend should call API Gateway, which invokes Lambda and returns a response.

**Result:**  
Demonstrated / Partial.

---

## Test Case 5: Playground Query

**Prompt:**  
Ask the same questions directly in Amazon Bedrock Playground.

**Expected Behavior:**  
The response should use retrieved knowledge base context.

**Result:**  
Demonstrated.

## Notes

Manual testing showed that Bedrock Playground responses were more consistent than GUI/API responses. With API refinement, the GUI should theoretically work as intended.