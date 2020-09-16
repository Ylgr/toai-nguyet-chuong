---
layout: blog
title: "Lập trình không code - Phần 1: JAMstack"
date: 2020-09-16T14:05:28.200Z
top_image: /images/uploads/jam-stack-2700x740.png
tags:
  - lập trình
  - giới thiệu
  - tech
categories:
  - Lập trình
---
*Lời nói đầu*

Như đã chia sẻ từ đầu, mình là một lập trình viên, tất nhiên là sẽ có những bài viết về chủ đề Tech. Seri về Tech đầu tiên của mình sẽ bắt đầu từ khái niệm lập trình không code, tận dụng những công nghệ có sẵn để phát triển ra những sản phẩm cá nhân hoặc thương mại nhanh gọn nhẹ, tiết kiện thời gian và chi phí cho việc phát triển.

<!--more-->

Tất cả những công cụ mà mình chia sẻ trong seri này mặc dù rất tuyệt, giải quyết được rất nhiều vấn đề và nhu cầu cá nhân hay tập thể tuy nhiên chúng không toàn vẹn. Nếu bạn muốn có một blog và thêm tính năng hiển thị gallery ảnh hay search bài viết, sẽ có những plugin hỗ trợ bạn. Nếu bạn muốn những tính năng xử lý đọc những trang web khác rồi so sánh nội dung, hãy thử ... tới mùa quýt cũng không tìm được plugin hỗ trợ, bạn sẽ cần kỹ năng code hoặc một người biết code để xử lý những việc này.

# 1. Kiến trúc JAMstack

![kiến trúc JAMstack](/images/uploads/jamstack-delivers-v1.png "kiến trúc JAMstack")

Tấm hình trên là tóm tắt toàn bộ nội dung của mục này. Giải thích ra thì JAMstack là một kiến trúc sử dụng Javascript để render client, tích hợp API để custom hay tích hợp với các sản phẩm của bên thứ 3 và sử dụng Markup là template cũng như nội dung để tạo nên trang web.

JAMstack không phải là:

\- Những trang web server-site CMS: Wordpress, Joombla, Drupla.

\- Web app dựng trên kiến trúc monolith.

\- Single page app.

Ưu điểm của JAMstack giúp người sử dụng:

\- Đạt hiệu năng kinh hoàng do không toàn bộ nội dung được biên soạn và build từ trước trong quá trình deploy, loại bỏ hoàn toàn việc xử lý ở server.

\- Dễ Scaling vì nội dung code hay content không bị bó buộc có thể được lưu trữ ở bất kỳ đâu.

\- Tính bảo mật cao do server được abstract thông qua kiến trúc microservice ở API khiến khó khăn trong việc tấn công cũng như dễ dàng tích hợp các dịch vụ từ bên thứ 3.

\- Tối ưu hóa trải nghiệm trong quá trình phát triển, kiến trúc chia ra một mặt cho statics site generator phục vụ hiển thị content và marketing bằng những web tĩnh từ data động tối ưu hóa cho việc SEO, mặt còn lại sử dụng các dịch vụ CMS để biên soạn và xử lý nội dung.

# 2. Static site generator

![static site generator](/images/uploads/best-static-site-generator-2020.png "static site generator")

Static site generator là bộ công cụ tạo ra các trang web tĩnh hỗ trợ SEO (vì web tĩnh cực kỳ tối ưu cho bot crawl của google nhận diện và tìm ra địa chỉ).

## 2.1. Hugo - Is you? Flash?

Ứng cử viên số 1 cho phân khúc này là Hugo sử dụng ngôn ngữ lập trình Golang (một trong những ngôn ngữ hệ thống mạnh nhất hiện nay tối ưu hóa cho việc xử lý hiệu năng hay tính toán, được thiết kế bởi Google). Nói đây là ứng cử viên số một vì sức mạnh kinh hoàng của hugo vượt mặt các ssg được giới thiệu tới đây và vượt xa phần đa các trang web hiện nay trên thế giới với tốc độ build 5000 trang blog trong vòng 6 giây.

Điểm yếu của nó chính là hơi ít tiện ích (plugin), muốn ăn ngon thì phải tự lăn vào bếp ... nhầm mở lap lên code.

## 2.2. GatsbyJS - Ta đẹp ta có quyền

Dù không nhanh như Hugo, nhưng vẫn phải bắt Hugo ngước nhìn đó chính là Gatsby. Được phát triển trên nền React và là một thành viên trong hệ sinh thái công nghệ của Facebook. Được nhiều cái tên máu mặt như Facebook, AirBnb, Nike sử dụng (tham khảo thêm tại đây: <https://www.gatsbyjs.com/showcase/>) mặc dù tuổi đời còn rất trẻ (sinh năm 2017).

Sở hữu một bộ plugin khổng lồ bao gồm 1160 plugin mặc dù bộ theme chưa được phong phú lắm vì sinh sau đẻ muộn. Ưu điểm đó chính là dễ tìm bạn đời (CMS đi kèm cực kỳ nhiều và dễ tích hợp), thân thiện với công cụ tìm kiếm.

## 2.3. Hexo - Đơn giản, mạnh mẽ cho một Blogger

Vẻ đẹp của Hexo đến từ sự đơn giản. Nói đùa thế thôi chứ bản thân Hexo sử dụng NodeJS, một ngôn ngữ khá quen thuộc và phổ biến trong giới lập trình hiện nay, đồng thời rất dễ tìm cho mình một Hosting hay tận dụng được cả núi thư viện của cộng đồng npm nữa chứ. Một khía cạnh khác cần lưu ý là Hexo tập trung vào lĩnh vực Blog nên bạn muốn một web thương mại với Hexo, chúc bạn may mắn tìm được theme vừa ý. Ngoài ra hệ sinh thái của Hexo có rất nhiều theme đẹp và plugin mạnh.

Điểm yếu lớn nhất của Hexo đó là cộng đồng phát triển phần đa là người Trung Quốc, các tài liệu về theme hay plugin nhiều khi không tìm được tiếng Anh gây khó khăn trong quá trình phát triển.

Nhân tiện Blog này cũng đã được dựng bằng Hexo.

# 3. Content management system

![content management system](/images/uploads/headless-cms.png "content management system")

Nếu như coi SSG là một file pdf chứa nội dung cần truyền tải thì CMS chính là trình soạn thảo của file pdf đó. Ở thế giới này cũng đa dạng giống loài.

## 3.1. Netlify CMS

Netlify CMS sẽ là cái tên đầu tiên được nêu lên vì nó hỗ trợ đủ để cho những người không cần kiến thức về kỹ thuật cũng có thể sử dụng được. Bản thân netlify cũng cung cấp sẵn hosting và domain cho người đùng, tất của những gì cần thực hiện là đẩy code SSG lên github, setting bố cục bài viết rồi đẩy lên netlify là có thể sử dụng được không cần thêm dịch vụ hosting nào.

## 3.2. Strapi (researching)

## 3.3. TinaCMS (researching)