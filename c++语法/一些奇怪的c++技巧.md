# 一些奇怪的c++技巧

- 使用逗号表达式和变参模板展开实现一些技巧

  ```c++
  // 这个函数实现了把任意多元素放入vector中
  template <typename... Args>
  void Push(vector<int> vec, Args... args)
  {
          std::initializer_list<int>{(vec.push_back(static_cast<int>(args)),0)...};
  
  }
  ```

  