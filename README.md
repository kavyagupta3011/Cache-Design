# Cache-Design


## **Project Overview**
This project involves building a **Set-Associative Cache Simulator** as part of the **EGC 223: Computer Architecture Memory Design** course. The simulator is implemented in Python using an object-oriented approach and explores various cache configurations to analyze performance metrics like hit and miss rates.  

---


## **Features**
- **Cache Design:**  
  - Implements a **4-way set-associative cache** with configurable cache size, block size, and associativity.  
  - Tracks least recently used (LRU) policy, valid bits, and tags through `BlockLine` and `EachSet` classes.  

- **Experiments Conducted:**  
  - **Part (a):** Fixed a 4-way set-associative cache with 1024kB size and 4-byte blocks.  
  - **Part (b):** Varied cache size from 128kB to 4096kB.  
  - **Part (c):** Varied block size from 1 byte to 128 bytes.  
  - **Part (d):** Varied associativity from 1-way to 64-way.  

- **Trace Files:**  
  - Simulation tested on multiple input trace files (e.g., `twolf.trace`, `gzip.trace`, etc.).

---

## **Simulation Details**

### **1. 4-Way Set-Associative Cache**
- **Setup:**  
  - Cache size: 1024kB.  
  - Block size: 4 bytes.  
  - Resulting cache lines: `1024 * 1024 / (4 * 4) = 65,536`.  

- **Observations:**  
  - Hit rate descending order: `twolf.trace > gcc.trace > swim.trace > gzip.trace > mcf.trace`.  

---

### **2. Cache Performance with Varying Cache Size**
- **Setup:**  
  - Cache size: 128kB to 4096kB.  
  - Block size: 4 bytes.  

- **Observations:**  
  - Changes in miss rates were minimal, highlighting limited exploitation of spatial and temporal locality.  
  - Graphs plotted to show minor differences.  

---

### **3. Cache Performance with Varying Block Size**
- **Setup:**  
  - Cache size: 1024kB.  
  - Block size: 1 byte to 128 bytes.  

- **Observations:**  
  - Miss rates decreased as block size increased, leveraging **spatial locality**.  
  - Hit rates improved slightly for larger block sizes.  

---

### **4. Cache Performance with Varying Associativity**
- **Setup:**  
  - Cache size: 1024kB.  
  - Associativity: 1-way (direct-mapped) to 64-way.  

- **Observations:**  
  - Hit rates generally increased with associativity but varied depending on input files.  
  - `gzip.trace` behaved differently due to its memory access patterns causing fewer conflicts.  

---

## **Results**
- **Metrics Analyzed:**  
  - Hit and miss rates were recorded and plotted for each experiment.  
  - Graphs and tables highlight cache performance across varying configurations.  

---

## **Conclusion**
The simulation provided insights into how cache size, block size, and associativity impact cache performance. Spatial and temporal locality played significant roles, but input trace patterns influenced the results.  

---

## **Usage Instructions**
1. Clone the repository.  
2. Run the Python script to initialize the simulation.  
3. Choose the experiment to execute (`a`, `b`, `c`, or `d`).  
4. View hit and miss rate tables and graphs.  

---

