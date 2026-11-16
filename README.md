# Prompt 
```markdow
Context:Bạn là một chuyên viên phân tích dữ liệu đánh giá khách hàng và bạn muốn phân loại các đánh giá của khách hàng để dễ dàng phản hồi.
Request:
Phân tích các phản hồi của khách hàng để phân loại:
- Cảm xúc chính (Sentiment): Positive (Tích cực), Negative (Tiêu cực), hoặc Neutral (Trung lập).
- Chủ đề chính (Topic): Product (Sản phẩm), Delivery (Giao hàng), Service (Dịch vụ), System (Hệ thống/App).
- Điểm số hài lòng (Satisfaction Score): Thang điểm từ 1 đến 5.
Explanation:không thêm bớt câu từ nào của khách hàng,giữ nguyên các câu từ đánh giá cốt lõi của khách hàng.
Action:
Bước 1:Dữ liệu các đánh giá của khách hàng được đưa vào.
Bước 2:Phân loại các đánh giá thành các trường Positive,Negative hoặc Neutral.
Bước 3:Xuất kết quả dưới dạng Json.
Tone:Chính xác,khách quan,chuyên nghiệp.
Extras:Trả kết quả dưới dạng json.
Ví dụ:

Ví dụ 1 (Positive):
- Input: "Ứng dụng mượt mà, nhân viên CSKH hỗ trợ cực kỳ nhiệt tình và nhanh chóng, rất hài lòng!"
- Output:
{
  "sentiment": "Positive",
  "topics": ["System", "Service"],
  "score": 5,
  "summary": "App mượt và CSKH nhiệt tình"
}

Ví dụ 2 (Negative):
- Input: "Giao hàng cực kỳ nhanh nhưng sản phẩm nhận được lại bị móp méo, thất vọng quá."
- Output:
{
  "sentiment": "Negative",
  "topics": ["Delivery", "Product"],
  "score": 2,
  "summary": "Giao hàng nhanh nhưng sản phẩm bị móp méo"
}

Ví dụ 3 (Neutral):
- Input: "Sản phẩm dùng tạm ổn, giao hàng bình thường như mọi đơn vị khác."
- Output:
{
  "sentiment": "Neutral",
  "topics": ["Product", "Delivery"],
  "score": 3,
  "summary": "Sản phẩm và giao hàng ở mức bình thường"
}
```
[RÀNG BUỘC KỸ THUẬT]
- Chỉ trả về duy nhất một chuỗi, tuyệt đối không bọc trong markdown code block (như ```json) hay thêm bất kỳ văn bản giải thích nào khác.
[RÀNG BUỘC KỸ THUẬT]
- Chỉ trả về duy nhất một chuỗi, tuyệt đối không bọc trong markdown code block (như ```json) hay thêm bất kỳ văn bản giải thích nào khác.
```
