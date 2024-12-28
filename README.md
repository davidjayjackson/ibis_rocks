# Plot Average Price for Avacoda by type
```
plt.figure(figsize=(10, 6))
sns.lineplot(data=df_mean, x='Date', y='mean_price', hue='type')
plt.title("Mean Price Over Time by Type")
plt.xlabel("Date")
plt.ylabel("Mean Price")
plt.legend(title="Type")
plt.show()

# Pivot so each 'type' becomes its own column of mean prices
df_pivoted = df_mean.pivot(index='Date', columns='type', values='mean_price')

# Plot each column (type) as a separate line
df_pivoted.plot(figsize=(10, 6))
plt.title("Mean Price Over Time by Type")
plt.xlabel("Date")
plt.ylabel("Mean Price")
plt.legend(title="Type")
plt.show()

```
