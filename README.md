# NASSCOM-VSD-SoC-Design-Program
>>Day 1
>>Steps to invoke the tool
// cd Desktop/work/tools/openlane_working_dir/openlane
// docker
// ls -ltr
// ./flow.tcl -interactive
// package require openlane 0.9
// prep -design picorv32a
// run_synthesis
>><img width="952" alt="synthesis" src="https://github.com/Shailaja9607/NASSCOM-VSD-SoC-Design-Program/assets/169365653/33a9a384-ca81-402e-adfd-64082d82581e">

//cd Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/12-05_08-28
//less merged.lef

<img width="960" alt="mergedfiles" src="https://github.com/Shailaja9607/NASSCOM-VSD-SoC-Design-Program/assets/169365653/90e60bdf-1fa7-43bc-9d31-d8395869b7cf">

//In Synthesis report , the flop ratio is calculated by considering ratio of D-flip-flops and total number of cells 
# flop ratio = (1613) / (14876) =0.108x100= 10.84 %
<img width="725" alt="numof cells" src="https://github.com/Shailaja9607/NASSCOM-VSD-SoC-Design-Program/assets/169365653/b90c687b-7624-4175-ac12-43a702d142b2">		    

<img width="676" alt="flipflop" src="https://github.com/Shailaja9607/NASSCOM-VSD-SoC-Design-Program/assets/169365653/eee4a457-ab46-4495-9315-eb24ec0df6f0">

//less 1-yosys_4.stat.rpt
<img width="700" alt="yosys stat rpt" src="https://github.com/Shailaja9607/NASSCOM-VSD-SoC-Design-Program/assets/169365653/be1ada98-b703-4cdf-a5b7-eda7e635b15e">

// less 2-opensta.rpt
<img width="685" alt="opensta rpt" src="https://github.com/Shailaja9607/NASSCOM-VSD-SoC-Design-Program/assets/169365653/2c889301-24be-4469-b69e-f1f7e42c5527">

// less 2-openstat.timing.rpt
<img width="677" alt="opensta timing rpt" src="https://github.com/Shailaja9607/NASSCOM-VSD-SoC-Design-Program/assets/169365653/2ff79b0d-62cb-4db1-91a3-938ed0aa7721">

// Day 2
# Utilization Factor = (Area occupied by netlist)/ (Total area of core)
# Aspect Ratio = Height / Width
 Steps to run floorplanning
 // Cd Desktop/work/tools/openlane_working_dir/openlane/configuration

 // less README.md
 <img width="953" alt="readme file" src="https://github.com/Shailaja9607/NASSCOM-VSD-SoC-Design-Program/assets/169365653/c787128f-d830-4d3c-9a42-82342beb2f02">

 // less floorplan.tcl
 <img width="958" alt="floorplan" src="https://github.com/Shailaja9607/NASSCOM-VSD-SoC-Design-Program/assets/169365653/5174e8ed-19f5-4cfa-90f5-9e9cf8b1b335">

# Floorplan defaults Vmetal- 3, Hmetal-4, Core utility-50, Aspectratio-1, Core Margin- 0

# Def file  Dimensions of chip in um 660685/1000 = 660.685um 
<img width="947" alt="die area in def file" src="https://github.com/Shailaja9607/NASSCOM-VSD-SoC-Design-Program/assets/169365653/c6627cf5-a0e8-4990-a373-8482772941f4">

# magic -T/home/nickson/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read picorv32a.floorplan.def &
<img width="924" alt="commands for layout in magic" src="https://github.com/Shailaja9607/NASSCOM-VSD-SoC-Design-Program/assets/169365653/a31911fc-c468-4212-b25d-1ef6d0e3b56d">
<img width="950" alt="layout" src="https://github.com/Shailaja9607/NASSCOM-VSD-SoC-Design-Program/assets/169365653/2d81c2ca-ace7-4589-90eb-35bc24cd59fb">

// run_placement after run_floorplan
# Placement
// Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/20-05_11-34/results/palcement
# magic -T/home/nickson/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read picorv32a.placement.def &
<img width="942" alt="placement layout" src="https://github.com/Shailaja9607/NASSCOM-VSD-SoC-Design-Program/assets/169365653/58bfaa2b-f4c9-42a7-ba63-f66cb2412f5b">
<img width="936" alt="layout1" src="https://github.com/Shailaja9607/NASSCOM-VSD-SoC-Design-Program/assets/169365653/629af675-8751-412d-8e09-75b697eb1d89">
<img width="807" alt="placement of cells" src="https://github.com/Shailaja9607/NASSCOM-VSD-SoC-Design-Program/assets/169365653/29be777b-0784-4041-8c7f-b1a71635b878">
<img width="942" alt="placement layout" src="https://github.com/Shailaja9607/NASSCOM-VSD-SoC-Design-Program/assets/169365653/71956b7a-693b-451b-91a4-40f44ac1cf30">


//Steps to change I/O pins distance 
# cd Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs
// ls -ltr
# cd 20-05_11-34/results/floorplan
// run the floorplan once again , we can observe equidistant placement of cells
# set::(FP_IO_MODE) 2
we can observe the floorplan has a I/O of equidistant 2

<img width="942" alt="placement layout" src="https://github.com/Shailaja9607/NASSCOM-VSD-SoC-Design-Program/assets/169365653/54b3d8b8-ac67-4417-8a7e-c106d067deab">

<img width="928" alt="after floorplan and placement cells with equidistant" src="https://github.com/Shailaja9607/NASSCOM-VSD-SoC-Design-Program/assets/169365653/cd735141-1cca-4e19-bfaf-45045ed83d45">
  
//  Day 3
// Cloning the inverter file through github
# cd Desktop/work/tools/openlane_working_dir/openlane git clone https:// github.com/nickson-jose/vsdstdcelldesign.git
<img width="831" alt="cloning vsdstdcelldesign from github" src="https://github.com/Shailaja9607/NASSCOM-VSD-SoC-Design-Program/assets/169365653/e0c5b54c-e3f0-4774-b103-09dcca170424">

# cd Desktop/work/tools/openlane_working_dir/pdks/sky130a/libs.tech magic 
# cp sky130A.tech/home/vsduser/desktop/work/tools/openlane_working_dir/openalne/vsdstdcelldesign
# magic -T sky130A.tech sky130_inv.mag &
<img width="947" alt="CMOS inv" src="https://github.com/Shailaja9607/NASSCOM-VSD-SoC-Design-Program/assets/169365653/5465293b-589f-45f4-a041-f3d50528a244">
<img width="943" alt="cmos inv layout" src="https://github.com/Shailaja9607/NASSCOM-VSD-SoC-Design-Program/assets/169365653/7ad761af-7a9a-4d40-9aa7-70335178e757">

# steps to run ngspice
<img width="743" alt="steps to run ngspice" src="https://github.com/Shailaja9607/NASSCOM-VSD-SoC-Design-Program/assets/169365653/2b81ad9c-fe06-4fc5-a8c2-96dd00c3c8a2">
//Spice file
<img width="710" alt="spice file" src="https://github.com/Shailaja9607/NASSCOM-VSD-SoC-Design-Program/assets/169365653/795efeae-a38a-4eea-a29a-fa1950eabaab">


























						
