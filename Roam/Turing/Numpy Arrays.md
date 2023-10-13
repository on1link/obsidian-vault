  * ## Slides:
    * ### Array Views vs. Copies
      * A numpy array object has a pointer to a dense block of memory that stores the data of the array.
      * *Basic* slices are just *views* of this data - they are **not** a new copy.
      * Binding the same object to different variables will **not** create a copy.
      * *Advanced* slices will create a copy if bound to a new 
variable - these are cases where the result may contain elements that 
are not contiguous in the original array
