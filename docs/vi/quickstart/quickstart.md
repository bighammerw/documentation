# Hướng dẫn bắt đầu nhanh

Trong hướng dẫn Bắt đầu Nhanh này, chúng ta sẽ tạo một dự án khởi động đơn giản mà bạn có thể sử dụng làm khuôn mẫu để phát triển Dự án SubQuery cho chính mình.

Ở cuối hướng dẫn này, bạn sẽ có một dự án SubQuery đang hoạt động chạy trên nút SubQuery với điểm cuối GraphQL mà có thể truy vấn dữ liệu từ đó.

Nếu chưa có, chúng tôi khuyên bạn nên tự làm quen với [thuật ngữ](../#terminology) được sử dụng trong SubQuery.

## Chuẩn bị

### Môi trường phát triển địa phương

- [Chỉ định loại](https://www.typescriptlang.org/) được yêu cầu để biên dịch dự án và xác định thể loại.
- Cả SubQuery CLI và Dự án đã tạo đều có phụ thuộc và yêu cầu phiên bản hiện đại [Node](https://nodejs.org/en/).
- SubQuery Nodes yêu cầu Docker

### Cài đặt CLI SubQuery

Cài đặt SubQuery CLI tổng thể trên terminal của bạn bằng cách sử dụng NPM:

```shell
# NPM
npm install -g @subql/cli
```

Xin lưu ý rằng chúng tôi **KHÔNG** khuyến khích sử dụng `yarn global` do việc quản lý phụ thuộc kém có thể dẫn đến lỗi xuống dòng.

Sau đó, bạn có thể chạy trợ giúp để xem các lệnh có sẵn và cách sử dụng do CLI cung cấp

```shell
subql help
```

## Khởi tạo Dự án SubQuery Starter

Bên trong thư mục mà bạn muốn tạo một dự án SubQuery, chỉ cần thay thế `PROJECT_NAME` bằng tên của riêng bạn và chạy lệnh:

```shell
subql init PROJECT_NAME
```

Bạn sẽ được hỏi một số câu hỏi nhất định khi dự án SubQuery được khởi động:

- Network: Một mạng blockchain mà dự án SubQuery này sẽ được phát triển để lập chỉ mục
- Template: Chọn một mẫu dự án SubQuery sẽ cung cấp một điểm khởi đầu để bắt đầu phát triển
- Git repository (Tùy chọn): Cung cấp URL Git cho kho lưu trữ dự án SubQuery này (khi được lưu trữ trong SubQuery Explorer)
- RPC endpoint (Bắt buộc): Cung cấp URL websocket (wss) tới điểm cuối RPC đang chạy sẽ được sử dụng theo mặc định cho dự án này. Bạn có thể nhanh chóng truy cập các điểm cuối công khai cho các mạng Polkadot khác nhau hoặc thậm chí tạo nút chuyên dụng riêng của mình bằng cách sử dụng [OnFinality](https://app.onfinality.io) hoặc chỉ sử dụng điểm cuối Polkadot mặc định. Nút RPC này phải là một nút lưu trữ (có trạng thái chuỗi đầy đủ).
- Authors (Bắt buộc): Nhập chủ sở hữu của dự án SubQuery này tại đây
- Description (Tùy chọn): Bạn có thể cung cấp một đoạn giới thiệu ngắn về dự án của mình, mô tả dự án chứa dữ liệu gì và người dùng có thể làm gì với dự án
- Version (Bắt buộc): Nhập số phiên bản tùy chỉnh hoặc sử dụng giá trị mặc định (`1.0.0`)
- License (Bắt buộc): Cung cấp giấy phép phần mềm cho dự án này hoặc chấp nhận mặc định (`Apache-2.0`)

Sau khi quá trình khởi tạo hoàn tất, bạn sẽ thấy một thư mục có tên dự án của bạn đã được tạo bên trong thư mục. Nội dung của thư mục này phải giống với nội dung được liệt kê trong [Cấu trúc thư mục](../create/introduction.md#directory-structure).

Cuối cùng, trong thư mục dự án, chạy lệnh sau để cài đặt các phụ thuộc của dự án mới.

<CodeGroup> <CodeGroupItem title="YARN" active> ```shell cd PROJECT_NAME yarn install ``` </CodeGroupItem>
<CodeGroupItem title="NPM"> ```bash cd PROJECT_NAME npm install ``` </CodeGroupItem> </CodeGroup>

## Định cấu hình và xây dựng dự án dành cho người mới bắt đầu

Trong gói khởi động mà bạn vừa khởi tạo, chúng tôi đã cung cấp cấu hình tiêu chuẩn cho dự án mới của bạn. Bạn sẽ chủ yếu làm việc trên các tệp sau:

- The Manifest in `project.yaml`
- Sơ đồ GraphQL trong `schema.graphql`
- Các chức năng ánh xạ trong thư mục `src/mappings/`

Để biết thêm thông tin về cách viết SubQuery của riêng bạn, hãy xem tài liệu của chúng tôi trong [Tạo dự án](../create/introduction.md)

### Tạo mô hình GraphQL

Để [lập chỉ mục](../run/run.md) dự án SubQuery của bạn, trước tiên bạn phải tạo các mô hình GraphQL bắt buộc mà bạn đã xác định trong tệp Sơ đồ GraphQL (`schema.graphql`). Chạy lệnh này trong thư mục gốc của thư mục dự án.

<CodeGroup> <CodeGroupItem title="YARN" active> ```shell yarn codegen ``` </CodeGroupItem>
<CodeGroupItem title="NPM"> ```bash npm run-script codegen ``` </CodeGroupItem> </CodeGroup>

Bạn sẽ tìm thấy các mô hình đã tạo trong thư mục `/src/types/models`

## Xây dựng dự án

Để chạy Dự án SubQuery của bạn trên một Nút SubQuery được lưu trữ cục bộ, bạn cần phải xây dựng công việc của mình.

Chạy lệnh xây dựng từ thư mục gốc của dự án.

<CodeGroup> <CodeGroupItem title="YARN" active> ```shell yarn build ``` </CodeGroupItem>
<CodeGroupItem title="NPM"> ```bash npm run-script build ``` </CodeGroupItem> </CodeGroup>

## Chạy và truy vấn dự án khởi đầu của bạn

Mặc dù bạn có thể nhanh chóng xuất bản dự án mới của mình lên[Dự án SubQuery](https://project.subquery.network) và truy vấn bằng cách sử dụng [Explorer](https://explorer.subquery.network) của chúng tôi, cách dễ nhất để chạy các nút SubQuery cục bộ là trong vùng chứa Docker, nếu không  có Docker, bạn có thể cài đặt nó từ [docker.com](https://docs.docker.com/get-docker/).

[_Bỏ qua điều này và xuất bản dự án mới của bạn lên SubQuery Projects_](../publish/publish.md)

### Chạy Dự án SubQuery của bạn

Tất cả cấu hình kiểm soát cách chạy nút SubQuery được xác định trong tệp `docker-compose.yml` file. Đối với một dự án mới vừa được khởi tạo, bạn sẽ không cần phải thay đổi bất kỳ điều gì nhưng có thể đọc thêm về tệp và cài đặt trong [phần Chạy dự án](../run/run.md) của chúng tôi

Trong thư mục dự án chạy lệnh sau:

```shell
docker-compose pull && docker-compose up
```

Có thể mất một chút thời gian để tải xuống các gói bắt buộc ([`@subql/node`](https://www.npmjs.com/package/@subql/node), [`@subql/query`](https://www.npmjs.com/package/@subql/query) và Postgres) lần đầu tiên nhưng bạn sẽ sớm thấy Nút SubQuery đang chạy.

### Truy vấn dự án của bạn

Mở trình duyệt của bạn và truy cập [ http://localhost:3000](http://localhost:3000).

Bạn sẽ thấy một sân chơi GraphQL đang hiển thị trong explorer và các lược đồ đã sẵn sàng để truy vấn. Ở trên cùng bên phải của sân chơi, bạn sẽ tìm thấy nút _Tài liệu_ sẽ mở bản vẽ tài liệu. Tài liệu này được tạo tự động và giúp bạn tìm thấy những thực thể và phương pháp nào bạn có thể truy vấn.

Đối với dự án khởi động SubQuery mới, bạn có thể thử truy vấn như sau để biết cách hoạt động của nó hoặc [tìm hiểu thêm về ngôn ngữ Truy vấn GraphQL](../query/graphql.md).

```graphql
{
  query {
    starterEntities(first: 10) {
      nodes {
        field1
        field2
        field3
      }
    }
  }
}
```

## Bước tiếp theo

Xin chúc mừng, bạn hiện có một dự án SubQuery đang chạy cục bộ chấp nhận các yêu cầu API GraphQL cho dữ liệu mẫu. Trong hướng dẫn tiếp theo, chúng tôi sẽ chỉ cho bạn cách xuất bản dự án mới lên [Dự án SubQuery](https://project.subquery.network) và truy vấn nó bằng cách sử dụng [Explorer](https://explorer.subquery.network) của chúng tôi

[Xuất bản dự án mới của bạn lên SubQuery Projects](../publish/publish.md)
