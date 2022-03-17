# Thực hiện Phân tích gộp với R: Hướng dẫn thực hành

---

[![Twitter URL](https://img.shields.io/twitter/url/https/twitter.com/MathiasHarrer.svg?style=social&label=MathiasHarrer)](https://twitter.com/MathiasHarrer)
[![Twitter URL](https://img.shields.io/twitter/url/https/twitter.com/pimcuijpers.svg?style=social&label=pimcuijpers)](https://twitter.com/pimcuijpers)
[![Twitter URL](https://img.shields.io/twitter/url/https/twitter.com/pimcuijpers.svg?style=social&label=Toshi_FRKW)](https://twitter.com/Toshi_FRKW)
[![Twitter URL](https://img.shields.io/twitter/url/https/twitter.com/DDEbert.svg?style=social&label=DDEbert)](https://twitter.com/DDEbert)
[![Twitter URL](https://img.shields.io/twitter/url/https/twitter.com/ntluong95.svg?style=social&label=LuongNT)](https://twitter.com/ntluong95)



<a href="https://bookdown.org/MathiasHarrer/Doing_Meta_Analysis_in_R/" target="_blank"><img src="images/cover.png" width="250" align="right" alt="" class="cover" /></a> Chào mừng bạn đã tới kho lưu trữ GitHub của cuốn sách <a href="https://bookdown.org/MathiasHarrer/Doing_Meta_Analysis_in_R/" target="_blank"><strong>"Thực hiện Phân tích gộp với R: Hướng dẫn thực hành"</strong></a>.

Cuốn sách này đóng vai trò giới thiệu các cách tiếp cận để có thể tiến hành các phân tích gộp bằng ngôn ngữ _R_. Các bước cơ bản để tiến hành phân tích gộp sẽ được đề cập, bao gồm tổng hợp các đo lường đầu ra, forest plots, phân tích tính không đồng nhất (heterogeneity), phân tích theo nhóm (subgroup analyses), hồi quy gộp (meta-regression), các phương pháp để kiểm soát sai số xuất bản (publication bias), đánh giá nguy cơ sai số và các công cụ vẽ biểu đồ. 

Các chủ đề nâng cao, nhưng có liên quan như phân tích gộp mạng tương quan (network meta-analysis), phân tích gộp đa/ba tầng (multi-/three-level meta-analyses), phân tích gộp sử dụng cách tiếp cận Bayesian (Bayesian meta-analysis), và phân tích gộp mô hình hệ phương trình cấu trúc (SEM meta-analysis) cũng được đề cập. 

Nền tảng lập trình và thống kê được đề cập trong cuốn sách được giữ ở cấp độ dành cho người **không chuyên**. **Bản in** của cuốn sách này đã được xuất bản tại [Chapman & Hall/CRC Press](https://www.routledge.com/Doing-Meta-Analysis-with-R-A-Hands-On-Guide/Harrer-Cuijpers-Furukawa-Ebert/p/book/9780367610074) (Taylor & Francis).


<br></br>

## Kho lưu trữ mã nguồn mở 

---

Cuốn sách này được viết bằng package [**{rmarkdown}**](https://rmarkdown.rstudio.com/docs/) và [**{bookdown}**](https://bookdown.org/). Các công thức được hiển thị bằng [MathJax](http://docs.mathjax.org/en/latest/index.html). Tất cả các tài liệu và mã nguồn chúng tôi đã sử dụng để viết cuốn sách này có thể được tìm thấy trong kho lưu trữ này. Bạn có thể tự do phân nhánh, chia sẻ và sử dụng lại nội dung. Tuy nhiên, mục đích của kho lưu trữ chủ yếu là "read-only"; Cách Pull Request (PRs) nói chung sẽ không được xem xét (xem phần bên dưới & [Lời nói đầu](https://bookdown.org/MathiasHarrer/Doing_Meta_Analysis_in_R/preface.html#contact-us) của cuốn sách để biết cách liên hệ với chúng tôi).   



<br></br>

## Đóng góp 

---

Hướng dẫn này là một dự án mã nguồn mở và chúng tôi đặc biệt cảm ơn các cộng tác viên chuyên gia của mình, những người đã cung cấp nội dung bổ sung trong một số chương của cuốn sách này.

* [**Luke A. McGuinness**](https://twitter.com/mcguinlu), University of Bristol: Chương 15, Các biểu đồ nguy cơ sai số.
* [**Luong Nguyen Thanh**](https://www.linkedin.com/in/ntluong95/), Uppsala University: Dịch giả phiên bản Tiếng Việt của cuốn sách này.

Bạn muốn tự mình đóng góp vào hướng dẫn này? Hãy gửi email tới **Mathias** (mathias.harrer@fau.de) và cho chúng tôi biết về các đề xuất bổ sung của bạn.

<br></br>

## Trích dẫn cuốn sách này 

---

Trích dẫn được đề xuất là:

```{block, type='boxempty'}
Harrer, M., Cuijpers, P., Furukawa, T.A., & Ebert, D.D. (2021). _Doing Meta-Analysis with R: A Hands-On Guide_. Boca Raton, FL and London: Chapmann & Hall/CRC Press. ISBN 978-0-367-61007-4.
```

Tải trích dẫn xuống dưới dạng [BibTeX](https://www.protectlab.org/meta-analysis-in-r/data/citation.bib) hoặc [.ris](https://www.protectlab.org/meta-analysis-in-r/data/citation.ris).


<br></br>


## Trích dẫn các Packages 

---

Trong hướng dẫn này, chúng tôi trình bày và sử dụng các packages _R_ khác nhau. Lý do tại sao tất cả chúng ta có thể sử dụng các gói này miễn phí là vì các chuyên gia trên khắp thế giới đã dành rất nhiều thời gian và nỗ lực cho sự phát triển của họ, điển hình là không phải trả phí. Nếu bạn sử dụng một số gói được đề cập trong cuốn sách này cho phân tích tổng hợp của riêng mình, chúng tôi đặc biệt khuyến khích bạn cũng nên trích dẫn chúng trong báo cáo của mình. 

Trong cuốn sách này, mỗi khi một package mới được giới thiệu, chúng tôi cũng cung cấp thông tin tham khảo để bạn có thể trích dẫn nó. Thực hiện bằng cách gõ lệnh `citation("package")` để lấy thông tin trích dẫn. Xin cám ơn!


<br></br>
