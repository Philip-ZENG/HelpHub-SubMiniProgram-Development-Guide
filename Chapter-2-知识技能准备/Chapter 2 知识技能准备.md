# Chapter 2 知识技能准备

最后更新日期：2021年10月2日

作者：曾焯儒



在开始接触代码之前，我们建议你先完成相关的前期准备工作以及知识技能的储备。

- 请下载和熟悉微信小程序的开发辅助工具: "微信开发者工具"
  - 参考文档：微信小程序开发文档： https://developers.weixin.qq.com/miniprogram/dev/framework/quickstart/
  
- 请学习软件开发文档的书写原则和规范
  - 参考资料：
  
    - 书写原则：Software Engineering at Google， Chapter 10 - Documentation （你可以在本文件夹里找到这本书的电子版）
    - 格式规范：https://guides.lib.berkeley.edu/how-to-write-good-documentation
  
  - 我们的代码注释规范
  
    ```c++
    // Template
    /*
     * Description:
     * Describe the purpose and functionality of this function
     * 
     * Parameters:
     * @para: Explain what is each parameter the function take in
     * 
     * Return: 
     * Explain what is the return value
     */
    
    // Example
    /*
     * Description:
     * This function adds up two numbers
     * 
     * Parameters:
     * @x : the first integer
     * @y : the second integer
     * 
     * Return: 
     * The sum of two intergers
     */
    
    int add(int x, int y)
    {
        return x+y;
    }
    ```
  
- 请安装开发文档的写作工具
  - 我们将使用Mark Down作为开发文档的写作语言，我们推荐的Mark Down编辑器是Typora
  - 你可以前往官网下载该程序： https://typora.io/
  
- 请学习GitHub的使用
  - 请熟悉GitHub的使用，在后续的开发过程中，我们将频繁使用到GitHub
  - 对于从来没有接触过GitHub的开发者，可以参考本文件夹下的文档Appendix-A中的GitHub入门指引进行学习
  
- 请联系HelpHub的GitHub组织管理员获取HelpHub+小程序的源码

- Taro框架学习

  - 参考官方文档：https://taro-docs.jd.com/taro/docs/GETTING-STARTED#cli-%E5%B7%A5%E5%85%B7%E5%AE%89%E8%A3%85
  - 入门学习参考Blog: https://www.cnblogs.com/cczlovexw/p/13808842.html

