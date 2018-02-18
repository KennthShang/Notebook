## Magic 关键字

Magic 关键字是可以在单元格中运行的特殊命令，能让你控制 notebook 本身或执行系统调用（例如更改目录）。例如，在 notebook 中可以使用 `%matplotlib` 将 matplotlib 设置为以交互方式工作。

Magic 命令的前面带有一个或两个百分号（`%` 或 `%%`），分别对应行 Magic 命令和单元格 Magic 命令。行 Magic 命令仅应用于编写 Magic 命令时所在的行，而单元格 Magic 命令应用于整个单元格。

**注意**：这些 Magic 关键字是特定于普通 Python 内核的关键字。如果使用其他内核，这些关键字很有可能无效。

### 代码计时

有时候，你可能要花些精力优化代码，让代码运行得更快。在此优化过程中，必须对代码的运行速度进行计时。可以使用 Magic 命令 `timeit` 测算函数的运行时间，如下所示：

<img src="https://s3.cn-north-1.amazonaws.com.cn/u-img/5107d13d-ebbb-4cce-bdbf-cc4dae39e210">

如果要测算整个单元格的运行时间，请使用 `%%timeit`，如下所示：

<img src="https://s3.cn-north-1.amazonaws.com.cn/u-img/4935f7ac-3024-40c3-87f2-406dc9d73400">

### 在代码中嵌入可视化内容

如前所述，notebook 允许你将图像与文本和代码一起嵌入。这在你使用 matplotlib 或其他绘图包创建可视化内容时最为有用。在 notebook 中可以使用 `%matplotlib` 将 matplotlib 设置为以交互方式工作。默认情况下，图形呈现在各自的窗口中。但是，你可以通过命令传递参数，以选择特定的“[后端](http://matplotlib.org/faq/usage_faq.html#what-is-a-backend)”（呈现图像的软件）。要直接在 notebook 中呈现图形，应将通过命令 `%matplotlib inline` 内联后端一起使用。


> 提示：在分辨率较高的屏幕（例如 Retina 显示屏）上，notebook 中的默认图像可能会显得模糊。可以在 `%matplotlib inline` 之后使用 `%config InlineBackend.figure_format = 'retina'` 来呈现分辨率较高的图像。

<img src="https://s3.cn-north-1.amazonaws.com.cn/u-img/5e263ad0-6e13-4ade-a766-5da705ce1e8e">

### 在notebook中进行调试

对于 Python 内核，可以使用 Magic 命令 `%pdb` 开启交互式调试器。出错时，你能检查当前命名空间中的变量。

<img src="https://s3.cn-north-1.amazonaws.com.cn/u-img/bf742711-6127-4af8-8111-ea370ef8f2da">

在上图中，可以看到我尝试对字符串求和，这造成了错误。调试器指出了该错误，并提示你检查代码。要详细了解 pdb，请阅读此[文档](https://docs.python.org/3/library/pdb.html)。要退出调试器，在提示符中输入 q 即可。

### 补充读物
Magic 命令还有很多，我只是介绍了你将会用得最多的一些命令。要了解更多信息，请查看此[列表](http://ipython.readthedocs.io/en/stable/interactive/magics.html)，它列出了所有可用的 Magic 命令。