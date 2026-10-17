---


---

<h1 id="🌱-🚀-smart-farm-–-hệ-thống-tưới-lan-thông-minh">🌱 🚀 Smart-Farm – Hệ thống tưới Lan thông minh</h1>
<p><a href="https://github.com/vanthuc14789/HCMK26_NhapMonCNTT_Session10_Ex05/blob/main/README.md#--smart-farm--h%E1%BB%87-th%E1%BB%91ng-t%C6%B0%E1%BB%9Bi-lan-th%C3%B4ng-minh"></a></p>
<blockquote>
<p><em>Smart-Farm ứng dụng IoT để theo dõi môi trường và hỗ trợ tưới nước cho trang trại Lan an toàn, tiết kiệm.</em></p>
</blockquote>
<h2 id="giới-thiệu-dự-án">1. Giới thiệu dự án</h2>
<p><a href="https://github.com/vanthuc14789/HCMK26_NhapMonCNTT_Session10_Ex05/blob/main/README.md#1-gi%E1%BB%9Bi-thi%E1%BB%87u-d%E1%BB%B1-%C3%A1n"></a></p>
<p>Smart-Farm thu thập dữ liệu từ cảm biến, xử lý dữ liệu trên bộ điều khiển và quyết định khi nào cần tưới. Người nông dân có thể theo dõi nhiệt độ, độ ẩm đất và trạng thái máy bơm.</p>
<p>Hệ thống là mô hình minh họa. Ngưỡng tưới và thiết bị cần được kiểm tra, hiệu chỉnh theo điều kiện thực tế của vườn Lan.</p>
<h2 id="hướng-dẫn-cài-đặt">2. Hướng dẫn cài đặt</h2>
<p><a href="https://github.com/vanthuc14789/HCMK26_NhapMonCNTT_Session10_Ex05/blob/main/README.md#2-h%C6%B0%E1%BB%9Bng-d%E1%BA%ABn-c%C3%A0i-%C4%91%E1%BA%B7t"></a></p>
<h3 id="thiết-bị-cần-có">2.1. Thiết bị cần có</h3>
<p><a href="https://github.com/vanthuc14789/HCMK26_NhapMonCNTT_Session10_Ex05/blob/main/README.md#21-thi%E1%BA%BFt-b%E1%BB%8B-c%E1%BA%A7n-c%C3%B3"></a></p>
<ul>
<li>Raspberry Pi hoặc bộ điều khiển tương thích.</li>
<li>Cảm biến nhiệt độ/độ ẩm không khí và cảm biến độ ẩm đất.</li>
<li>Mạch relay phù hợp với máy bơm.</li>
<li>Nguồn điện đúng thông số của từng thiết bị.</li>
<li>Kết nối mạng nếu cần giám sát từ xa.</li>
</ul>
<h3 id="cài-đặt-môi-trường">2.2. Cài đặt môi trường</h3>
<p><a href="https://github.com/vanthuc14789/HCMK26_NhapMonCNTT_Session10_Ex05/blob/main/README.md#22-c%C3%A0i-%C4%91%E1%BA%B7t-m%C3%B4i-tr%C6%B0%E1%BB%9Dng"></a></p>
<p>Mở Terminal và kiểm tra Python:</p>
<pre><code>python3 --version

</code></pre>
<p>Tạo môi trường ảo và cài các thư viện ví dụ:</p>
<pre><code>python3 -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
python -m pip install gpiozero

</code></pre>
<p>Trên Windows, kích hoạt môi trường ảo bằng <code>.venv\\Scripts\\activate</code>. Lệnh điều khiển GPIO chỉ chạy trên phần cứng và hệ điều hành tương thích. Hãy cài thêm thư viện cảm biến đúng với mẫu thiết bị đang dùng.</p>
<h3 id="chạy-chương-trình">2.3. Chạy chương trình</h3>
<p><a href="https://github.com/vanthuc14789/HCMK26_NhapMonCNTT_Session10_Ex05/blob/main/README.md#23-ch%E1%BA%A1y-ch%C6%B0%C6%A1ng-tr%C3%ACnh"></a></p>
<p>Lưu chương trình vào <code>smart_farm.py</code>, kiểm tra cấu hình chân GPIO và ngưỡng tưới trước khi chạy:</p>
<pre><code>python smart_farm.py

