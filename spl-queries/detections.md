# Failed Password Detection

```spl
index=main "password check failed"
| stats count by host
```

# Sudo Activity Monitoring

```spl
index=main sudo
| timechart span=1h count
```

# Authentication Monitoring

```spl
index=main auth
| timechart span=1h count
```

#Top Log Sources

```spl
index=main
| top source
```
