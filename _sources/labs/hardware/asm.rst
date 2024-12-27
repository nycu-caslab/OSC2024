======================
The Assembly You Need
======================

Although this course is not about learning assembly language, you still need to write some assembly in bare metal programming.

Here, we provide pieces of assembly code you possibly need.
After copy and paste, you still need to look up the manual to understand how this codes work.


.. important::
  You might still need others to achieve some extra function.
  Please refer to this two manual for more information.

  `the_a64_Instruction_set_100898_0100.pdf <https://github.com/nycu-caslab/OSC2024/raw/main/supplement/the_a64_Instruction_set_100898_0100.pdf>`_

  `DDI_0596_ARM_a64_instruction_set_architecture.pdf <https://github.com/nycu-caslab/OSC2024/raw/main/supplement/DDI_0596_ARM_a64_instruction_set_architecture.pdf>`_
  
  `DDI0487E_a_armv8_arm.pdf <https://github.com/nycu-caslab/OSC2024/raw/main/supplement/DDI0487E_a_armv8_arm.pdf>`_

#####
Lab 0
#####

.. code-block:: c
  
  // enter busy loop
  _start:
    wfe
    b _start

#####
Lab 1
#####

.. code-block:: c

  // set stack pointer and branch to main function.
  2:
  	ldr x0, = _stack_top
  	mov sp, x0
  	bl main
  1:
  	b 1b
