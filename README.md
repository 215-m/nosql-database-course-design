# 校园快递驿站管理系统

## 技术栈
Python / FastAPI / Redis-Py / Vue 3 / TypeScript / Element Plus

## 功能
- 管理员端：快递入库、包裹管理、取件核验、寄件核验、异常件处理、用户管理、黑名单、滞留包裹统计、用户包裹数量排行
- 用户端：注册登录、我的快递、取件码查询、自主取件、寄件申请、历史取件记录、个人信息管理

## 我负责的部分
后端全部 API 设计与 Redis 数据建模。使用 Hash 存包裹状态、Set 维护取件码集合、Sorted Set 实现滞留排行；用 Lua 脚本保证取件核验原子性，Pipeline 批量写入提升性能。

## 运行方式
1. 启动 Redis
2. 安装后端依赖：`pip install -r requirements.txt`
3. 启动 FastAPI：`uvicorn main:app --reload`
4. 前端：`npm install && npm run dev`
