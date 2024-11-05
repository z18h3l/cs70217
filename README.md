java c
MAEG 5755 2023-2024 PROJECT GUIDE 
(DEADLINE: 2024/11/04 23:59:59)To help you finish the project easily and not leave everything in the final week, we break down the project into several small tasks. You are required to complete them by the given deadlines.  Given that you have to finish the project anyway, I hope this guideline can reduce your pain.
1. Function Descriptions. Joint Space trajectory generation for 6DoF Robot.
You are suggested to write some functions for trajectory generation. Both of the input and output are in joint space.
(a) Example NO NEED TO COMPLETE Generate cubic trajectories for 3DoF robot    You don’t need to complete this problem. This is only for the Example (Python): 
generate_traj_cubic_3dof(start_point,  end_point,  freq,  total_time):joint_1_list  =  []joint_2_list  =  []joint_3_list  =  []#  your  codes  herefor  . . . :
...joint 1 list.append( . . .)joint 2 list.append( . . .)joint 3 list.append( . . .)
result  =  [joint_1_list,  joint_2_list,  joint_3_list]
return  result
Description: This function should generate a 3DoF cubic trajectory for the given input. Input: Start quaternion, end quaternion, frequency, and time interval.
Output: A 2D array, where the first dimension is the axis index, and the second is the value for each coordinate at each frame.
(b)  Generate cubic trajectories with intermediate points for 6DoF robot
generate_traj_cubic_6dof(point_list,  velocity_mode_list,  time_list,  freq): #  your  code  here
return  [joint1_list,  joint2_list,  . . . ,  joint6_list]Description: This function should generate a cubic trajectory for the joint angles. Assume the start velocity and the end velocity are both zero.  You should be able to choose the velocity mode for each intermediate point:  1) zero velocity, 2) average velocity, and 3) equal velocity and equal acceleration. For the third mode, only one intermediate point is enough.
Input: Position list, which should contain the starting joint angles, intermedia joint angles, and the ending joint angles, velocity mode list, time list, and frequency.
Output: In A 2D array, the first dimension is the axis index, and the second dimension is the value for each coordinate at each frame.
(c)  Generate quintic trajectories for 6DoF robot
generate_traj_quintic_6dof(start,  end,  vel_list,  acc_list,  time_list,  frequency): #  your  code  here
return  [joint1_list,  joint2_list,  . . . ,  joint6_list]
Description: This function should generate a quintic trajectory for the given starting and ending joint angles.
Input: Joint angle list, velocity list, acceleration list, time list, and frequency.
Output: A 2D array, where the first dime代 写MAEG 5755 2023-2024 PROJECT GUIDER
代做程序编程语言nsion is the axis index, and the second is the value for each coordinate at each frame.
(d)  Generate linear trajectories with parabolic blends for 6DoF robot
generate_traj_linear w parabolic_6dof(start,  end,  linear_time_list,  time_list,  frequency): #  your  code  here
return  [joint1_list,  joint2_list,  . . . ,  joint6_list]
Description: This function should generate linear trajectories with parabolic blends for given starting and ending joint angles. Assume the intermediate velocities are zero.
Input: Joint angle list, linear time for each segment, time list, and frequency.
Output: A 2D array, where the first dimension is the axis index, and the second is the value for each coordinate at each frame.
(e)  Generate SLERP(Spherical linear interpolation) trajectories for two quaternions
generate_traj_slerp(start,  end,  total_time,  freq): #  your  code  here
return  [frame_1,  frame_2, . . . ,  frame_n]
Description: This function should generate an SLERP for given starting and ending quater- nions.
Input: starting quaternion, ending quaternion, and frequency.
Output: A 1D array, where each element should be the intermedia quaternion for the trajec- tory.
2. Test and Submit. Test your code and submit.
After you finish all the functions, you can generate trajectories and use the online simulator to test.
(a) Test: You can test your trajectories in the online platform. by uploading your trajectory files. Only the first three DoFs will be tested in task space mode. Firstly, you need to convert the 2D array to text, you can use the provided code below:
def  save_traj(trajectories,  filename): result  =  "angle;"
for  trajectory  in  trajectories:
result  +=  ",".join([str(x)  for  x  in  trajectory]) result  +=  ";"
f  =  open(filename, mode="w")
f.write(result) f.close()
Description: This function should convert the 2D array into a text form. Input: Trajectory 2D array.
Output: A string that describes the trajectory. The format should be:angle; < q11 >,< q12 >, ...,< q1n >; < q21 >,< q22 >, ...,< q2n >; < q31 >,< q32 >, ...,< q3n >; < q41 >,< q42 >, ...,< q4n >; < q51 >,< q52 >, ...,< q5n >; < q61 >,< q62 >, ...,< q6n >;
Where i is the joint index and j is the timeframe. index for qij .  For example q35 means the angle of joint 3 in time frame. 5.
Then you can upload your trajectory file to the simulator.
(b) Submission: In light of the requirements mentioned above, each group is expected to provide the following works by the due date:
i. Group information ii. Code Files.
Please compress your files to a zip file and submit them on Blackboard.





         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
