# Insertion Sort Analizi

## Soru Açıklaması
Verilen `[22, 27, 16, 2, 18, 6]` dizisinde, aşağıdaki görevler yerine getirilecek:

1. Diziyi sıralamak için **Insertion Sort** algoritmasının adımlarını yazmak.
2. Algoritma için Big-O gösterimini belirtmek.
3. Diziyi sıraladıktan sonra `18` sayısını aramak için **time complexity** durumunu (best, average ya da worst) belirlemek.

---

## Çözüm

### Insertion Sort Adımları
Insertion Sort algoritmasını kullanarak `[22, 27, 16, 2, 18, 6]` dizisini adım adım sıralıyoruz:

1. **İlk dizi**: `[22, 27, 16, 2, 18, 6]`
2. `27` ile `22`'yi karşılaştıralım. Değişiklik yapmayız: `[22, 27, 16, 2, 18, 6]`
3. `16` sayısını `27` ve `22` ile karşılaştıralım. `16` sayısını doğru konuma yerleştirelim: `[16, 22, 27, 2, 18, 6]`
4. `2` sayısını `27`, `22` ve `16` ile karşılaştıralım. `2` sayısını doğru konuma yerleştirelim: `[2, 16, 22, 27, 18, 6]`
5. `18` sayısını `27`, `22` ve `16` ile karşılaştıralım. `18` sayısını doğru konuma yerleştirelim: `[2, 16, 18, 22, 27, 6]`
6. `6` sayısını `27`, `22`, `18` ve `16` ile karşılaştıralım. `6` sayısını doğru konuma yerleştirelim: `[2, 6, 16, 18, 22, 27]`

**Dizinin sıralanmış hali**: `[2, 6, 16, 18, 22, 27]`

---

### Big-O Gösterimi
Insertion Sort algoritmasının time complexity şu şekildedir:

- **Best case**: \(O(n)\) (dizi zaten sıralı ise).
- **Worst case**: \(O(n^2)\) (dizi tersten sıralı ise).
- **Average case**: \(O(n^2)\).

---

### `18` Sayısı İçin Time Complexity
Başta verilen dizinin sıralandıktan sonraki durumu şöyledir: `[2, 6, 16, 18, 22, 27]`. Şimdi `18`sayısının konumunu analiz edelim:

- **Best case**: Aranan sayı ilk elemandır (`18` başta olmadığı için bu durum geçerli değildir).
- **Worst case**: Aranan sayı son elemandır (`18` sonda olmadığı için bu durum geçerli değildir).
- **Average case**: Aranan sayı ortadadır. `18` dizinin ortasında olduğu için, **average case** geçerlidir.

---

## Son Kısım
1. **Adımlar**: Diziyi sıralamak için yukarıdaki adımlara bakın.
2. **Big-O Gösterimi**: Average case için \(O(n^2)\).
3. **Time Complexity Durumu**: The search for `18` corresponds to the **average case**.

---

# Selection Sort Analizi

## Soru Açıklaması
Verilen `[7, 3, 5, 8, 2, 9, 4, 15, 6]` dizisi için Selection Sort algoritmasına göre ilk 4 adımını yazmak.

---

## Çözüm

### Selection Sort Adımları
Selection Sort algoritmasını kullanarak `[7, 3, 5, 8, 2, 9, 4, 15, 6]` dizisini adım adım sıralıyoruz:

1. **1. Adım**: Dizideki en küçük elemanı bulalım ve ilk elemanla değiştirelim:
   - En küçük eleman: `2`
   - `2` ile `7` sayılarının yerlerini değiştirelim.
   - **1. Adım** uygulandıktan sonra dizinin son hali: `[2, 3, 5, 8, 7, 9, 4, 15, 6]`

2. **2. Adım**: Dizinin kalan sıralanmamış bölümündeki en küçük elemanı bulalım (indeks 1'den başlayarak) ve ikinci elemanla değiştirelim:
   - En küçük eleman: `3`
   - Değişikliğe gerek yok (zaten doğru konumda)
   - **2. Adım** uygulandıktan sonra dizinin son hali: `[2, 3, 5, 8, 7, 9, 4, 15, 6]`

3. **3. Adım**: Dizinin kalan sıralanmamış bölümündeki en küçük elemanı bulalım (indeks 2'den başlayarak) ve üçüncü elemanla değiştirelim:
   - En küçük eleman: `4`
   - `4` ile `5` sayılarının yerlerini değiştirelim.
   - **3. Adım** uygulandıktan sonra dizinin son hali: `[2, 3, 4, 8, 7, 9, 5, 15, 6]`

4. **4. Adım**: Dizinin kalan sıralanmamış bölümündeki en küçük elemanı bulalım (indeks 3'ten başlayarak) ve dördüncü elemanla değiştirelim:
   - En küçük eleman: `5`
   - `5` ile `8` sayılarının yerlerini değiştirelim.
   - **4. Adım** uygulandıktan sonra dizinin son hali: `[2, 3, 4, 5, 7, 9, 8, 15, 6]`

---

## Son Kısım
1. **1. Adım**: `[2, 3, 5, 8, 7, 9, 4, 15, 6]`
2. **2. Adım**: `[2, 3, 5, 8, 7, 9, 4, 15, 6]`
3. **3. Adım**: `[2, 3, 4, 8, 7, 9, 5, 15, 6]`
4. **4. Adım**: `[2, 3, 4, 5, 7, 9, 8, 15, 6]`
