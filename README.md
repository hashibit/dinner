# Dinner - 午餐订购系统

基于 Ruby on Rails 的内部午餐订购系统。

## 系统功能

- 菜品管理：添加、编辑、删除菜品信息
- 订单管理：创建和管理个人午餐订单
- 用户管理：用户注册、登录和部门管理
- 权限控制：基于角色的访问控制

## 技术栈

- Ruby 3.1.2
- Rails 7.0.4
- 数据库：SQLite 3
- 认证：Devise
- 授权：CanCan
- 后台管理：RailsAdmin
- 前端：jQuery + Bootstrap + HAML

## 快速开始

### 安装依赖

```bash
bundle install
```

### 数据库初始化

```bash
rails db:create
rails db:migrate
rails db:seed
```

### 启动服务器

```bash
rails server
```

访问 http://localhost:3000

## 目录结构

```
app/
  controllers/    # 控制器
  models/         # 数据模型
  views/          # 视图模板
db/               # 数据库文件和迁移
config/           # 配置文件
```

## 主要模型

- User：用户，关联到部门
- Department：部门
- Dish：菜品
- Order：订单
- OrderDish：订单菜品关联

## 权限说明

管理员用户可以管理菜品，普通用户只能创建和管理自己的订单。
