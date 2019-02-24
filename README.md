
# SmartShow
仿iOS弹窗

### config in java code
```java
new AlertView("上传头像", null, "取消", null,
                new String[]{"拍照", "从相册中选择"},
                this, AlertView.Style.ActionSheet, new OnItemClickListener(){
                    public void onItemClick(Object o,int position){
                        Toast.makeText(this, "点击了第" + position + "个",
                        Toast.LENGTH_SHORT).show();
                    }
                }).show();

//或者builder模式创建
new AlertView.Builder().setContext(context)
                .setStyle(AlertView.Style.ActionSheet)
                .setTitle("选择操作")
                .setMessage(null)
                .setCancelText("取消")
                .setDestructive("拍照", "从相册中选择")
                .setOthers(null)
                .setOnItemClickListener(listener)
                .build()
                .show();
```
```java
new AlertView("标题", "内容", null, new String[]{"确定"}, null, this,
                AlertView.Style.Alert, null).show();
```



MIT License

Copyright (c) 2019 刘鹏

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
