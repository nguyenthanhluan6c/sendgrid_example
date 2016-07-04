# Sendgrid email
## SendGrid là gì

SendGrid là 1 trong những dịch vụ nổi tiếng trong việc cung cấp email giao dịch (transaction email). Sendgrid cung cấp giải pháp email dựa trên nền tảng đám mây thay thế cho hệ thống email truyền thống của bạn, do đó bạn không cần phải xây dựng, quy mô và duy trì các hệ thống mail server.

Sử dụng SendGrid giúp giảm bớt lượng mail gửi đến thư mục rác (junk folder), dễ dàng mở rộng nâng cấp qui mô hệ thống, cung cấp khả năng đánh giá tính hiệu quả của các chiến dịch mail marketing cũng như 1 kho API với các tính năng hữu ích cần thiết.

Mức giá mà SendGrid đưa ra không quá cao và cũng không quá thấp: 9.95$ / tháng/ 40,000 emails.

## Cài đặt trong rails
1. Đăng ký tài khoản 
  [https://app.sendgrid.com](https://app.sendgrid.com)
2. Cài đặt trong Rails
  * tạo action mailer

>       rails generate mailer UserNotifier

  * config trong file config/environment.rb

>     ActionMailer::Base.smtp_settings = {
>       :user_name => 'your_sendgrid_username',
>       :password => 'your_sendgrid_password',
>       :domain => 'yourdomain.com',
>       :address => 'smtp.sendgrid.net',
>       :port => 587,
>       :authentication => :plain,
>       :enable_starttls_auto => true
>     }


