Date = ["19.1.2025" , "20.12.2025" , "21.12.2025" , "22.12.2025"]
Day = ["Mon" , "Tue" , "Wed" , "Thur"]
Sale = [2000 , 3000 , 1500 , 3000]
Order = [45 , 50 , 30 , 51]
print(f" {'Date':<12} {'Day':<10} {'Sale':<8} {'Order':<4} {'Apc':<6}")
print("-" * 45)
for i in range(4): 
    Apc = Sale[i] // Order[i]
    print(f"{Date[i]:<12} {Day[i]:<10} {Sale[i]:<8} {Order[i]:<4} {Apc:<6}")
total_sale = 0
total_order = 0
for i in range(4):

    total_sale  += Sale[i]
    total_order += Order[i]
print("-" * 45)
print(f"Weekly total sale: {total_sale:,} AED")
print(f"Weekly Avg APC: {total_sale // total_order} AED")
sale_chart = "weekly sale chart"
with open("my_sale_chart.txt", "w") as f:
    f.write(sale_chart)
print("sale_chart saved as my_sale_chart.txt")
