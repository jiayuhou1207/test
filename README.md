This is a point cloud dataset for irregular underground roadways. Due to the large size of the point cloud data, the authors are currently attempting to fully upload it to this repository.
Scan Session	Timestamp	Description	Key Features
Version 1	2025-06-07 09:03	Large closed-loop scan (entry-exit)	Low illumination, horizontal alignment bias
Version 2	2025-06-07 14:28	Half closed-loop scan (interrupted at slope)	Better lighting, overall good quality
Version 3	2025-06-08 10:19	Right half-loop scan with RTK	RTK-assisted positioning, slower scanning speed, partial coverage at forks
File Formats
.laz: Compressed LAS format for colored point cloud data (contains XYZ coordinates + RGB color information)
.pcd: Point Cloud Data format (filtered version of Version 2 scan)
.txt: Trajectory/path log files (recording scanner position and orientation during scanning)
Scan Session Details
1. 2025-06-07 09:03 (Large Closed-Loop)
Scenario: Full large closed-loop scan, starting and ending at the tunnel entrance.
Limitations:
Low ambient illumination → darker point cloud appearance, reduced color distinguishability.
Horizontal direction bias → potential misalignment in registration results.
Use Case: Suitable for testing low-light point cloud enhancement and robust registration algorithms.
2. 2025-06-07 14:28 (Half Closed-Loop)
Scenario: Half closed-loop scan, interrupted at a ramp section.
Advantages:
Improved lighting conditions → clearer point cloud color and detail.
Good overall scan quality → suitable for baseline experiments.
Use Case: Recommended as the primary dataset for general underground tunnel point cloud research.
3. 2025-06-08 10:19 (RTK-Assisted Right Half-Loop)
Scenario: Right half-loop scan with RTK positioning support.
Characteristics:
RTK integration → higher absolute positioning accuracy.
Slower scanning speed → denser point cloud sampling.
Partial coverage at tunnel forks → only aligned scanning at branch points.
Use Case: Ideal for research on multi-sensor fusion (LiDAR + RTK) and underground SLAM.
Data Usage Notes
Coordinate System: The point cloud data uses the scanner's native coordinate system; RTK data in Version 3 is in WGS84.
Preprocessing: Raw data may contain noise and outliers; filtering (e.g., statistical outlier removal) is recommended before use.
Registration: Version 1 has horizontal bias; Version 3 provides RTK constraints for more accurate alignment.
Visualization: Can be opened and visualized using tools like CloudCompare, MeshLab, or Open3D.
