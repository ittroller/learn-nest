<h1> Read me Learn NEST.JS </h1>

## **Install:**

Check Nodejs version trước

Có thể chọn platform build source:

- platform-express (mặc định)

- platform-fastify

`npm i -g @nestjs/cli`

Cú pháp tạo dự án:

`nest new <project-name> --package-manager npm --language ts --template graphql`

Ví dụ: `nest new my-graphql-app --template graphql`

Ngắn gọn hơn: `nest new project-name`

## **Learn:**

### 1. NestJS CLI command:

- Tạo resource: `nest generate resource <module-name>`

  _Sẽ xuất hiện các tùy chọn để tạo ra 1 cụm file router/controller/module/service, folder entities/dto (có thể dùng từ viết tắt để lượt bỏ quá trình chọn)_

- Tạo module (1 file .module.ts - quản lý cấu hình module): `nest generate module <module-name>` === `nest g mo <module-name>`

- Tạo controller (1 file .controller.ts - đăng ký các controller trong module): `nest generate controller <module-name>` === `nest g co <module-name>`

- Tạo service (1 file .service.ts - tạo các service theo các hàm trong controller): `nest generate service <module-name>` === `nest g s <module-name>`

- Tạo provider (1 file .ts - có thể là service, repository hoặc một helper function): `nest generate provider <module-name>` === `nest g pr <module-name>`

- Tạo middleware (1 file .middleware.ts): `nest generate middleware <module-name>` === `nest g mi <module-name>`

- Tạo interceptor (1 file .interceptor.ts - để can thiệp vào request hoặc response): `nest generate interceptor <module-name>`

- Tạo guard (1 file .guard.ts - để kiểm soát quyền truy cập): `nest generate guard <module-name>` === `nest g gu <module-name>`

- Tạo pipe (1 file .pipe.ts - để xử lý dữ liệu đầu vào): `nest generate pipe <module-name>` === `nest g pi <module-name>`

### 2. Controller:

| Nest                        | ExporessJS                      |
| :-------------------------- | :------------------------------ |
| @Request(), @Req()          | req                             |
| @Response(), @Res()\*       | res                             |
| @Next()                     | next                            |
| @Session()                  | req.session                     |
| @Param(key?: string)        | req.params / req.params[key]    |
| @Body(key?: string)         | req.body / req.body[key]        |
| @Query(key?: string)        | req.query / req.query[key]      |
| @Headers(name?: string)     | req.headers / req.headers[name] |
| @Ip()                       | req.ip                          |
| @HostParam()                | req.hosts                       |
| @HttpCode(<number>)         | res.status(<number>)            |
| @Header('<key>', '<value>') | Header.<key> = <value>          |
