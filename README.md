# numpy_transform
transform among rotation matrix, euler angles and quaternion

写程序经常遇到各种欧拉角，矩阵，四元数转化，这个包还有下面的网址也许可以帮到你

本文中的euler2rotm是相对于静态坐标系的，如果是动态坐标系可以直接用ROS的API：


tf.transformations.euler_matrix(r,p,y,axes='rxyz')#动态


tf.transformations.euler_matrix(r,p,y,axes='sxyz')#静态


Some function can be provided by ROS.
Some ROS api are also provided here:
For example:
1) quaternion to euler:

q = (msg.pose.pose.orientation.x,
     msg.pose.pose.orientation.y,
     msg.pose.pose.orientation.z,
     msg.pose.pose.orientation.w) 
tf.transformations.euler_from_quaternion(q)

2) euler to quaternion:

tf.transformations.quaternion_from_euler(r,p,y)

...

And i recommend you to read:
http://docs.ros.org/jade/api/tf/html/python/transformations.html#tf.transformations.euler_matrix


写的有点乱，也没指望谁能看懂，我看的懂就行
