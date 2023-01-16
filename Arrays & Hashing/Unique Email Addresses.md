**Unique Email Addresses**

```java
class Solution {
    public int numUniqueEmails(String[] emails) {
        HashSet<String> hs=new HashSet<>();
        for(int i=0;i<emails.length;i++)
        {
            String str[]=emails[i].split("@");
            String local=str[0];
            String domain=str[1];
            String l[]=local.split("\\+");
            local=l[0];
            local=local.replace(".","");
            String s=local+"@"+domain;
            hs.add(s);
        }
        return hs.size();
    }
}
```

