---
title: "F# Interactive 选项"
description: "了解有关 F # Interactive，支持的命令行选项 fsi.exe。"
keywords: "visual f#, f#, 函数编程"
author: cartermp
ms.author: phcart
ms.date: 05/16/2016
ms.topic: language-reference
ms.prod: .net
ms.technology: devlang-fsharp
ms.devlang: fsharp
ms.assetid: f9f3e39b-ce6c-41ff-991f-0625f46441ae
ms.openlocfilehash: 0fc369993b3ee4c8a9139e4a365330197fe66946
ms.sourcegitcommit: cf22b29db780e532e1090c6e755aa52d28273fa6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2018
---
# <a name="f-interactive-options"></a><span data-ttu-id="c7468-104">F# Interactive 选项</span><span class="sxs-lookup"><span data-stu-id="c7468-104">F# Interactive Options</span></span>

> [!NOTE]
<span data-ttu-id="c7468-105">本文目前仅介绍适用于 Windows 的体验。</span><span class="sxs-lookup"><span data-stu-id="c7468-105">This article currently describes the experience for Windows only.</span></span>  <span data-ttu-id="c7468-106">它将被重写。</span><span class="sxs-lookup"><span data-stu-id="c7468-106">It will be rewritten.</span></span>

<span data-ttu-id="c7468-107">本主题介绍 F # Interactive，支持的命令行选项`fsi.exe`。</span><span class="sxs-lookup"><span data-stu-id="c7468-107">This topic describes the command-line options supported by F# Interactive, `fsi.exe`.</span></span> <span data-ttu-id="c7468-108">F # Interactive 接受许多 F # 编译器，与相同的命令行选项，但还接受一些附加选项。</span><span class="sxs-lookup"><span data-stu-id="c7468-108">F# Interactive accepts many of the same command line options as the F# compiler, but also accepts some additional options.</span></span>

## <a name="using-f-interactive-for-scripting"></a><span data-ttu-id="c7468-109">使用 F # Interactive 用于脚本编写</span><span class="sxs-lookup"><span data-stu-id="c7468-109">Using F# Interactive for Scripting</span></span>
<span data-ttu-id="c7468-110">F # Interactive， `fsi.exe`、 以交互方式，可启动或从命令行运行脚本可启动它。</span><span class="sxs-lookup"><span data-stu-id="c7468-110">F# Interactive, `fsi.exe`, can be launched interactively, or it can be launched from the command line to run a script.</span></span> <span data-ttu-id="c7468-111">命令行语法</span><span class="sxs-lookup"><span data-stu-id="c7468-111">The command line syntax is</span></span>

```
> fsi.exe [options] [ script-file [arguments] ]
```

<span data-ttu-id="c7468-112">F # 脚本文件的文件扩展名是`.fsx`。</span><span class="sxs-lookup"><span data-stu-id="c7468-112">The file extension for F# script files is `.fsx`.</span></span>

## <a name="table-of-f-interactive-options"></a><span data-ttu-id="c7468-113">F # Interactive 选项的表</span><span class="sxs-lookup"><span data-stu-id="c7468-113">Table of F# Interactive Options</span></span>
<span data-ttu-id="c7468-114">下表总结了所支持的 F # Interactive 选项。</span><span class="sxs-lookup"><span data-stu-id="c7468-114">The following table summarizes the options supported by F# Interactive.</span></span> <span data-ttu-id="c7468-115">在命令行上或通过 Visual Studio IDE，你可以设置这些选项。</span><span class="sxs-lookup"><span data-stu-id="c7468-115">You can set these options on the command-line or through the Visual Studio IDE.</span></span> <span data-ttu-id="c7468-116">若要在 Visual Studio IDE 中设置这些选项，打开**工具**菜单上，选择**选项...**，然后展开**F # 工具**节点，然后选择**F # Interactive**。</span><span class="sxs-lookup"><span data-stu-id="c7468-116">To set these options in the Visual Studio IDE, open the **Tools** menu, select **Options...**, then expand the **F# Tools** node and select **F# Interactive**.</span></span>

