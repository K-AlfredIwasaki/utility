Replace NA in all columns with ""
```
df2 %>% replace(., is.na(.), "")
```
Replace NA in specified columns with ""
```
df %>% replace_na(list(x = 0, y = "unknown"))
```

