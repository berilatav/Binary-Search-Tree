Merge Sort Project
### [7, 5, 1, 8, 3, 6, 0, 9, 4, 2] dizisinin Binary-Search-Tree aşamalarını yazınız.
##### İkili arama ağacı, her düğümün solundaki koldan ulaşılabilecek bütün verilerin düğümün değerinden küçük, sağ kolundan ulaşılabilecek verilerin değerinin o düğümün değerinden büyük olmasını şart koşar.

|     Açıklama    |  |  |  |
|--               |- |- |- |
|**root=7**       |  | 7|  |



**5 sayısı 7'den küçük olduğunda 7'nin soluna eklenmelir.**
|   Açıklama  |     |  |  |
|--           |-    |- |- |
|             |     |  | 7|  
|             |     | /|  | 
|**5 eklendi**|**5**|  |  | 


**1 sayısı 5'ten ve 7'den küçük olduğundan 7 ve 5'in soluna eklendi.** 
|     Açıklama  |     |  |  |  |  |
|             --|--   |--|- |- |- |
|               |     |  |  |  | 7|  
|               |     |  |  | /|  | 
|               |     |  | 5|  |  |  
|               |     | /|  |  |  | 
|**1 eklendi**  |**1**|  |  |  |  |

**8 sayısı 7'den büyük olduğundan 7'nin sağına eklendi.** 
| Açıklama      |  |  |  |  |  |  |     |
|--             |--|--|- |- |- |- |-    |
|               |  |  |  |  | 7|  |     |  
|               |  |  |  | /|  |\ |     | 
|**8 eklendi**  |  |  | 5|  |  |  |**8**| 
|               |  | /|  |  |  |  |     | 
|               | 1|  |  |  |  |  |     |

**3 sayısı  7'den ve 5'ten küçük  olduğundan 5'in soluna, 1'den büyük olduğundan 1'in sağına eklendi.**  
|  Açıklama     |  |  |     |  |  |  |  |
|--             |--|--|-    |- |- |- |- |
|               |  |  |     |  | 7|  |  |  
|               |  |  |     | /|  |\ |  | 
|               |  |  | 5   |  |  |  |8 | 
|               |  | /|     |  |  |  |  | 
|               | 1|  |     |  |  |  |  |
|               |  |\ |     |  |  |  |  |
|**3 eklendi**  |  |  |**3**|  |  |  |  |

**6 sayısı 7'den küçük  olduğundan 7'nin soluna, 5'ten büyük olduğundan 5'in sağına eklendi.**  
| Açıklama      |  |  |  |  |     |  |  |
|--             |--|--|- |- |-    |- |- |
|               |  |  |  |  | 7   |  |  |  
|               |  |  |  | /|     |\ |  | 
|               |  |  | 5|  |     |  |8 | 
|               |  | /|  |\ |     |  |  | 
| **6 eklendi** | 1|  |  |  |**6**|  |  |
|               |  |\ |  |  |     |  |  |
|               |  |  | 3|  |     |  |  |

**0 sayısı  7'den, 5'ten ve 1'den küçük olduğundan 1'in soluna eklendi.**  
| Açıklama       |     |  |  |  |  |  |  |  |  |
|--              |--   |--|- |- |- |- |- |- |- |
|                |     |  |  |  |  |  | 7|  |  |  
|                |     |  |  |  |  | /|  |\ |  | 
|                |     |  |  |  | 5|  |  |  |8 | 
|                |     |  |  | /|  |\ |  |  |  |
|                |     |  | 1|  |  |  |6 |  |  |
|                |     | /|  |\ |  |  |  |  |  |
| **0 eklendi**  |**0**|  |  |  | 3|  |  |  |  |

**9 sayısı  7'den ve 8'den büyük olduğundan 8'in sağına eklendi.**  
| Açıklama     |  |  |  |  |  |  |  |  |  |  |     |
|--            |--|--|- |- |- |- |- |- |- |- |-    |
|              |  |  |  |  |  |  | 7|  |  |  |     |  
|              |  |  |  |  |  | /|  |\ |  |  |     | 
|              |  |  |  |  | 5|  |  |  |8 |  |     | 
|              |  |  |  | /|  |\ |  |  |  |\ |     | 
| **9 eklendi**|  |  | 1|  |  |  |6 |  |  |  |**9**|
|              |  | /|  |\ |  |  |  |  |  |  |     |
|              | 0|  |  |  | 3|  |  |  |  |  |     |


**4 sayısı  7'den ve 5'ten küçük olduğundan 5'in soluna, 1'den ve 3'ten büyük olduğundan 3'ün sağına eklendi.** 
| Açıklama    |  |  |  |  |  |  |     |  |  |  |  |
|--           |--|--|- |- |- |- |-    |- |- |- |- |
|             |  |  |  |  |  |  | 7   |  |  |  |  |  
|             |  |  |  |  |  | /|     |\ |  |  |  | 
|             |  |  |  |  | 5|  |     |  |8 |  |  | 
|             |  |  |  | /|  |\ |     |  |  |\ |  |
|             |  |  | 1|  |  |  |6    |  |  |  | 9|
|             |  | /|  |\ |  |  |     |  |  |  |  |
|             | 0|  |  |  | 3|  |     |  |  |  |  |
|             |  |  |  |  |  |\ |     |  |  |  |  |
|**4 eklendi**|  |  |  |  |  |  |**4**|  |  |  |  |

**2 sayısı  7'den ve 5'ten küçük olduğundan 5'in soluna, 1'den büyük olduğundan 1'in sağına ve 3'ten küçük olduğundan 3'ün soluna eklendi.** 
| Açıklama    |  |  |     |  |  |  |  |  |  |  |  |
|--           |--|--|-    |- |- |- |- |- |- |- |- |
|             |  |  |     |  |  |  | 7|  |  |  |  |  
|             |  |  |     |  |  | /|  |\ |  |  |  | 
|             |  |  |     |  | 5|  |  |  |8 |  |  | 
|             |  |  |     | /|  |\ |  |  |  |\ |  | 
|             |  |  | 1   |  |  |  |6 |  |  |  | 9|
|             |  | /|     |\ |  |  |  |  |  |  |  |
|             | 0|  |     |  | 3|  |  |  |  |  |  |
|             |  |  |     | /|  |\ |  |  |  |  |  |
|**2 eklendi**|  |  |**2**|  |  |  |4 |  |  |  |  |
