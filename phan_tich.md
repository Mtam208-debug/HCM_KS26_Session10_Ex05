---


---

<h2 id="so-sánh-plain-text-và-rich-text">1. So sánh Plain Text và Rich Text</h2>
<p><a href="https://github.com/vanthuc14789/HCMK26_NhapMonCNTT_Session10_Ex06/blob/main/phan_tich.md#1-so-s%C3%A1nh-plain-text-v%C3%A0-rich-text"></a></p>
<p><strong>Plain Text</strong> là văn bản chỉ chứa nội dung chữ và ký tự, không có định dạng phức tạp. Ví dụ: file <code>.txt</code> hoặc <code>.md</code>.</p>
<p><strong>Rich Text</strong> là văn bản có thể chứa nhiều kiểu định dạng như màu sắc, phông chữ, hình ảnh và căn lề. Ví dụ: file Word <code>.docx</code>.</p>
<h3 id="so-sánh-hai-loại-văn-bản">So sánh hai loại văn bản</h3>
<p><a href="https://github.com/vanthuc14789/HCMK26_NhapMonCNTT_Session10_Ex06/blob/main/phan_tich.md#so-s%C3%A1nh-hai-lo%E1%BA%A1i-v%C4%83n-b%E1%BA%A3n"></a></p>
<p><strong>Plain Text:</strong></p>
<ul>
<li>
<p>Dung lượng thường nhẹ, dễ mở bằng nhiều phần mềm.</p>
</li>
<li>
<p>Nội dung ít bị ảnh hưởng khi chuyển giữa các hệ điều hành.</p>
</li>
<li>
<p>Dễ theo dõi thay đổi khi sử dụng Git Diff.</p>
</li>
<li>
<p>Markdown dùng ký tự như <code>#</code>, <code>*</code> để tạo tiêu đề và chữ in đậm.</p>
</li>
</ul>
<p><strong>Rich Text:</strong></p>
<ul>
<li>
<p>Có nhiều định dạng đẹp mắt như màu chữ, bảng và hình ảnh.</p>
</li>
<li>
<p>Phù hợp để soạn thảo báo cáo có bố cục phức tạp.</p>
</li>
<li>
<p>Có thể gặp vấn đề về định dạng khi mở bằng phần mềm khác.</p>
</li>
<li>
<p>Git Diff khó theo dõi nội dung thay đổi bên trong file <code>.docx</code> hơn so với file Markdown.</p>
</li>
</ul>
<h2 id="phân-tích-tình-huống-của-nam">2. Phân tích tình huống của Nam</h2>
<p><a href="https://github.com/vanthuc14789/HCMK26_NhapMonCNTT_Session10_Ex06/blob/main/phan_tich.md#2-ph%C3%A2n-t%C3%ADch-t%C3%ACnh-hu%E1%BB%91ng-c%E1%BB%A7a-nam"></a></p>
<p>Nam sử dụng Microsoft Word để viết tài liệu giới thiệu dự án GreenTech rồi đưa file <code>.docx</code> lên GitHub. Cách làm này vẫn sử dụng được, nhưng có một số hạn chế.</p>
<ul>
<li>
<p>Khi các thành viên cùng sửa file, việc xem chính xác nội dung nào đã thay đổi sẽ khó hơn.</p>
</li>
<li>
<p>File Word có cấu trúc và định dạng phức tạp nên Git Diff không hiển thị thay đổi thuận tiện như với file văn bản thuần.</p>
</li>
<li>
<p>Nếu file bị hỏng dữ liệu, khả năng mở và khôi phục nội dung còn phụ thuộc vào phần dữ liệu bị ảnh hưởng. Không phải cứ mất một byte là toàn bộ file chắc chắn bị hỏng.</p>
</li>
</ul>
<h2 id="giải-pháp-cho-dự-án-greentech">3. Giải pháp cho dự án GreenTech</h2>
<p><a href="https://github.com/vanthuc14789/HCMK26_NhapMonCNTT_Session10_Ex06/blob/main/phan_tich.md#3-gi%E1%BA%A3i-ph%C3%A1p-cho-d%E1%BB%B1-%C3%A1n-greentech"></a></p>
<p>Theo em, nhóm nên sử dụng Markdown để viết tài liệu giới thiệu dự án và lưu thành file <code>README.md</code> trên GitHub.</p>
<p>Lý do:</p>
<ul>
<li>
<p>Markdown dễ viết và dễ đọc.</p>
</li>
<li>
<p>File nhẹ, thuận tiện khi quản lý bằng Git.</p>
</li>
<li>
<p>Các thành viên dễ xem nội dung thay đổi qua Git Diff.</p>
</li>
<li>
<p>GitHub hỗ trợ hiển thị trực tiếp file <code>README.md</code>.</p>
</li>
</ul>
<p><strong>Kết luận:</strong> Word phù hợp với tài liệu cần trình bày phức tạp, còn Markdown phù hợp hơn với tài liệu dự án được quản lý trên GitHub. Vì vậy, nhóm GreenTech nên dùng <code>README.md</code> để giới thiệu dự án.</p>