</code></pre>
<p>Không nối máy bơm trực tiếp vào chân GPIO. Dùng mạch điều khiển phù hợp, có bảo vệ điện và kiểm tra hệ thống khi máy bơm chưa nối tải.</p>
<h2 id="tính-năng">3. Tính năng</h2>
<p><a href="https://github.com/vanthuc14789/HCMK26_NhapMonCNTT_Session10_Ex05/blob/main/README.md#3-t%C3%ADnh-n%C4%83ng"></a></p>
<ul>
<li>Đọc dữ liệu nhiệt độ và độ ẩm từ cảm biến.</li>
<li>So sánh độ ẩm đất với ngưỡng tưới đã cấu hình.</li>
<li>Bật/tắt máy bơm thông qua mạch relay phù hợp.</li>
<li>Hiển thị trạng thái hoạt động cho người vận hành.</li>
<li>Lưu nhật ký để theo dõi và tìm lỗi.</li>
<li>Kiểm tra cảnh báo khi cảm biến mất kết nối hoặc dữ liệu bất thường.</li>
</ul>
<h2 id="bảng-thông-số-tham-khảo">4. Bảng thông số tham khảo</h2>
<p><a href="https://github.com/vanthuc14789/HCMK26_NhapMonCNTT_Session10_Ex05/blob/main/README.md#4-b%E1%BA%A3ng-th%C3%B4ng-s%E1%BB%91-tham-kh%E1%BA%A3o"></a></p>
<p>Thành phần</p>
<p>Thông số / vai trò</p>
<p>Ghi chú</p>
<p>Cảm biến nhiệt độ</p>
<p>Ví dụ: DHT22</p>
<p>Chọn theo môi trường và yêu cầu độ chính xác</p>
<p>Cảm biến độ ẩm đất</p>
<p>Loại điện dung hoặc loại phù hợp</p>
<p>Hiệu chuẩn theo loại đất và giá thể</p>
<p>Bộ điều khiển</p>
<p>Raspberry Pi hoặc thiết bị tương thích</p>
<p>Cần kiểm tra chân giao tiếp</p>
<p>Mạch relay</p>
<p>Theo điện áp và dòng tải của máy bơm</p>
<p>Không điều khiển tải công suất lớn trực tiếp bằng GPIO</p>
<p>Máy bơm</p>
<p>Theo thiết kế hệ thống tưới</p>
<p>Dùng nguồn riêng đúng định mức</p>
<p>Kết nối</p>
<p>Wi-Fi hoặc LAN</p>
<p>Cần thiết nếu có giám sát từ xa</p>
<p>Ngưỡng tưới</p>
<p>Ví dụ: độ ẩm đất dưới 30%</p>
<p>Giá trị minh họa, phải hiệu chỉnh thực tế</p>
<h2 id="sơ-đồ-hệ-thống">5. Sơ đồ hệ thống</h2>
<p><a href="https://github.com/vanthuc14789/HCMK26_NhapMonCNTT_Session10_Ex05/blob/main/README.md#5-s%C6%A1-%C4%91%E1%BB%93-h%E1%BB%87-th%E1%BB%91ng"></a></p>
<p><a href="https://github.com/vanthuc14789/HCMK26_NhapMonCNTT_Session10_Ex05/blob/main/images/so-do-smart-farm.svg"><img src="https://github.com/vanthuc14789/HCMK26_NhapMonCNTT_Session10_Ex05/raw/main/images/so-do-smart-farm.svg" alt="Sơ đồ hệ thống Smart-Farm: cảm biến gửi dữ liệu đến bộ điều khiển, bộ điều khiển ra lệnh qua relay để vận hành máy bơm; dữ liệu có thể gửi lên màn hình hoặc đám mây."></a></p>
<p>Luồng cơ bản: <strong>Cảm biến → Bộ điều khiển/SoC → Mạch relay → Máy bơm</strong>. Dữ liệu trạng thái có thể được gửi đến giao diện giám sát.</p>
<h2 id="cpu-xử-lý-lệnh-tưới-theo-chu-kỳ-fetch–decode–execute">6. CPU xử lý lệnh tưới theo chu kỳ Fetch–Decode–Execute</h2>
<p><a href="https://github.com/vanthuc14789/HCMK26_NhapMonCNTT_Session10_Ex05/blob/main/README.md#6-cpu-x%E1%BB%AD-l%C3%BD-l%E1%BB%87nh-t%C6%B0%E1%BB%9Bi-theo-chu-k%E1%BB%B3-fetchdecodeexecute"></a></p>
<blockquote>
<ol>
<li><strong>Fetch (Lấy lệnh):</strong> CPU lấy lệnh tiếp theo của chương trình từ bộ nhớ.</li>
<li><strong>Decode (Giải mã):</strong> CPU giải mã lệnh để xác định thao tác cần thực hiện.</li>
<li><strong>Execute (Thực thi):</strong> CPU thực hiện phép tính hoặc thao tác, chẳng hạn so sánh giá trị độ ẩm với ngưỡng và yêu cầu bộ điều khiển bật/tắt relay.</li>
</ol>
<p>Chu kỳ này diễn ra liên tục khi chương trình chạy. Lệnh bật máy bơm vẫn phải đi qua phần mềm và mạch điều khiển phù hợp; CPU không cấp điện trực tiếp cho máy bơm.</p>
</blockquote>
<h2 id="mô-hình-dikw-từ-dữ-liệu-đến-hành-động">7. Mô hình DIKW: từ dữ liệu đến hành động</h2>
<p><a href="https://github.com/vanthuc14789/HCMK26_NhapMonCNTT_Session10_Ex05/blob/main/README.md#7-m%C3%B4-h%C3%ACnh-dikw-t%E1%BB%AB-d%E1%BB%AF-li%E1%BB%87u-%C4%91%E1%BA%BFn-h%C3%A0nh-%C4%91%E1%BB%99ng"></a></p>
<ol>
<li><strong>Data – Dữ liệu:</strong> Cảm biến ghi nhận nhiệt độ <code>32°C</code> và độ ẩm đất <code>25%</code>.</li>
<li><strong>Information – Thông tin:</strong> Hệ thống xác định nhiệt độ đang cao và độ ẩm đất thấp hơn ngưỡng cài đặt <code>30%</code>.</li>
<li><strong>Knowledge – Kiến thức:</strong> Theo quy tắc đã hiệu chỉnh cho vườn Lan, đất dưới ngưỡng có thể cần được tưới; cần kiểm tra cảm biến và điều kiện thực tế.</li>
<li><strong>Wisdom – Trí tuệ / quyết định:</strong> Hệ thống quyết định bật máy bơm trong thời gian giới hạn, theo dõi lại độ ẩm và dừng tưới khi đạt điều kiện an toàn.</li>
</ol>
<pre><code>             /----------------------\
            /  WISDOM – Quyết định   \
           /--------------------------\
          / KNOWLEDGE – Quy tắc tưới   \
         /------------------------------\
        / INFORMATION – Ý nghĩa dữ liệu  \
       /----------------------------------\
      / DATA – Giá trị cảm biến thô        \
     /--------------------------------------\

