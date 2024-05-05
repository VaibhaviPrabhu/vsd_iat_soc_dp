This report consists of 5 days workshop on RTL to GDS-II flow by VSD-IAT. Each day is documented, for the theory the screenshots are taken from the website and for the labs the screenshots are attached from the system used. <br>
- [Day1](#Day1)
- [Day2](#Day2)
- [Day3](#Day3)
- [Day4](#Day4)
- [Day5](#Day5)

<a name="Day1"></a>
# Day1

## How to talk to computers
![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/944ac8e7-0cc4-419e-bd18-eb853867ba53)
|-
## SoC design and OpenLANE
Digital ASIC design consists of RTL IP’s, EDA Tools and PDK files. <br>
**1. RTL Design:** There are numerous RTL design open online sources like librecores.org, opencores.org, github.org, etc.  <br>
**2. EDA Tools:** The EDA tools previously used was SPICE simulator, SIS, Magic, and many others. Now, the EDA tools used are Qflow, OpenROAD, OpenLANE.  <br>
**3. PDK Files:** It is the Process Design Kit. It includes the process design rules, device models, digital standard cells, I/O libraries, … The first ever open source PDK was released by Google which is Skywater technology.  <br>
![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/0c188475-be27-456b-aba5-0b0ee5178894)
|-
![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/480c1cd6-186c-4b24-b0dd-087709b15f4a)
|-
![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/6f95c3a7-fd53-4cec-bf71-7452e5147f5a)
|-
## Familiarization of EDA tools
- Design Preparation Steps: 
```
cd tools/openlane_working_dir/openlane
docker
pwd
./flow.tcl -interactive
package require openlane 0.9
prep -design picorv32a
```
![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/ad41b978-1b7d-4b95-bdcf-d6cfdf236e7e)
|-

![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/b52b27c3-cb4d-4a4b-bb94-37db08375aa6)
|-

![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/3d743184-6c86-45f0-bfcb-a3402e24846e)
|-

![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/f961adce-edcf-4442-bdae-c753a96d1248)
|-

![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/2c2d14ca-8c8c-4da0-9a87-252a38bf4799)
|-

![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/0b8cf10d-73b3-4579-937f-62b22ee937d5)
|-


![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/cb00049e-05d3-41ae-b4c8-0e0a90090b41)
|-

![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/15d5531c-3231-4179-8076-8df5ac7b846e)
|-

- The GitHub repository for open lane is as follows: [Open Lane GitHub](https://github.com/The-OpenROAD-Project/OpenLane) <br>
- YouTube Playlist: [FOSSi Dial-Up](https://www.youtube.com/playlist?list=PLUg3wIOWD8yoZCg9XpFSgEgljx6MSdm9L) <br>

## Steps To Characterize Synthesis Results

![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/73c137f7-71d5-4b14-af3c-2ef9bc5d833b)
|-

![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/7039766c-8e9e-4365-b46d-1ff633bfc3fa)
|-


![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/08c56f52-c260-4fa7-af73-05a3c0225de1)
|-

Task: To calculate the flop ratio.
Flop Ratio = (No.  of D Flip-Flop)/(Total no.  of cells )
In our design, flop ratio = 1613/14876 = 10.8429 %


![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/73574591-42c0-4ff8-aeb6-7d0723260488)
|-


![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/6870445f-cd67-49b6-aa2d-1330362270f5)
|-


![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/9e9b6e19-66c6-4162-9287-be3369349e0b)
|-
<a name="Day2"></a>
# Day2
### Chip Floor Planning Considerations

![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/08286afd-ae1a-4616-a17e-8cc66e12ee0e)
|-


![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/5b9a9a13-382c-413d-8a5d-5ff363df8bfa)
|-


![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/a2c4dcb4-e91e-42f1-b01f-dcf066484449)
|-


![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/a006f206-a9d2-4a4e-8275-def6f56cb1ae)
|-


![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/f5733869-63ba-41e9-a15f-1e034717afec)
|-


![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/43b7394b-07e0-487c-9cb5-346ad55a9355)
|-


![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/643ee79b-2755-47f0-a7e2-3b8128feba9d)
|-


![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/50740906-5936-4d01-aa12-fc04da9a1805)
|-


![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/704d765a-7a2a-4089-bfac-7289f8a50aff)
|-


![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/f7e47a08-34f2-4e75-b51a-89c53a52b25b)
|-


![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/3cbd1ccb-1a6a-4f63-851f-7499461c6e01)
|-


![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/fffe3588-a1fd-44cc-ab32-c1ecfea6c3e8)
|-
#### Synthesis in OpenLANE
```
run_synthesis
```
![9](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/5b82948c-0f8f-44cd-bb58-5b49b69497d3)
|-

![10](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/04ac068d-0a69-42aa-a443-7488da8f5b67)
|-

### Floor Plan
```
run_floorplan
```
![11](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/63239290-a12b-453b-87ba-6dfb4271b60b)
|-

![12](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/b364bf5c-b89e-4e3b-b45f-39b2627815eb)
|-

![13](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/4f971da5-91ac-496a-8af0-f21c48ebefb0)
|-

To view the design in Magic we use the following command:
```
magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read picorv32a.floorplan.def &
```
![14](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/d1f1e831-2cb5-45a7-9a51-2b206fee2145)
|-

### Library Binding and Placement

![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/e9194b95-ab0f-441c-8ab1-3e06c3029fc8)
|-

- Netlist is the interconnection of the components in the design. The blocks of the design are all present in the library with information such as timing, delays, height, width and also various dimensions for the same block is also present in the library. 


![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/ed0842a7-5e9d-4b65-9b93-1e9b648b8960)
|-


![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/e5dfe82f-a184-42b7-ae62-e4d1e712c1a0)
|-

- Typical flow: Logic Synthesis ---> Floor Planning ---> Placement ---> Clock Tree Synthesis ---> Routing

![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/9500c19a-e269-46c0-857f-9bb0fd07257c)
|-

#### Placement
```
run_placement
```
To view the design in Magic we use the following command:
```
magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read picorv32a.placement.def &
``` 

![15](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/6bcaac9c-8de3-4c01-afe2-ea104eb96405)
|-

### Cell Design and Characterization Parameters

![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/9cab9bb3-c13c-4013-858a-a3e29208032b)
|-


![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/fc51e8c0-642a-44c5-a467-6eadfddc95f9)
|-


![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/67c7fb45-2d42-4a13-88cc-2e6769d7976b)
|-


![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/1b2485c5-e96e-4fac-add4-62b098923db2)
|-


![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/043a071b-9c98-4a9e-8d4f-d1d21dac0941)
|-


![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/755c6872-d8ae-41e6-870f-4afd2e83277d)
|-


![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/01591d50-65ad-47dd-a28f-36af89ad60bb)
|-


![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/e019f0e0-e1f1-4d19-964f-cec523128ee1)
|-

### General Timing Characterization Parameters

![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/aeaa0476-2f49-4938-b1e6-32b9ea7a3241)
|-

<a name="Day3"></a>
# Day3
### Labs for Inverter
The specifications can be directly updated in the bash. An example is changing the distance between the cells.

![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/c38d9b81-11cc-407d-8718-a7803724a935)
|-

![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/5ae4fa8e-c91e-49e3-875d-4a972cd6b091)
|-

![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/3e423339-591b-4102-81e9-923422247d9c)
|-

Link for Git Repository: [VSD_STD_Cell_Design](https://github.com/nickson-jose/vsdstdcelldesign) <br>
Command for clone
```
git clone https://github.com/nickson-jose/vsdstdcelldesign.git
```
![18](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/419204e5-4920-4b9a-a471-1a8dba4a40cd)
|-

![19](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/15fc2eab-fb88-4ad9-8d3a-213670971bf0)
|-

### Layout and CMOS Fabrication

![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/b49069ca-9a22-4340-bdba-d27ec6e68c94)
|-

![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/635846a6-5027-4783-a470-f7af751c6693)
|-

![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/a87b899e-121a-41ab-adbc-116a7301b731)
|-

![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/0c49d003-317a-4694-8237-4fec80a7183b)
|-

![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/f85269d1-3f20-4bb4-9b44-d1dc68cb163c)
|-

![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/0e0c13a3-e588-4739-8df4-c760e53feeaf)
|-

![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/e6221bb1-d3be-4902-b71c-4b5f3e43e629)
|-

![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/84670ef6-fc00-48e7-b733-88e61efe8a33)
|-

![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/c6cc1356-8b7c-474b-9ca9-85f51873d870)
|-

![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/882e6fb9-d013-4a59-90d7-bd5ed2692977)
|-

![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/1b7ec479-f9e8-440f-9a86-3894e9543526)
|-

![image](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/0ec8422f-c77d-4462-808b-fa17338517c4)
|-

![20](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/306ca7b9-e0e4-47a4-ab3f-282914e325ca)
|-

![21](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/df405089-faf7-417c-a28c-41b7cb5a99f5)
|-

![22](https://github.com/VaibhaviPrabhu/vsd_iat_soc_dp/assets/144148368/d2018cd6-38bd-4633-99b3-bf57cb4c0145)
|-
<a name="Day4"></a>
# Day4

<a name="Day5"></a>
# Day5
