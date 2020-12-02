# AWS Reinvent 2020
* [運算](#computing) 
* [容器](#containers)  
* [儲存](#storage)  
* [資料庫](#database)  
* [分析](#analytics)  
* [ML/DL](#ml-dl)  
* [客戶互動](#customer-engagement)  
* [IoT](#iot)  
* [Hybrid](#hybrid)  

## <a id="computing"></a>運算

### EC2

- 新運算實體

	- [D3en](https://amz.run/44DI)、最大區域（local）儲存空間實體 (336TB、正式通用)
	- 只有 AWS 有、[MacOS 運算實體](https://amz.run/44DL) （正式通用）
- Graviton 2  
	- 搭載AWS Gravition2 ARM 處理器的運算實體
	- 在各種工作負載上、40% 更佳的價格/效能
		- [C6g](https://amz.run/44DB)、強化網路（預覽版）
		- [T4g](https://amz.run/44DG)、可高載執行 （正式通用）
- 基於 [Habana Gaudi 的 EC2 運算實體](https://amz.run/44DM)  
	- 2021年上半看開放
	- 支援英特爾 Habana Gaudi 處理器
	- 比現有基於 GPU 、機器學習訓練的運算實體最高好上 40% 的價格/效能 
	- 支援 TensorFlow 與 PyTorch
- [AWS Trainium](https://amz.run/44DP)  
	- 2021年可用
	- 在雲上提供最有價格競爭力的訓練、AWS 客製化設計的機器學習訓練晶片
	- 任何 ML 運算實體 每秒一萬億次浮點運算 （teraflops）
	- 使用了與 Inferentai 一樣的 Neuron SOK
	- 在 Amazon SageMaker或 EC2 上皆可使用

### AWS Lambda
- 簡要
	- 最多節省 70 % 成本的[毫秒計費](https://amz.run/44DT)（與 100毫秒相比）
- 支援 [Lambda 容器](https://amz.run/44DU)
	- 以 Docker 或是 OCI 容器打包程式碼與相依套件
	- 使用具相容性的容器映像檔與基於 Lambda 應用程式的一致性組合工具集
	- 部署建立在第三方容器映像檔之上的 Lambda functions

## <a id="containers"></a>容器
### 將容器移到雲上的管理挑戰
- [隨處可用的Amazon ECS](https://amz.run/44DX)
	- 2021年到來
	- 一樣的AWS風格的 ECS APIs、叢集管理、工作負載安排、和監控
	- 可在任何基礎設施上運行
	- 橫跨本地基礎設施和 AWS 的 ECS 無縫體驗
- [隨處可用的Amazon EKS](https://amz.run/44DY)
	- 2021年到來
	- 和在本地（on-premises）Kubernetes 叢集上設定、升級、與操作一樣的 EKS 體驗
	- 可在任何基礎設施上運行
	- 無縫 EKS 體驗
	- 橫跨本地基礎設施和 AWS 的Amazon EKS Distro
	- Amazon EKS Distro 開源

### 移動至更小單元運算的挑戰
- [AWS Proton](https://amz.run/44Da)（正式通用）
	- 首個容器與無伺服器應用程式的完全託管部署服務

## <a id="storage"></a>儲存
### 區塊儲存是頂基礎與最廣泛形式的儲存
- Amazon Elastic Block Store
	- EBS 的 [gp3](https://amz.run/44De) 磁碟區（正式通用）
	- 更高的 IOPS 與輸送量 的 [io2](https://amz.run/44De)
- [io2 Block Express](https://amz.run/44De)
	- 4倍 IOPS (最高256,000)、輸送量(4,000MB/s)、和儲存空間 (64TB)的io2
	- 只需要針對你需要的空間擴展、佈建、與付費
	- 良好的SAN 效能
	- 更多 SAN 功能在 2021 年到來: Multi-Attach, I/O Fencing, Fast Snapshot Restore, and Elastic Volumes

## <a id="database"></a>資料庫
- [Amazon Aurora Serverless V2](https://amz.run/44Dg)（預覽版）
	- 一秒鐘內可延展至數以萬計的資料庫交易
	- 在應用程式恰好所需的空間量方面、可細緻增加的擴增與縮減(scale up and down)
		- 峰值的佈建容量 vs 最多省 90 %
		- 支援多AZ、Global Database、讀取複本、回溯、與平行查詢
- [Aurora PostgreSQL 的 Babelfish](https://amz.run/44Dh)（預覽版）
	- 透過少許甚至不用改動程式碼的方式、在 Aurora PostgreSQL 上執行 SQL 伺服器應用程式
	- 一些細節
		- 不在對你不需要的 SQL 伺服器應用程式付費
		- 在 Aurora PostgreSQL 上嶄新的翻譯能力（translation capability）輕鬆執行 SQL 伺服器應用程式
		- 能知道 SQL 伺服器的proprietary dialect (T-SQL)、與通訊協定(TDS)
		- 透過 DMS 遷移資料、然後更新你的應用程式設定檔使其指向 Aurora 而不是 SQL 伺服器
- [PostgreSQL 的 Babelfish](https://amz.run/44Dj)
	- 2021年到來
	- 開源專案
	- 使用Apache 2.0 授權
	- 讓源碼可觸及好增加新功能
	- 2021在 Github 上開放

## <a id="analytics"></a>分析
### [AWS Glue Elastic Views](https://amz.run/44Dk)（預覽版）
- 輕鬆建立橫跨多種資料儲存（體）自動結合與複寫資料的物化檢視（materialized view）

## <a id="ml-dl"></a>ML/DL
### # Ask 2
- [Amazon SageMaker Data Wrangler](https://amz.run/44Dm)（正式通用）
	- 給機器學習準備資料的最快方式
- [Amazon SageMaker Feature Store](https://amz.run/44Dn)（正式通用）
	- 使儲存、更新、和分享 ML 特徵變得輕鬆的 repo
- [Amazon SageMaker Pipelines](https://amz.run/44E8)（正式通用）
	- 專特為 ML 打造的 CICD 服務  
- Amazon CodeGuru
	- 支援 Python（正式通用）
- [Amazon DevOps Guru](https://amz.run/44Du)（預覽版）
	- 透過機器學習在維運議題影響客戶前找出它們的新服務
- [Amazon QuickSight Q](https://amz.run/44Dv)（預覽版）
	- 透過自然語言詢問 Q 任何問題並在數秒內獲得解答

## <a id="customer-engagement"></a>客戶互動
### Amazon Connect
- Amazon Connect Wisdom（預覽版）
	- 透過機器學習給客服人員遞送他們在即時需要解決問題的產品和服務資訊
- Amazon Connect Customer Profiles（正式通用）
	- 給客服人員提供每一位客戶統一的檔案、在撥打中提供更多的個人化服務
- Real-Time Contact Lens for Amazon Connect（正式通用）
	- 在通話中即時辨認問題、影響客戶互動
- Amazon Connect Tasks（正式通用）
	- 替聯繫的客服中心人員自動化、追蹤、與管理任務
- Amazon Connect Voice ID（預覽版）
	- 使用ML賦能語音分析的撥打辨認

## <a id="#iot"></a>IoT
### 改善工業流程
- #1 機器資料
	- Amazon Monitron（正式通用）
		-設備監控的端到端解決方案
	- Amazon Lookout for Equipment（預覽版）
		- 機械工業的異常偵測服務
- #2 電腦視覺
	- Amazon Panorama Appliance（預覽版）
		- 讓企業在現有的本地照相機上具有電腦視覺（功能）的硬體裝置
	- Amazon Panorama SDK（預覽版）

## <a id="hybrid"></a>hybrid
### 嘗試將工作負載從本地移到雲端
- [兩種新大小的 AWS Outposts](https://amz.run/44Dy)
	- 2021 到來
	- 用到更少空間、在本地中運行 AWS 基礎設施、更小的Outposts

### [AWS 本地區域](https://amz.run/44Dw)  
- AWS 區域的延伸
- 遞送單位數毫秒的延遲給當地端使用者
- 2019年在洛杉磯發起
- 波士頓、休士頓、邁阿密可使用（預覽）
- 2021年多 12 個本地區域：亞特蘭大、芝加哥、達拉斯、丹佛、堪薩斯城、拉斯維加斯、明尼阿波利斯、紐約、費城、鳳凰城、波特蘭、和西雅圖

![](new_background.jpg)
