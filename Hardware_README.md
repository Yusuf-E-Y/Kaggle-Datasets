
# Video Game Console Generations & Hardware Sales Dataset (1972-2026)

## Konsol Pazarı (Nesillere Göre)
```text
1. Nesil   | 2.35M
2. Nesil   |██ 41.5M
3. Nesil   |████ 75.91M
4. Nesil   |███████████ 220.4M
5. Nesil   |███████ 148.1M
6. Nesil   |███████████████ 296.3M
7. Nesil   |███████████████████████████ 507.0M  <-- Zirve Noktası (Akıllı Telefon Öncesi)
8. Nesil   |█████████████ 251.5M
9. Nesil   |████████████ 241.46M (2026 Güncel)
```

## Örnek Python Kullanımı

```python
import pandas as pd

# Veri setini yükle
df = pd.read_csv("Hardware-Generation.csv")

# 1. En çok satan 5 konsol
top_5 = df.sort_values(by="Sales_Million", ascending=False).head(5)
print("--- Tüm Zamanların En Çok Satan 5 Konsolu ---")
print(top_5[["Console_Name", "Manufacturer", "Sales_Million"]])

# 2. Üreticilere göre toplam donanım satışı payları
brand_shares = df.groupby("Manufacturer")["Sales_Million"].sum().sort_values(ascending=False)
print("\n--- Üretici Şirketlerin Toplam Pazar Payları (Milyon) ---")
print(brand_shares)
```

---
