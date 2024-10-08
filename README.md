# Assignment-7
#To Determine the bearing capacity of soil with water table
Bulk_Density=float(input("Enter the value of Bulk Density of soil:"))
Salt_Density=float(input("Enter the value of Saturated Density of soil:"))
Water_Density=float(input("Enter the unit Weight of Water:"))
Df=float(input("Enter the value of depth of footing:"))
Dw=float(input("Enter the value of water table above footing level:"))
Dw1=float(input("Enter the value of Water table below the level of footing:"))
B=float(input("Enter the value of width of footing:"))
Nq=float(input("Enter the value of Nq:"))
N=float(input("Enter the value of N gamma (N):"))
Sub_Density=0
# You need to assign a value to SubDensity
Sat_Density=0
# You need to assign a value to SatDensity
Water_Density = 0
# You need to assign a value to WaterDensity
print("Submerged Weight of soil is:", Sub_Density)
# The bearing capacity of soil when water table is at ground
print("CASE A")
qu=(Sub_Density*Df*Nq) +(0.5*0.8*B*Sub_Density*N)
# Changed Ng to Nq
print("The value of ultimate bearing capacity of soil is:", qu)
# Approximate calculation of Bearing capacity of soil is.
Rw=0.5+0.5*(Dw/B)
print("The value of Rw is:",Rw)
Rw1=0.5+0.5*(Dw1/8)
print("The value of Rw1 is:",Rw1)
qu=(Bulk_Density*Df*Nq*Rw)+(0.5*0.8*3*Bulk_Density*N*Rw1)
# Changed Ng to Nq
print("The value ultimate bearing capacity of soil is:",qu)
# Case B
print("CASE B")
qu=(Bulk_Density*Df*Nq)+(0.5*0.8*8*Sub_Density)
# This line has a syntax error, it's unclear what the intended calculation is.
print("The value of ultimate bearing capacity is:",qu)
Dw=float(input("Enter the value of water table above footing level:"))
Dw1=float(input("Enter the value of Water table below the level of footing:"))
print("The approximate value of ultimate bearing capacity is:")
Rw=0.5+0.5*(Dw/B)
print("The value of Rw is:",Rw)
Rw1=0.5+0.5*(Dw1/8)
print("The value of Rw1 is:",Rw1)
qu=(Bulk_Density*Df*Nq*Rw)/(0.5+0.8*8*Bulk_Density*Rw1)
# Changed Ng to Nq and corrected NR1 to Rw1
print("The approximate value of ultimate hearing capacity is: ",qu)
# Case C
print("CASE C")
x=float(input("Enter the value of depth of water below footing:"))
# Assuming you have defined BulkDensity, SubDensity, B, and N elsewhere
qu=(Bulk_Density*Nq)+(0.5*0.8*((Bulk_Density*x)+ Sub_Density*(B - x))*N)
# Changed Ng to Nq
print("The value of ultimate bearing capacity is:",qu)
Dw=float(input("Enter the value of water table above footing level:"))
Dw1=float(input("Enter the value of Water table below the level of footing:"))
print("The approximate value of ultimate bearing capacity is:")
Rw=8.5+8.5*(Dw/B)
print("The value of Rw is:", Rw)
Rw1=0.5+0.5*(Dw1/8)
print("The value of Rwl is: ", Rw1)
qu=(Bulk_Density*Df*Nq*Rw)+(0.5*0.8*8*Bulk_Density*N*Rw1)
# Changed Ng to Nq and corrected the typo Bulk_Density to BulkDensity
print("the value of ultimate bearing capaciy is:",qu)
#Q-2
# To find the ultimate load carring capacity of pile
UCS=float(input("Enter the value of UCS of soil:"))
Cu=UCS/2
B=float(input("Enter the value of dimension of pile:"))
l=float(input("Enter the length of pile:"))
Alpha=float(input("Enter the value of adhesion factor:"))
Nc=float(input("The value of Nc: "))
Ab=B*B
print("the Base area of footing is:", Ab)
As=4*B*l
print("The value of chohesion of soil is:", Cu)
Qpu=Cu*Nc*Ab
print("Qpu:", Qpu)
Qf=Alpha*Cu*As
print("Qf:", Qf)
Qu=Qpu+Qf
print("the value of load carring capacity of pile is (Qu):", Qu)
#Q-3
# To Determine the bearing capacity of soil with water table
Bulk_Density = float (input("Enter the value of Bulk Density of soil:"))
Sat_Density = float (input("Enter the value of Saturated Density of soil:"))
Water_Density = float (input("Enter the unit Weight of Water:"))
Df = float(input("Enter the value of depth of footing:"))
B = float(input("Enter the value of width of footing:"))
Ng = float(input("Enter the value of Ng:"))
N_Gamma =float(input("Enter the value of N gamma (N):"))
Sub_Density = Sat_Density - Water_Density
print("Submerged Weight of soil is:", Sub_Density)
M = int(input("Number of data values of Water table above footing level: "))
N = int(input("Number of data values of Water table below footing level: "))
Dw=[]
Dw1=[]
for i in range (1, M+1) :
  print("Enter the value of water table above footing level measured w.r.t.ground (Dw) : ")
  Depth_Dw = float (input ())
  Dw.append(Depth_Dw)
  Rw=0.5+0.5*(Depth_Dw/B)
  print ("The value of Rw is:", Rw)
for j in range (1, N+1):
  print("Enter the value of water table above footing level measured w.r.t.ground (Dw1): ")
  Depth_Dw1 = float (input())
  Dw.append (Depth_Dw1)
  Rw1 = 0.5 + 0.5*(Depth_Dw1/B)
  print ("The value of Rw1 is:", Rw1)
  qu= (Bulk_Density*Df*Nq*Rw)+(0.5*0.8*B*Bulk_Density*N_Gamma*Rw1)
  print ("qu: ", qu, "kN/m^2")
