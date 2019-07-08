# Trafic Prediction in a Bike Sharing System (2015)
저자 : Yexin Li, Yu Zheng, Huichu Zhang, Lei Chen

<br><br><br>
  
### 클러스터 방법

#### Bipartite Station Clustering
Step 1. Geo-Clustering : Algorithm 최초 1회 때는 Step 1-1, 그 이후는 1-2를 수행합니다.
* Step 1-1. (최초 1회 수행)
  * 자전거 정류소의 위도, 경도 데이터를 기준으로 K-means Clustering을 통해 K1개의 Cluster를 만듭니다. 
  <br>

* Step 1-2. (1회 이후부터 수행)
  * T-Clustering 한 K2개의 Cluster 각각에 대해 1-1의 Geo-Clustering을 적용하여 총 K1개의 Cluster를 형성합니다. <br>
  -> T-Cluster에 Geo-clustering을 할 때 각각의 클러스터 개수 : [(N1*K1)/n], [(N2*K1)/n] , ... , [(NK2*K1)/n] <br>
    (이 부분은 아래의 그림을 참조하시면 이해가 빠를 수 있습니다.) 
    <br><br>
    
* Step 2. T-matrix Generation
  * 7개의 time slot을 만듭니다.
    
