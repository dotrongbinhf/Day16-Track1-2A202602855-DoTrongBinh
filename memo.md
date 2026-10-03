# Memo Teardown — Claude (Anthropic)

**Họ tên:** Đỗ Trọng Bình - 2A202602855

**Vì sao chọn sản phẩm này:** Claude có AI trực tiếp thực hiện việc đọc, viết và phân tích; nguồn công khai đủ để dựng hơn 6 mốc quyết định. Memo tập trung vào sự chuyển dịch từ trả lời câu hỏi sang hoàn thành công việc tri thức.

**Ngày chốt phân tích:** 03/10/2026. Phạm vi: trợ lý Claude trên web/desktop; model và API được xét khi mở khả năng làm việc mới. Dữ kiện có link trực tiếp trong memo. AI hỗ trợ nghiên cứu và đề xuất bản phân tích ban đầu; tôi đã đọc, xác nhận và chỉnh sửa câu chữ cùng một số nội dung trước khi hoàn thiện bài.

**Nguồn khai phá CP0:** AI đã mở [release notes chính thức](https://support.claude.com/en/articles/12138966-release-notes), [trang launch Product Hunt](https://www.producthunt.com/products/claude/launches/claude-sonnet-5) và [phỏng vấn founder Dario Amodei](https://lexfridman.com/dario-amodei-transcript), nghiên cứu 33 mốc ứng viên rồi chọn 8 mốc dưới đây.

**§1. Timeline các cập nhật lớn**

| Thời điểm | Cập nhật | Context lúc đó | Nguyên lý |
|---|---|---|---|
| 14/03/2023 | **Ra mắt trợ lý Claude**, chat/API cho đọc, viết và lập trình. [Ra mắt](https://www.anthropic.com/news/introducing-claude). | Mở rộng sau alpha với Notion, Quora và DuckDuckGo; công bố nhấn mạnh độ tin cậy và khả năng làm theo yêu cầu. | **Định nghĩa “tốt”:** đáp ứng đúng ý và hành vi đáng tin là tiêu chuẩn chất lượng của trợ lý. |
| 11/05/2023 | **Context 9K → 100K tokens qua API**, xử lý tập tài liệu dài. [100K](https://www.anthropic.com/news/100k-context-windows). | Khách hàng đã tích hợp Claude; báo cáo, nghiên cứu và tài liệu kỹ thuật cần tổng hợp trên nhiều trang. | **x10:** context tăng hơn 11 lần mở loại tác vụ mới; chưa chứng minh năng suất tăng 10 lần. |
| 06/2024* | **Artifacts preview**, xem và sửa tài liệu/code cạnh chat, cùng Sonnet 3.5. [Artifacts](https://www.anthropic.com/news/claude-3-5-sonnet). | Coding được cải thiện; [GPT-4o ra 13/05/2024](https://openai.com/index/hello-gpt-4o/) nhấn mạnh tương tác đa phương thức. | **Định nghĩa “tốt”:** đầu ra phải chỉnh sửa và phát triển tiếp được, nối model với sản phẩm cụ thể. |
| 25/06/2024 | **Projects**, tài liệu/chỉ dẫn theo dự án cho Pro/Team, chia sẻ hội thoại cho Team. [Projects](https://www.anthropic.com/news/projects). | Sonnet 3.5 và Artifacts đã có; bài ra mắt nêu thiếu ngữ cảnh nội bộ khi bắt đầu tác vụ. | **Wrapper/moat:** tổ chức kiến thức và quy trình quanh model tạo chi phí thiết lập lại; moat bền vững chưa được chứng minh. |
| 15/04/2025 | **Research + Google Workspace beta**, nghiên cứu nhiều bước với trích dẫn. [Research](https://claude.com/blog/research). | Web search có từ tháng 3; [OpenAI deep research ra 02/02/2025](https://openai.com/index/introducing-deep-research/). Chưa đủ để kết luận động cơ đáp trả. | **Wrapper/moat:** kết nối dữ liệu công việc làm kết quả phù hợp hoàn cảnh riêng; không đồng nghĩa sở hữu dữ liệu khách hàng. |
| 09/09/2025 | **Tạo/chỉnh sửa file preview**, Excel, Word, PowerPoint và PDF. [Tạo file](https://claude.com/blog/create-files). | Sau Research và Artifacts, môi trường máy tính riêng cho phép chạy code để tạo đầu ra. | **Định nghĩa “tốt”:** nghiệm thu bằng file bàn giao được trong quy trình tiếp theo. |
| 12/01/2026 | **Cowork research preview**, ban đầu Max/macOS, file cục bộ và MCP trong VM. [Release notes](https://support.claude.com/en/articles/12138966-release-notes). | Đưa năng lực agent của Claude Code vào desktop cho công việc ngoài lập trình. | **x10:** giao mục tiêu nhiều bước thay cho điều phối từng thao tác; đây là hướng thiết kế, chưa có đo lường x10. |
| 16/09/2026 | **Hợp nhất Cowork và chat**, bắt đầu rollout Pro/Max, Docs/Slides beta. [Hợp nhất](https://claude.com/blog/cowork-is-now-claude). | User phản hồi khó chọn nơi giao việc và ngữ cảnh không chuyển giữa các khu vực. | **Vòng lặp học:** triển khai → nhận phản hồi → sửa trải nghiệm; không phải tự động huấn luyện model bằng hội thoại. |

\* Dùng tháng vì trang Artifacts hiện ghi 21/06/2024, ngày công bố ban đầu chưa đối chiếu xong. Trạng thái/gói trong bảng là tại thời điểm ra mắt; tên nguyên lý theo đề bài, chưa đối chiếu tài liệu buổi học.

**Vì sao chọn những mốc này:** Tám mốc thay đổi loại việc được giao, ngữ cảnh sử dụng hoặc cách nhận đầu ra. Artifacts giữ quá trình cộng tác trong Claude, còn tạo file mở bước bàn giao ra ngoài nên cả hai được giữ. Android, Haiku và rollout web search toàn cầu bị loại vì chủ yếu mở kênh, đổi lựa chọn model hoặc mở rộng tiếp cận; các quyết định đó ít giải thích trục công việc đã chọn hơn, chứ không phải không quan trọng.

**§2. Tệp user & JTBD**

Hai tệp dưới đây là lát cắt có trường hợp cụ thể, chưa chứng minh tệp nào chiếm đa số. Early adopters ở đây là người dùng web năm 2023, không đại diện toàn bộ khách hàng API đầu tiên.

| | Early adopters | Tệp hiện tại |
|---|---|---|
| Đặc điểm | Người ứng tuyển vị trí giảng dạy, biết các chatbot OpenAI, tự đưa CV/mô tả tuyển dụng vào prompt để xử lý hồ sơ dài. | Người phụ trách vận hành tại công ty dịch vụ sổ sách, lương và HR cho doanh nghiệp nhỏ; chịu trách nhiệm báo cáo khách hàng. |
| Người cụ thể | **u/lulz_lurker**, [Reddit 07/2023](https://www.reddit.com/r/ChatGPT/comments/152e374/claudeai_is_nice/): hồ sơ giảng dạy 7 phần, 25 trang. Danh tính tự khai, chưa xác minh ngoài Reddit. | **Chris Scott, COO HireEffect, Dallas**, [case 15/09/2026](https://claude.com/blog/claude-for-small-business-launches-new-workflows-integrations-and-training-programs): tìm giao dịch gây lệch sổ; công ty dựng báo cáo từ QuickBooks/CRM. Case do Anthropic xuất bản. |
| JTBD chính | “Khi nộp hồ sơ giảng dạy nhiều phần, tôi muốn biến kinh nghiệm trong CV thành câu trả lời phù hợp yêu cầu tuyển dụng, để hoàn thành hồ sơ nhất quán và kiểm tra trước khi nộp.” | “Khi số liệu khách hàng không khớp hoặc đến kỳ báo cáo, tôi muốn tìm nguyên nhân và tổng hợp kết quả dễ giải thích, để bàn giao đúng hạn và quyết định bước xử lý.” |
| Trước đó họ làm bằng cách nào | Suy luận: tự đọc, viết và sửa từng phần; hoặc thử ChatGPT theo từng yêu cầu. Nguồn không mô tả đầy đủ workflow cũ. | Nguồn nói tác vụ báo cáo tháng từng mất hai giờ. Suy luận: lấy dữ liệu từng hệ thống rồi đối chiếu/tổng hợp thủ công; chưa xác nhận mọi thao tác. |
| Cột mốc mở đường ở §1 | **100K context (05/2023)** mở xử lý tài liệu dài; quyền tiếp cận web còn đến từ [Claude 2 (07/2023)](https://www.anthropic.com/news/claude-2), khác mốc API. | **Projects (06/2024), Research (04/2025), tạo file (09/2025), Cowork (01/2026)** tạo nền tảng xử lý việc lặp lại. Không khẳng định HireEffect dùng đủ bốn tính năng. |

**Dịch chuyển tệp:** Từ người tự ghép prompt cho một việc cá nhân sang người cần quy trình lặp lại và đầu ra bàn giao cho khách hàng. Cowork là bước nối trực tiếp vì mở thực hiện nhiều bước ngoài coding; hai case cho thấy mở rộng cách dùng, chưa chứng minh tệp cũ bị thay thế.

**Switching cost (map 4 forces):** Cùng một chiều phân tích: người đang dùng Claude cân nhắc chuyển việc sang công cụ khác hoặc cách làm thủ công.

| Lực | Cơ chế và bằng chứng |
|---|---|
| **Push — bất mãn với hiện tại** | Lỗi và giới hạn ngắt công việc. [Charles, GetApp 27/02/2025](https://www.getapp.za.com/reviews/2082505/claude) cần tạo trò chơi đào tạo, gặp kết quả sai/giới hạn và hủy gói trả phí. JTBD thất bại: hoàn thành tài liệu đúng, liền mạch. |
| **Pull — sức hút giải pháp mới** | Đối thủ làm cùng việc đúng hơn, ít sửa/gián đoạn hơn sẽ hút tác vụ; đây là điều kiện kiểm tra. [Niklas, GetApp 10/09/2024](https://www.getapp.za.com/reviews/2082505/claude) vẫn dùng GPT để kiểm tra hoặc làm việc ít quan trọng: có thể dùng song song. |
| **Anxiety — lo ngại khi chuyển** | Phải kiểm tra lại chất lượng, xử lý dữ liệu khách hàng và khả năng tái tạo quy trình. Suy luận: tệp vận hành chịu trách nhiệm đầu ra nên rào cản thử lại cao hơn người làm một hồ sơ. |
| **Habit — quán tính hiện tại** | Đã quen chỉ dẫn, kiểm tra kết quả và workflow trong Claude. Dashboard/skill riêng ở HireEffect gợi ý chi phí dựng lại, thử lại và hướng dẫn đồng nghiệp; chưa có bằng chứng tương đương ở case cá nhân. |

**Lực giữ mạnh nhất:** Với tệp vận hành lặp lại, **Habit của workflow đã thiết lập**, kèm Anxiety về tái kiểm chứng, là phán đoán mạnh nhất; chưa có đo retention. Nếu chuyển workflow dễ dàng, lực này giảm và lựa chọn quay về độ đúng, sự liền mạch, chi phí mỗi việc; Push do lỗi có thể thắng Habit. [Xuất hội thoại](https://support.claude.com/en/articles/9450526-export-your-claude-data) và [xuất memory](https://support.claude.com/en/articles/12123587-import-and-export-your-memory-from-claude) đã được hỗ trợ, nên không coi dữ liệu là khóa cứng hay mặc nhiên coi cộng đồng là moat.

**§3. Ba dự đoán hướng đi (6–12 tháng tới)**

Chốt ngày **03/10/2026**; đánh giá trong **03/04–03/10/2027**, hạn cuối **03/10/2027**. Chỉ tính đúng khi nguồn chính thức xác nhận đủ phạm vi; đây là phán đoán, không phải roadmap.

**Dự đoán 1** *(loại: mở rộng tính năng)*

- **Dự đoán:** Anthropic công bố cả **Claude Docs và Claude Slides đạt GA cho Enterprise**.
- **Lập luận:** §1 nối Artifacts → tạo file → hợp nhất chat/Cowork; §2 cho thấy tệp vận hành cần bàn giao được. [Release notes 16/09/2026](https://support.claude.com/en/articles/12138966-release-notes) vẫn ghi beta trên Enterprise, nên hoàn thiện độ ổn định là bước hợp lý.

**Dự đoán 2** *(loại: mở rộng segment)*

- **Dự đoán:** Anthropic ra **bộ workflow chính thức riêng cho công ty dịch vụ kế toán**, kèm thiết lập ngữ cảnh/quyền truy cập tách theo khách hàng.
- **Lập luận:** Projects/Cowork ở §1 mở quy trình riêng; §2 ghi nhận [HireEffect](https://claude.com/blog/claude-for-small-business-launches-new-workflows-integrations-and-training-programs) dùng đối soát/báo cáo. Đóng gói công việc lặp lại mở sâu hơn bộ SMB chung; workshop hay phân quyền chung chưa đủ tính đúng.

**Dự đoán 3** *(loại: mở rộng tính năng)*

- **Dự đoán:** **Portal nhà phát triển plugin** thêm cả thống kê lỗi thực thi và thời gian chạy, theo workflow/lệnh.
- **Lập luận:** Vòng phản hồi (09/2026) ở §1 và việc hủy gói do gián đoạn ở §2 gợi ý cần giúp builder sửa nút thắt. [Portal 25/09/2026](https://claude.com/blog/build-plugins-for-claude) mới mô tả cài đặt/khám phá; [smart reports Enterprise](https://support.claude.com/en/articles/16893491-get-started-with-smart-reports) đã có không được tính là chức năng mới của portal.

**Phản biện:** Tự tin nhất ở **dự đoán 1**, vì nối nhu cầu bàn giao với công cụ đã beta. Giả định: chỉnh sửa/xuất file đạt độ đúng cần thiết và Anthropic tiếp tục ưu tiên Docs/Slides trong Enterprise; chất lượng không đạt hoặc đổi hướng làm dự đoán gãy. Chỉ một công cụ GA hay tiếp tục mở beta đều chưa đủ.

**§4. AI Log**

AI ở đây là **Codex trong hội thoại này**. Tôi chọn sản phẩm, đọc và xác nhận bản phân tích, chỉnh sửa câu chữ cùng một số nội dung, đồng thời quyết định phạm vi bài nộp. AI hỗ trợ tìm thông tin, dẫn link nguồn, tổng hợp, gợi ý insight và soạn bản nháp. Việc tôi xác nhận nội dung không đồng nghĩa đã tự mở và đối chiếu từng link; các bước kiểm tra nguồn do AI thực hiện được ghi riêng dưới đây.

| Việc | AI làm hay bạn làm? | Bạn kiểm chứng/phán đoán lại thế nào? |
|---|---|---|
| Chọn sản phẩm và phạm vi bài nộp | **Tôi** chọn Claude và yêu cầu bài cá nhân, chỉ nộp `memo.md`; **AI hỗ trợ** đối chiếu tiêu chí và tổ chức bài. | Tôi xác nhận lựa chọn sản phẩm và yêu cầu bỏ file phụ. AI kiểm tra nguồn công khai cho tiêu chí có AI, đủ mốc và use case rõ. |
| Tìm thông tin và dẫn nguồn | **AI hỗ trợ** tìm, mở và tổng hợp nguồn; nghiên cứu 33 mốc ứng viên. | AI đối chiếu link gốc, phân biệt launch/rollout và preview/GA; giữ nguồn cho 8 mốc được chọn. Tôi đã đọc bản tổng hợp; ngày Artifacts còn chưa chốt được chính xác nên giữ chú thích. |
| Dựng timeline và gợi ý nguyên lý | **AI** đề xuất 8 mốc, bối cảnh và cách map nguyên lý; **tôi** đọc và xác nhận bản phân tích. | Tôi rà soát nội dung trong quá trình đọc và biên tập. AI hỗ trợ tách dữ kiện khỏi suy luận: context x10 chưa chứng minh năng suất x10, workflow chưa chứng minh moat. |
| Phân tích user, JTBD và 4 forces | **AI hỗ trợ** tìm case/review, gợi ý insight và soạn phân tích; **tôi** đọc, xác nhận nội dung bài. | AI ghi rõ giới hạn của Reddit, case do Anthropic xuất bản và workflow cũ suy luận. Bài giữ các giới hạn này; chưa có phỏng vấn, thử nghiệm trực tiếp hoặc đo retention. |
| Xây dựng ba dự đoán | **AI** đề xuất dự đoán, lập luận và mức tự tin; **tôi** đọc và xác nhận phần phân tích trước khi hoàn thiện. | AI kiểm tra hiện trạng để tránh dự đoán điều đã có, bổ sung thời hạn và điều kiện bác bỏ. Việc xác nhận không biến dự đoán thành dữ kiện hay roadmap chính thức. |
| Chỉnh sửa câu chữ | **Tôi** trực tiếp biên tập câu chữ; **AI hỗ trợ** bản nháp và cách tổ chức ý. | Tôi đọc lại và chỉnh cách diễn đạt trong memo. AI không ghi thay danh sách câu cụ thể vì tôi chưa cung cấp chi tiết các thay đổi. |
| Rà soát và chỉnh sửa nội dung | **Tôi** đọc, xác nhận và điều chỉnh một số nội dung; **AI hỗ trợ** thông tin, link nguồn và góc nhìn để tham khảo hoặc kiểm chứng. | Tôi xác nhận đã thực hiện bước rà soát và chỉnh sửa. Log ghi nhận ở mức này, không mặc định tôi đã tự tìm mọi nguồn, chọn lại toàn bộ mốc hoặc lập luận hoàn toàn độc lập. |
| Hoàn thiện cấu trúc và AI Log | **Tôi** quyết định phạm vi nộp và yêu cầu cập nhật vai trò; **AI hỗ trợ** sửa file, kiểm tra cấu trúc và khai báo đóng góp. | AI kiểm tra đủ 4 phần, 8 mốc, 3 dự đoán kèm lập luận và các ô AI Log; cập nhật việc tôi đã đọc, xác nhận, chỉnh sửa, đồng thời giữ rõ vai trò AI trong bản nháp ban đầu. |

**Phản biện CP4:** AI đóng góp nhiều nhất ở nghiên cứu và chuỗi lập luận ban đầu: chọn mốc → diễn giải nguyên lý → đề xuất JTBD → dự đoán. Tôi đã đọc, xác nhận và chỉnh sửa bài; phần tự giải thích không nhìn bản nháp chưa được ghi nhận trong log. Ba ý để tự bảo vệ là: Artifacts phục vụ cộng tác trong Claude, tạo file phục vụ bàn giao; workflow đã thiết lập có thể tạo chi phí chuyển đổi; dự đoán GA phụ thuộc chất lượng đầu ra và ưu tiên Enterprise. Đây là lập luận cần đánh giá, không phải kết luận được bảo đảm chỉ vì AI đề xuất.
