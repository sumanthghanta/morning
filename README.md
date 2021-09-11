# morning

[rohit](Image/Image.jpg)


----

## recommended for food list

Food/item |  Location |  Amount (inr)  |

 ******   |*******    |  ********      |

biryani   |  hyderabad|    300         |

icecream  |  Bglr     |    100         |

MAnchuriya| Karimnagar|    200         |


------

## quotes
 
"Life is what happens when you’re busy making other plans." — Sumanth
“Get busy living or get busy dying.” — Stephen King

## Ternary search

https://cp-algorithms.com/data_structures/segment_tree.html

int sum(int v, int tl, int tr, int l, int r) {
    if (l > r) 
        return 0;
    if (l == tl && r == tr) {
        return t[v];
    }
    int tm = (tl + tr) / 2;
    return sum(v*2, tl, tm, l, min(r, tm))
           + sum(v*2+1, tm+1, tr, max(l, tm+1), r);
}