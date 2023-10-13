  * # Eager Execution
    * The benefit is that the *entire* model graph does not have to be built.
    * Instead, operations are evaluated *immediatley*, making it easier to get started building your models (as well as debugging them)
  * # GradientTape
    * Open a GradientTape allows to record the operations run during the foward pass, which enables autodifferentiation.
      * ![[Roam/Turing/Attachments/imgs/app/Turing/9PPFkEChuI.png]]
