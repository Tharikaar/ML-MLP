# Traditional ML vs MLP
## Highlight
* ข้อมูล Structured data ที่มีการทำ feature engineering แล้ว การทดลองตัวแบบระหว่าง Traditional ML และ MLP จะให้ค่า accuracy ไม่แตกต่างกันมาก 
* จากการทดลอง จะเห็นความแตกต่างของการปรับ Activation function in Hidden layer ซึ่งพบว่า การใช้ sigmoid ได้ค่าเฉลี่ยของ accuracy สูงกว่าการใช้ relu แม้จะทำการทดลองที่จำนวน layer และ batch sizeเท่ากัน 
* การกำหนดจำนวน hidden node และ hidden layer เยอะ ทำให้ค่า accuracy ดีขึ้นจริง แต่มีโอกาสที่จะไม่ส่งผลให้โมเดลดีขึ้น อาจทำให้ model เกิดการจดจำ data train set แต่ไม่เกิดการเรียนรู้ pattern ของ data test set ส่งผลให้เกิดการ overfit ได้ 
* การทดลองโดยตัวแบบ MLP ใช้เวลาและทรัพยากรที่สูงกว่า ตัวแบบ Traditional ML
### Introduction
การทดลองนี้จัดทำขึ้นเพื่อสร้างแบบลองสำหรับจำแนกระดับความน่าเชื่อถือของบุคคล  (Credit score classification) ออกเป็น 3 กลุ่ม ซึ่งอาศัยข้อมูลที่ธนาคารสามารถรวบรวมได้มาใช้เป็น input ของแบบจำลอง เพื่อใช้ในการอนุมัติสินเชื่อทางการเงิน  โดยการทดลองนี้มุ่งเน้นการเปรียบเทียบแบบจำลองที่มีความแตกต่างกันระหว่าง traditional machine learning และ deep learning
### Data
* Data source : [Credit score classification : Kaggle](https://www.kaggle.com/datasets/parisrohan/credit-score-classification?select=train.csv) <br />
ข้อมูลมีจำนวน 27 columns มีรายละเอียดดังนี้ <br />
Col1  | Col2  |  Col3 | Col4<br />
----- | ----- | ----- | ----- |<br />
Test1 | Test1 | Test1 | Test1 |<br />
Test2 | Test2 | Test2 | Test2 |<br />
Test3 | Test3 | Test3 | Test3 |<br />
