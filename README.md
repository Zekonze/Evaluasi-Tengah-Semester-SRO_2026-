# Evaluasi-Tengah-Semester-SRO_2026-
Muhammad Darrell Raditiya - 5022231063

Misi: menghasilkan representasi 3D lingkungan tertutup dari pembacaan depth scanner selama Quadcopter mengikuti waypoint. Python mencatat lintasan, mengubah titik lokal sensor menjadi koordinat dunia, lalu mengelompokkan titik ke voxel.
Komponen
Peran dalam misi
/Quadcopter
Bodi drone; posisi dan orientasi menjadi acuan transformasi dunia.
Target drone (dummy)
Setpoint posisi yang diikuti pengendali Quadcopter bawaan; alias dapat berbeda.
/FlightMission (dummy)
Menyimpan simulation script Lua untuk urutan waypoint dan status misi.
fast3DLaserScanner
Model pemindai yang menjadi child Quadcopter.
Vision sensor /sensor
Menyediakan depth buffer. Resolusi yang pernah terdiagnosis: 64 × 64.
Floor / ExternalWall
Permukaan lantai dan pembatas arena pemetaan.
Cuboid[0]–[2]
Tiga penghalang berbentuk kotak sebagai target pemindaian.