<span data-ttu-id="c7468-117">其中列表出现在 F # Interactive 选项自变量，用分号分隔列表元素 (`;`)。</span><span class="sxs-lookup"><span data-stu-id="c7468-117">Where lists appear in F# Interactive option arguments, list elements are separated by semicolons (`;`).</span></span>

|<span data-ttu-id="c7468-118">选项</span><span class="sxs-lookup"><span data-stu-id="c7468-118">Option</span></span>|<span data-ttu-id="c7468-119">描述</span><span class="sxs-lookup"><span data-stu-id="c7468-119">Description</span></span>|
|------|-----------|
|**--**|<span data-ttu-id="c7468-120">用于指示 F # Interactive 对 F # 程序或脚本，你可以在代码中使用访问列表作为命令行自变量视为其余的自变量**fsi.CommandLineArgs**。</span><span class="sxs-lookup"><span data-stu-id="c7468-120">Used to instruct F# Interactive to treat remaining arguments as command line arguments to the F# program or script, which you can access in code by using the list **fsi.CommandLineArgs**.</span></span>|
|<span data-ttu-id="c7468-121">**--checked**[**+**&#124;**-**]</span><span class="sxs-lookup"><span data-stu-id="c7468-121">**--checked**[**+**&#124;**-**]</span></span>|<span data-ttu-id="c7468-122">与相同**fsc.exe**编译器选项。</span><span class="sxs-lookup"><span data-stu-id="c7468-122">Same as the **fsc.exe** compiler option.</span></span> <span data-ttu-id="c7468-123">有关详细信息，请参阅[编译器选项](compiler-options.md)。</span><span class="sxs-lookup"><span data-stu-id="c7468-123">For more information, see [Compiler Options](compiler-options.md).</span></span>|
|<span data-ttu-id="c7468-124">**--codepage:&lt;int&gt;**</span><span class="sxs-lookup"><span data-stu-id="c7468-124">**--codepage:&lt;int&gt;**</span></span>|<span data-ttu-id="c7468-125">与相同**fsc.exe**编译器选项。</span><span class="sxs-lookup"><span data-stu-id="c7468-125">Same as the **fsc.exe** compiler option.</span></span> <span data-ttu-id="c7468-126">有关详细信息，请参阅[编译器选项](compiler-options.md)。</span><span class="sxs-lookup"><span data-stu-id="c7468-126">For more information, see [Compiler Options](compiler-options.md).</span></span>|
|<span data-ttu-id="c7468-127">**--crossoptimize**[**+**&#124;**-**]</span><span class="sxs-lookup"><span data-stu-id="c7468-127">**--crossoptimize**[**+**&#124;**-**]</span></span>|<span data-ttu-id="c7468-128">启用或禁用跨模块优化。</span><span class="sxs-lookup"><span data-stu-id="c7468-128">Enable or disable cross-module optimizations.</span></span>|
|<span data-ttu-id="c7468-129">**--debug**[**+**&#124;**-**]</span><span class="sxs-lookup"><span data-stu-id="c7468-129">**--debug**[**+**&#124;**-**]</span></span><br /><br /><span data-ttu-id="c7468-130">**--debug:**[**full**&#124;**pdbonly**]</span><span class="sxs-lookup"><span data-stu-id="c7468-130">**--debug:**[**full**&#124;**pdbonly**]</span></span><br /><br /><span data-ttu-id="c7468-131">**-g**[**+**&#124;**-**]</span><span class="sxs-lookup"><span data-stu-id="c7468-131">**-g**[**+**&#124;**-**]</span></span><br /><br /><span data-ttu-id="c7468-132">**-g:**[**full**&#124;**pdbonly**]</span><span class="sxs-lookup"><span data-stu-id="c7468-132">**-g:**[**full**&#124;**pdbonly**]</span></span>|<span data-ttu-id="c7468-133">与相同**fsc.exe**编译器选项。</span><span class="sxs-lookup"><span data-stu-id="c7468-133">Same as the **fsc.exe** compiler option.</span></span> <span data-ttu-id="c7468-134">有关详细信息，请参阅[编译器选项](compiler-options.md)。</span><span class="sxs-lookup"><span data-stu-id="c7468-134">For more information, see [Compiler Options](compiler-options.md).</span></span>|
|<span data-ttu-id="c7468-135">**--define:&lt;string&gt;**</span><span class="sxs-lookup"><span data-stu-id="c7468-135">**--define:&lt;string&gt;**</span></span>|<span data-ttu-id="c7468-136">与相同**fsc.exe**编译器选项。</span><span class="sxs-lookup"><span data-stu-id="c7468-136">Same as the **fsc.exe** compiler option.</span></span> <span data-ttu-id="c7468-137">有关详细信息，请参阅[编译器选项](compiler-options.md)。</span><span class="sxs-lookup"><span data-stu-id="c7468-137">For more information, see [Compiler Options](compiler-options.md).</span></span>|
|<span data-ttu-id="c7468-138">**--exec**</span><span class="sxs-lookup"><span data-stu-id="c7468-138">**--exec**</span></span>|<span data-ttu-id="c7468-139">指示 F # interactive 加载文件或运行命令行上给出的脚本文件后退出。</span><span class="sxs-lookup"><span data-stu-id="c7468-139">Instructs F# interactive to exit after loading the files or running the script file given on the command line.</span></span>|
|<span data-ttu-id="c7468-140">**--fullpaths**</span><span class="sxs-lookup"><span data-stu-id="c7468-140">**--fullpaths**</span></span>|<span data-ttu-id="c7468-141">与相同**fsc.exe**编译器选项。</span><span class="sxs-lookup"><span data-stu-id="c7468-141">Same as the **fsc.exe** compiler option.</span></span> <span data-ttu-id="c7468-142">有关详细信息，请参阅[编译器选项](compiler-options.md)。</span><span class="sxs-lookup"><span data-stu-id="c7468-142">For more information, see [Compiler Options](compiler-options.md).</span></span>|
|<span data-ttu-id="c7468-143">**--gui**[**+**&#124;**-**]</span><span class="sxs-lookup"><span data-stu-id="c7468-143">**--gui**[**+**&#124;**-**]</span></span>|<span data-ttu-id="c7468-144">启用或禁用 Windows 窗体事件循环。</span><span class="sxs-lookup"><span data-stu-id="c7468-144">Enables or disables the Windows Forms event loop.</span></span> <span data-ttu-id="c7468-145">默认为已启用。</span><span class="sxs-lookup"><span data-stu-id="c7468-145">The default is enabled.</span></span>|
|<span data-ttu-id="c7468-146">**--help**</span><span class="sxs-lookup"><span data-stu-id="c7468-146">**--help**</span></span><br /><br /><span data-ttu-id="c7468-147">**-?**</span><span class="sxs-lookup"><span data-stu-id="c7468-147">**-?**</span></span>|<span data-ttu-id="c7468-148">用于显示的命令行语法和每个选项的简短说明。</span><span class="sxs-lookup"><span data-stu-id="c7468-148">Used to display the command line syntax and a brief description of each option.</span></span>|
|<span data-ttu-id="c7468-149">**--lib:&lt;folder-list&gt;**</span><span class="sxs-lookup"><span data-stu-id="c7468-149">**--lib:&lt;folder-list&gt;**</span></span><br /><br /><span data-ttu-id="c7468-150">**-I:&lt;folder-list&gt;**</span><span class="sxs-lookup"><span data-stu-id="c7468-150">**-I:&lt;folder-list&gt;**</span></span>|<span data-ttu-id="c7468-151">与相同**fsc.exe**编译器选项。</span><span class="sxs-lookup"><span data-stu-id="c7468-151">Same as the **fsc.exe** compiler option.</span></span> <span data-ttu-id="c7468-152">有关详细信息，请参阅[编译器选项](compiler-options.md)。</span><span class="sxs-lookup"><span data-stu-id="c7468-152">For more information, see [Compiler Options](compiler-options.md).</span></span>|
|<span data-ttu-id="c7468-153">**--load:&lt;filename&gt;**</span><span class="sxs-lookup"><span data-stu-id="c7468-153">**--load:&lt;filename&gt;**</span></span>|<span data-ttu-id="c7468-154">将在启动时给定的源代码编译并将已编译的 F # 构造加载到会话。</span><span class="sxs-lookup"><span data-stu-id="c7468-154">Compiles the given source code at startup and loads the compiled F# constructs into the session.</span></span> <span data-ttu-id="c7468-155">如果目标源包含脚本的指令，例如**#use**或**#load**，则必须使用**-使用**或**#use**而不是**-加载**或**#load**。</span><span class="sxs-lookup"><span data-stu-id="c7468-155">If the target source contains scripting directives such as **#use** or **#load**, then you must use **--use** or **#use** instead of **--load** or **#load**.</span></span>|
|<span data-ttu-id="c7468-156">**--mlcompatibility**</span><span class="sxs-lookup"><span data-stu-id="c7468-156">**--mlcompatibility**</span></span>|<span data-ttu-id="c7468-157">与相同**fsc.exe**编译器选项。</span><span class="sxs-lookup"><span data-stu-id="c7468-157">Same as the **fsc.exe** compiler option.</span></span> <span data-ttu-id="c7468-158">有关详细信息，请参阅[编译器选项](compiler-options.md)。</span><span class="sxs-lookup"><span data-stu-id="c7468-158">For more information, see [Compiler Options](compiler-options.md).</span></span>|
|<span data-ttu-id="c7468-159">**--noframework**</span><span class="sxs-lookup"><span data-stu-id="c7468-159">**--noframework**</span></span>|<span data-ttu-id="c7468-160">与相同**fsc.exe**编译器选项。</span><span class="sxs-lookup"><span data-stu-id="c7468-160">Same as the **fsc.exe** compiler option.</span></span> <span data-ttu-id="c7468-161">有关详细信息，请参阅[编译器选项](compiler-options.md)</span><span class="sxs-lookup"><span data-stu-id="c7468-161">For more information, see [Compiler Options](compiler-options.md)</span></span>|
|<span data-ttu-id="c7468-162">**--nologo**</span><span class="sxs-lookup"><span data-stu-id="c7468-162">**--nologo**</span></span>|<span data-ttu-id="c7468-163">与相同**fsc.exe**编译器选项。</span><span class="sxs-lookup"><span data-stu-id="c7468-163">Same as the **fsc.exe** compiler option.</span></span> <span data-ttu-id="c7468-164">有关详细信息，请参阅[编译器选项](compiler-options.md)。</span><span class="sxs-lookup"><span data-stu-id="c7468-164">For more information, see [Compiler Options](compiler-options.md).</span></span>|
|<span data-ttu-id="c7468-165">**--nowarn:&lt;warning-list&gt;**</span><span class="sxs-lookup"><span data-stu-id="c7468-165">**--nowarn:&lt;warning-list&gt;**</span></span>|<span data-ttu-id="c7468-166">与相同**fsc.exe**编译器选项。</span><span class="sxs-lookup"><span data-stu-id="c7468-166">Same as the **fsc.exe** compiler option.</span></span> <span data-ttu-id="c7468-167">有关详细信息，请参阅[编译器选项](compiler-options.md)。</span><span class="sxs-lookup"><span data-stu-id="c7468-167">For more information, see [Compiler Options](compiler-options.md).</span></span>|
|<span data-ttu-id="c7468-168">**--optimize**[**+**&#124;**-**]</span><span class="sxs-lookup"><span data-stu-id="c7468-168">**--optimize**[**+**&#124;**-**]</span></span>|<span data-ttu-id="c7468-169">与相同**fsc.exe**编译器选项。</span><span class="sxs-lookup"><span data-stu-id="c7468-169">Same as the **fsc.exe** compiler option.</span></span> <span data-ttu-id="c7468-170">有关详细信息，请参阅[编译器选项](compiler-options.md)。</span><span class="sxs-lookup"><span data-stu-id="c7468-170">For more information, see [Compiler Options](compiler-options.md).</span></span>|
|<span data-ttu-id="c7468-171">**--preferreduilang:&lt;lang&gt;**</span><span class="sxs-lookup"><span data-stu-id="c7468-171">**--preferreduilang:&lt;lang&gt;**</span></span>| <span data-ttu-id="c7468-172">指定首选的输出语言区域性名称 （例如，ES-ES、 JA-JP）。</span><span class="sxs-lookup"><span data-stu-id="c7468-172">Specifies the preferred output language culture name (for example, es-ES, ja-JP).</span></span> |
|<span data-ttu-id="c7468-173">**--quiet**</span><span class="sxs-lookup"><span data-stu-id="c7468-173">**--quiet**</span></span>|<span data-ttu-id="c7468-174">禁止显示 F # Interactive 的输出到**stdout**流。</span><span class="sxs-lookup"><span data-stu-id="c7468-174">Suppress F# Interactive's output to the **stdout** stream.</span></span>|
|<span data-ttu-id="c7468-175">**--quotations-debug**</span><span class="sxs-lookup"><span data-stu-id="c7468-175">**--quotations-debug**</span></span>|<span data-ttu-id="c7468-176">指定应从 F # 引号文本派生，并反映定义的表达式发出额外的调试信息。</span><span class="sxs-lookup"><span data-stu-id="c7468-176">Specifies that extra debugging information should be emitted for expressions that are derived from F# quotation literals and reflected definitions.</span></span> <span data-ttu-id="c7468-177">调试信息添加到 F # 表达式树节点的自定义属性。</span><span class="sxs-lookup"><span data-stu-id="c7468-177">The debug information is added to the custom attributes of an F# expression tree node.</span></span> <span data-ttu-id="c7468-178">请参阅[代码引用](code-quotations.md)和[Expr.CustomAttributes](https://msdn.microsoft.com/library/eb89943f-5f5b-474e-b125-030ca412edb3)。</span><span class="sxs-lookup"><span data-stu-id="c7468-178">See [Code Quotations](code-quotations.md) and [Expr.CustomAttributes](https://msdn.microsoft.com/library/eb89943f-5f5b-474e-b125-030ca412edb3).</span></span>|
|<span data-ttu-id="c7468-179">**--readline**[**+**&#124;**-**]</span><span class="sxs-lookup"><span data-stu-id="c7468-179">**--readline**[**+**&#124;**-**]</span></span>|<span data-ttu-id="c7468-180">启用或禁用在交互模式中的 tab 自动补全。</span><span class="sxs-lookup"><span data-stu-id="c7468-180">Enable or disable tab completion in interactive mode.</span></span>|
|<span data-ttu-id="c7468-181">**--reference:&lt;filename&gt;**</span><span class="sxs-lookup"><span data-stu-id="c7468-181">**--reference:&lt;filename&gt;**</span></span><br /><br /><span data-ttu-id="c7468-182">**-r:&lt;filename&gt;**</span><span class="sxs-lookup"><span data-stu-id="c7468-182">**-r:&lt;filename&gt;**</span></span>|<span data-ttu-id="c7468-183">与相同**fsc.exe**编译器选项。</span><span class="sxs-lookup"><span data-stu-id="c7468-183">Same as the **fsc.exe** compiler option.</span></span> <span data-ttu-id="c7468-184">有关详细信息，请参阅[编译器选项](compiler-options.md)。</span><span class="sxs-lookup"><span data-stu-id="c7468-184">For more information, see [Compiler Options](compiler-options.md).</span></span>|
|<span data-ttu-id="c7468-185">**--tailcalls**[**+**&#124;**-**]</span><span class="sxs-lookup"><span data-stu-id="c7468-185">**--tailcalls**[**+**&#124;**-**]</span></span>|<span data-ttu-id="c7468-186">启用或禁用的结尾 IL 指令，这会导致堆栈帧要重用为尾递归函数使用。</span><span class="sxs-lookup"><span data-stu-id="c7468-186">Enable or disable the use of the tail IL instruction, which causes the stack frame to be reused for tail recursive functions.</span></span> <span data-ttu-id="c7468-187">默认情况下会启用此选项。</span><span class="sxs-lookup"><span data-stu-id="c7468-187">This option is enabled by default.</span></span>|
|<span data-ttu-id="c7468-188">**--use:&lt;filename&gt;**</span><span class="sxs-lookup"><span data-stu-id="c7468-188">**--use:&lt;filename&gt;**</span></span>|<span data-ttu-id="c7468-189">告知解释程序以使用上启动的给定的文件作为初始的输入。</span><span class="sxs-lookup"><span data-stu-id="c7468-189">Tells the interpreter to use the given file on startup as initial input.</span></span>|
|<span data-ttu-id="c7468-190">**--utf8output**</span><span class="sxs-lookup"><span data-stu-id="c7468-190">**--utf8output**</span></span>|<span data-ttu-id="c7468-191">Fsc.exe 编译器选项相同。</span><span class="sxs-lookup"><span data-stu-id="c7468-191">Same as the fsc.exe compiler option.</span></span> <span data-ttu-id="c7468-192">有关详细信息，请参阅[编译器选项](compiler-options.md)。</span><span class="sxs-lookup"><span data-stu-id="c7468-192">For more information, see [Compiler Options](compiler-options.md).</span></span>|
|<span data-ttu-id="c7468-193">**--warn:&lt;warning-level&gt;**</span><span class="sxs-lookup"><span data-stu-id="c7468-193">**--warn:&lt;warning-level&gt;**</span></span>|<span data-ttu-id="c7468-194">与相同**fsc.exe**编译器选项。</span><span class="sxs-lookup"><span data-stu-id="c7468-194">Same as the **fsc.exe** compiler option.</span></span> <span data-ttu-id="c7468-195">有关详细信息，请参阅[编译器选项](compiler-options.md)。</span><span class="sxs-lookup"><span data-stu-id="c7468-195">For more information, see [Compiler Options](compiler-options.md).</span></span>|
|<span data-ttu-id="c7468-196">**--warnaserror**[**+**&#124;**-**]</span><span class="sxs-lookup"><span data-stu-id="c7468-196">**--warnaserror**[**+**&#124;**-**]</span></span>|<span data-ttu-id="c7468-197">与相同**fsc.exe**编译器选项。</span><span class="sxs-lookup"><span data-stu-id="c7468-197">Same as the **fsc.exe** compiler option.</span></span> <span data-ttu-id="c7468-198">有关详细信息，请参阅[编译器选项](compiler-options.md)。</span><span class="sxs-lookup"><span data-stu-id="c7468-198">For more information, see [Compiler Options](compiler-options.md).</span></span>|
|<span data-ttu-id="c7468-199">**--warnaserror**[**+**&#124;**-**]:**&lt;int-list&gt;**</span><span class="sxs-lookup"><span data-stu-id="c7468-199">**--warnaserror**[**+**&#124;**-**]:**&lt;int-list&gt;**</span></span>|<span data-ttu-id="c7468-200">与相同**fsc.exe**编译器选项。</span><span class="sxs-lookup"><span data-stu-id="c7468-200">Same as the **fsc.exe** compiler option.</span></span> <span data-ttu-id="c7468-201">有关详细信息，请参阅[编译器选项](compiler-options.md)。</span><span class="sxs-lookup"><span data-stu-id="c7468-201">For more information, see [Compiler Options](compiler-options.md).</span></span>|

## <a name="related-topics"></a><span data-ttu-id="c7468-202">相关主题</span><span class="sxs-lookup"><span data-stu-id="c7468-202">Related Topics</span></span>

|<span data-ttu-id="c7468-203">标题</span><span class="sxs-lookup"><span data-stu-id="c7468-203">Title</span></span>|<span data-ttu-id="c7468-204">描述</span><span class="sxs-lookup"><span data-stu-id="c7468-204">Description</span></span>|
|-----|-----------|
|[<span data-ttu-id="c7468-205">编译器选项</span><span class="sxs-lookup"><span data-stu-id="c7468-205">Compiler Options</span></span>](compiler-options.md)|<span data-ttu-id="c7468-206">描述 F # 编译器，可用的命令行选项**fsc.exe**。</span><span class="sxs-lookup"><span data-stu-id="c7468-206">Describes command line options available for the F# compiler, **fsc.exe**.</span></span>|