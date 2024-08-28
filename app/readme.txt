Example: tdse-tp0_05-hw_sw_test

 Description:
 Bare Metal - Event-Triggered Systems (ETS)
 App - retarget_printf_to_Console
 Project for STM32 Project (STM32CubeIDE Version: 1.7.0)

  SystemCoreClock     => 64MHz (15.625nS)
  SysTick Rate Hertz  => 1000 ticks per second (1mS)

  app.c (app.h)
   Endless loops, which execute tasks with fixed computing time. This 
   sequential execution is only deviated from when an interrupt event occurs.

  task_a.c (task_a.h) 
   Blocking Code

  task_b.c (task_b.h)
   Non-Blocking Code

  task_c.c (task_c.h)
   Update by Time Code

  logger.h (logger.c)
   Utilities for Retarget "printf" to Console

  dwt.h
   Utilities for Mesure "clock cycle" and "execution time" of code
  
  Special connection requirements:
   There are no special connection requirements for this example.

Build procedures:
Visit the Getting started with STM32: STM32 step-by-step at 
"https://wiki.st.com/stm32mcu/wiki/STM32StepByStep:Getting_started_with_STM32_:_STM32_step_by_step"
to get started building STM32 Projects.

Debug Log:

app_init is running - Tick [mS] = 0

 Bare Metal - Event-Triggered Systems (ETS)

 App - retarget_printf_to_Console

 g_app_cnt = 0

  task_a_init is running - Task A - Blocking Code

   g_task_a_cnt = 0

  task_b_init is running - Task B - Non-Blocking Code

   g_task_b_cnt = 0

  task_c_init is running - Task C - Update by Time Code

   g_task_c_cnt = 0



app_update is running - Tick [mS] = 1

 g_app_cnt = 1



 cycle_counter_reset

  task_a_update is running - Task A - Blocking Code

   g_task_a_cnt = 1

 cycle_counter: 1716748 - cycle_counter_time_us: 26824 uS



 cycle_counter_reset

  task_b_update is running - Task B - Non-Blocking Code

   g_task_b_cnt = 1

 cycle_counter: 14106 - cycle_counter_time_us: 220 uS



 cycle_counter_reset

  task_c_update is running - Task C - Update by Time Code

   g_task_c_cnt = 1

 cycle_counter: 15449 - cycle_counter_time_us: 241 uS