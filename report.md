Data mining report guideline:

MN có thể tham khảo mấy notebook ở trên kaggle để viết

# introduction, objective các thứ

# dataset analysis and extraction(từ này dùng có đúng k)

Có thể viết lại code ở trong link này và chạy thử, tùy
Nếu lười thì chỉ cần copy lại các ảnh với paraphrase các phân tích của ông này trong phần 1 và 2 thôi

https://www.kaggle.com/astandrik/simple-anime-recommendation-system-content-based

Conclusion của phần này:
Về anime: chỉ sử dụng các feature sau để recommend: genre, sử dụng onehot encoded vector để biểu diễn (), views(số user đã xem)

Về user: chỉ nghiên cứu những user đã xem từ 250 đến 800 => giảm bớt khối lượng data để phân tích, loại bớt noise để cluster cho dễ hơn

# method

## approach (để t viết)

## theoretical background

- TSNE for visualization
- K-means for clustering
- Gaussian mixture model for clustering

# results and discussion
## results để t viết
## discussion:

- no testing and validating method
- scalability: dataset quá to nên phương pháp chạy quá chậm, đặc biệt là tsne và gmm
- khi sử dụng dataset đã đực giảm size, kq có thể k chính xác
- nói ra thêm một vài vde tùy mn rồi đề xuất giải pháp thôi