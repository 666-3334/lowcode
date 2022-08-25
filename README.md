/components/getAllComps.js          中定义我们页面中左侧有的组件

/components/defaultcomp.vue         是左侧的每一个组件

/components/actualcomp.vue          是中间部分的每一个组件

/views

      /centerview                   中间页面效果部分

      /leftview                     左侧组件选择部分

      /rightview                    右侧组件属性部分

      /topview                      顶部标题部分

      /homeview                     整个页面


全局数据传递关键：compindex 即 所选在getAllComps.js中的index

文本组件

    目前实现：左侧组件展示（可优化部分：组件预览），拖动到中间区域添加组件（在中间部分的拖拽效果未实现）

    目前未实现：右侧编辑组件功能

    理想效果：双击组件触发编辑