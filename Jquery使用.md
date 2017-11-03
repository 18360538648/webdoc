# Jquery使用

## 1. 常见语法

### 1.1 $(event.target)指触发事件dom对象

### 1.2 $.inArray(obj, arr) 检测obj是否在arr中，如果不在返回-1

### 事件绑定监听

```
// 监听输入框内容改变
$('#username').off('input porpertychange').on('input porpertychange', function () {
    console.log('onchange');
    const input = $(this).val();
    console.log('input', input);
    if (isNaN(input)) {
      swal({
        title: '手机号码格式有误',
        confirmButtonColor: '#1caac4',
        confirmButtonText: '确定',
        type: 'warning'
      });
      return false;
    }
  });
```