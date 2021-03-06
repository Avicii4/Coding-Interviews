# 整数中1出现的次数（从1到n整数中1出现的次数）

**题目描述：**

求出 1~13 的整数中 1 出现的次数,并算出 100~1300 的整数中 1 出现的次数？为此他特别数了一下1~13中包含1的数字有 1、10、11、12、13 因此共出现 6 次,但是对于后面问题他就没辙了。ACMer 希望你们帮帮他，并把问题更加普遍化，可以很快的求出任意非负整数区间中1出现的次数（从1 到 n 中1出现的次数）。

**分析：**

1. 如果第 m 位（自右至左，从 1 开始标号）上的数字为0，则第 m 位可能出现 1 的次数由更高位决定（若没有高位，视高位为 0），等于更高位数字 × 当前位数的权重 10<sup> *i-1*</sup>。

2. 如果第 m 位上的数字为 1，则第 m 位上可能出现 1 的次数不仅受更高位影响，还受低位影响（若没有低位，视低位为 0），等于更高位数字 × 当前位数的权重 10<sup> *i-1*</sup> + (低位数字+1)。

3. 如果第 m 位上的数字大于 1，则第 m 位上可能出现 1 的次数仅由更高位决定（若没有高位，视高位为0），等于 (更高位数字 +1) × 当前位数的权重 10<sup> *i-1*</sup>。

结合代码分析。根据第二个一般化的代码，第 [*lg* i + 1] 位数字大于 certainNumber，结果是其高位 +1 后与 i 的积；第 [*lg* (i) + 1] 位数字小于 certainNumber，结果是其高位与 i 的积；第 [*lg*(i) + 1] 位数字等于 certainNumber，结果是其高位与 i 的积加上其低位数字 +1。

