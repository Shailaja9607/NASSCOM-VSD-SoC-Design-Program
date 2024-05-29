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












						