</code></pre>
<p>Các giá trị trên chỉ là ví dụ. Nhiệt độ cao không tự động có nghĩa là cần tưới; quyết định nên dựa vào độ ẩm đất, ngưỡng được hiệu chuẩn và giới hạn an toàn.</p>
<h2 id="kiến-thức-soc-và-ipo">8. Kiến thức SoC và IPO</h2>
<p><a href="https://github.com/vanthuc14789/HCMK26_NhapMonCNTT_Session10_Ex05/blob/main/README.md#8-ki%E1%BA%BFn-th%E1%BB%A9c-soc-v%C3%A0-ipo"></a></p>
<ul>
<li><strong>SoC (System on a Chip):</strong> Một chip tích hợp nhiều thành phần của hệ thống, có thể gồm CPU và các bộ điều khiển ngoại vi. Cấu hình cụ thể phụ thuộc thiết bị.</li>
<li><strong>IPO (Input – Process – Output):</strong>
<ul>
<li><strong>Input:</strong> Nhiệt độ, độ ẩm đất, cấu hình và lệnh người dùng.</li>
<li><strong>Process:</strong> Bộ điều khiển đọc dữ liệu, CPU chạy chương trình và so sánh với ngưỡng.</li>
<li><strong>Output:</strong> Hiển thị thông số, cập nhật nhật ký và điều khiển relay/máy bơm.</li>
</ul>
</li>
</ul>
<h2 id="lưu-ý-an-toàn-và-xử-lý-khi-ram-đầy">9. Lưu ý an toàn và xử lý khi RAM đầy</h2>
<p><a href="https://github.com/vanthuc14789/HCMK26_NhapMonCNTT_Session10_Ex05/blob/main/README.md#9-l%C6%B0u-%C3%BD-an-to%C3%A0n-v%C3%A0-x%E1%BB%AD-l%C3%BD-khi-ram-%C4%91%E1%BA%A7y"></a></p>
<p>Nếu RAM tăng cao do chương trình ghi nhật ký quá nhiều, hệ thống có thể chậm hoặc dừng hoạt động. Thực hiện theo thứ tự an toàn:</p>
<ol>
<li>Kiểm tra mức sử dụng RAM bằng <code>free -h</code> trên Linux hoặc <code>top</code>.</li>
<li>Xác định tiến trình gây tăng RAM; không kết thúc tiến trình hệ thống một cách tùy tiện.</li>
<li>Kiểm tra cấu hình ghi log. Dùng xoay vòng nhật ký (log rotation), giới hạn dung lượng và thời gian lưu.</li>
<li>Không lưu toàn bộ nhật ký vào một biến hoặc danh sách trong RAM; ghi theo từng dòng hoặc theo lô nhỏ.</li>
<li>Sao lưu log cần thiết trước khi dọn dẹp. Không dùng lệnh xóa hàng loạt như <code>rm -rf</code> khi chưa xác minh đường dẫn.</li>
<li>Nếu máy bơm đang chạy, chuyển hệ thống về trạng thái an toàn theo quy trình vận hành trước khi khởi động lại chương trình.</li>
<li>Chỉ khởi động lại dịch vụ khi đã xác định nguyên nhân và có thể kiểm tra lại cảm biến, relay, máy bơm sau đó.</li>
</ol>
<p><strong>Khuyến nghị:</strong> Đặt cảnh báo khi RAM vượt ngưỡng vận hành đã kiểm thử, giới hạn kích thước log và kiểm tra trạng thái máy bơm độc lập với việc ghi log.</p>
<h2 id="kiểm-thử-trước-khi-bàn-giao">10. Kiểm thử trước khi bàn giao</h2>
<p><a href="https://github.com/vanthuc14789/HCMK26_NhapMonCNTT_Session10_Ex05/blob/main/README.md#10-ki%E1%BB%83m-th%E1%BB%AD-tr%C6%B0%E1%BB%9Bc-khi-b%C3%A0n-giao"></a></p>
<ul>
<li>So sánh số đo cảm biến với thiết bị đo tham chiếu.</li>
<li>Thử tình huống độ ẩm thấp hơn ngưỡng.</li>
<li>Thử tình huống độ ẩm bằng hoặc cao hơn ngưỡng.</li>
<li>Kiểm tra máy bơm dừng khi chương trình kết thúc hoặc gặp lỗi.</li>
<li>Kiểm tra mất kết nối cảm biến và phản ứng an toàn.</li>
<li>Kiểm tra nhật ký có giới hạn dung lượng và RAM ổn định.</li>
<li>Hướng dẫn người vận hành cách dừng hệ thống khẩn cấp.</li>
</ul>

