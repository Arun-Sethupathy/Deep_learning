#exp1 test case1
def xor(a,b):
  return a ^ b
test_inputs=[[0,0],[0,1],[1,0],[1,1]]
print("Test Input (X) Expected output (Y)")
for pair in test_inputs:
  output=xor(pair[0],pair[1])
  print(f"{str(pair):22} {output}")
  OUTPUT:
  <img width="251" height="85" alt="Screenshot 2025-08-13 102710" src="https://github.com/user-attachments/assets/5ff920b5-03e3-475f-bb5a-391f56bb6961" />
