## Q1:
### **1. Converting Code to Graph**

The given code defines the method `useDynamicWindow(byte windowValue)`, which manipulates the `data.windowUse` array by searching for a given `windowValue`, rearranging indices, and updating the most recently used index. To convert this into a control flow graph (CFG), we must follow these steps:

```java title:"CharsetSCSU.java"
private void useDynamicWindow(byte windowValue){ 
	/*first find the index of the window*/ 
	int i,j; 
	i = data.nextWindowUseIndex; 
	
	do{ 
		if(--i<0){ 
			i=7; 
		} 
	} while(data.windowUse[i]!=windowValue);
	
	/*now copy each window[i+1] to [i]*/ 
	j= i+1; 
	if(j==8)
	{ 
		j=0; 
	} 
	
	while(j!=data.nextWindowUseIndex)
	{ 
		data.windowUse[i] = data.windowUse[j]; 
		i=j; 
		if(++j==8){ 
			j=0; 
	}
	
	/*finally, set the window into the most recently used index*/
	data.windowUse[i]= windowValue; 
}
```


---

#### Step 1: Identify the Key Control Flow Elements

- **Start of the function** → The function initializes variables `i` and `j`.
- **First loop (do-while loop)** → Searches for the `windowValue` in `data.windowUse`, iterating backward.
- **Second loop (while loop)** → Shifts elements of `data.windowUse` forward in a circular manner.
- **Final assignment** → Updates `data.windowUse[i]` with `windowValue`.

#### Step 2: Construct the Graph Nodes

1. **Entry Point** → Function starts.
2. **Initialization** → Variables `i` and `j` are declared.
3. **do-while loop** → Iterates to find `windowValue`, with a condition check.
4. **if condition inside do-while** → Checks if `i < 0`, resetting it to 7.
5. **while loop** → Moves elements in `data.windowUse` forward.
6. **Final update** → Assigns `windowValue` to `data.windowUse[i]`.
7. **Exit Point** → Function ends.

#### Step 3: Define the Edges (Connections Between Nodes)

- Start → Initialization → `do-while` loop.
- `do-while` loop → If condition inside it (check `i < 0`).
- If condition → Back to `do-while` or exits to next part.
- `while` loop → Iterates until it reaches `data.nextWindowUseIndex`.
- Final update occurs → Function exits.

This creates a **control flow graph (CFG)** that visually represents the paths the program execution can take.


---

### 2. Labelling Definitions (defs) and Uses (uses)
- **Variable `i`:**
    - **Definitions (defs):** Line 6 (`i = data.nextWindowUseIndex`), Line 11 (`i = 7` if `i < 0`), Line 20 (`i = j`).
    - **Uses (uses):** Line 10 (`--i < 0` condition), Line 14 (`j = i + 1`), Line 22 (`data.windowUse[i] = data.windowUse[j]`), Line 26 (`data.windowUse[i] = windowValue`).
    
- **Variable `j`:**
    - **Definitions (defs):** Line 14 (`j = i + 1`), Line 16 (`j = 0` if `j == 8`), Line 23 (`if (++j == 8) j = 0`).
    - **Uses (uses):** Line 22 (`data.windowUse[i] = data.windowUse[j]`), Line 23 (`while (j != data.nextWindowUseIndex)`).
    
- **Variable `data`:**
    - **Definitions (defs):** `data.windowUse` is being assigned in Line 26.
    - **Uses (uses):** Throughout (`data.windowUse[i]`, `data.windowUse[j]`, `data.nextWindowUseIndex`).


---

### 3. Graph:
##### **CFG:**
![[Wk3 Question1 graph1]]
[[Wk3 Question1 graph1]]


##### **CFG with defs and uses:**
![[Wk3 Question1 graph2]]
[[Wk3 Question1 graph2]]


---

## Q2: Find the du-paths for x.:

![[Pasted image 20250311124611.png]]To find the **definition-use paths (du-paths)** for `x` in the given control flow graph, we need to identify:

1. **Definitions of `x`** → Where `x` is assigned a value.
2. **Uses of `x`** → Where `x` is referenced in an expression or condition.
3. **Paths between definitions and uses** without redefining `x`.

### Step 1: Identify Definitions and Uses of `x`

- **Node 0**: `x` is **defined** and **used**.
- **Node 7**: `x` is **used**.

### Step 2: Find Paths from Definitions to Uses

A **du-path** must start from a definition and reach a use without `x` being redefined along the way.

Possible paths from **Node 0 (def x) → Node 7 (use x)**:

1. **Path 1**: `0 → 2 → 5 → 7`
2. **Path 2**: `0 → 3 → 5 → 7`
3. **Path 4**: `0 → 2 → 5 → 6 → 5 → 7`
4. **Path 5**: `0 → 3 → 5 → 6 → 5 → 7`
5. **Path 6**: `0 → 1 → 5 → 6 → 5 → 7`

These are the **du-paths** for `x` in the given graph.

