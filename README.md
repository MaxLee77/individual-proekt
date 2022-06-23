# individual-proekt

print(
    "Assalomu aleykum \nKeling elektron magazin uchun mahsulotlar ro'yxatini tuzamiz"
)
list_products = {}
while True:
    product = input("Birorta mahsulot kiriting: ")
    price_product = input(f"{product.title()}ni narxini kiriting:")
    list_products[product] = price_product
    javob = input("Yana mahsulot kiritasizmi? ha/yo'q: \n: ")
    if javob.lower() != "ha":
        print(list_products)
        break
    else:
        continue

print("Assalomu aleykum \nBozor ro'yxatini tuzamiz")
royxat = []
n = 1
while True:
    list = f"ro'yxatdagi {n}-mahsulotni kiriting: "
    mahsulot = input(list)
    royxat.append(mahsulot)
    javob = input("yana mahsulot kiritasizmi? ha/yo'q: ")
    if javob == "ha":
        n += 1
        continue
    else:
        break
while royxat:
    mah = royxat.pop()
    if mah in list_products.keys():
        narh = list_products[mah]
        print(f" {mah}- {narh} so'm")
    else:
        print(f"bizda {mah} yo'q")
