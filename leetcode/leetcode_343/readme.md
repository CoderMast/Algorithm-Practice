## 动态规划

这道题目的解决方法，最先能想到的就是动态规划，最核心的还是确定 dp 数组。

dp[i] 代表的是，将数字 i 分割后的最大乘积。

得到 dp[i] 有两种途径

- 分成 i - j 和 j，且均不再分割，故 dp[i] = (i - j) * j
- 分成 i - j 和 j，但这里需要对 i - j 进行分割，那么 dp[i] = Max(dp[i - j] * j , dp[i]);

则 dp[i] = Max(dp[i],dp[i - j] * j,(i - j) * j);

三者的最大值。