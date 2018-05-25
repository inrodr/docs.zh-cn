### <a name="support-special-relative-uri-notation-when-unicode-is-present"></a><span data-ttu-id="c4152-101">存在 Unicode 时支持特殊的相对 URI 表示法</span><span class="sxs-lookup"><span data-stu-id="c4152-101">Support special relative URI notation when Unicode is present</span></span>

|   |   |
|---|---|
|<span data-ttu-id="c4152-102">详细信息</span><span class="sxs-lookup"><span data-stu-id="c4152-102">Details</span></span>|<span data-ttu-id="c4152-103">在包含 Unicode 的特定相对 URI 上调用 <xref:System.Uri.TryCreate%2A> 时，<xref:System.Uri> 不再引发 <xref:System.NullReferenceException>。以下是最简单的 <xref:System.NullReferenceException> 重现，两个语句等效：</span><span class="sxs-lookup"><span data-stu-id="c4152-103"><xref:System.Uri> will no longer throw a <xref:System.NullReferenceException> when calling <xref:System.Uri.TryCreate%2A> on certain relative URIs containing Unicode.The simplest reproduction of the <xref:System.NullReferenceException> is below, with the two statements being equivalent:</span></span><pre><code class="lang-csharp">bool success = Uri.TryCreate(&quot;http:%C3%A8&quot;, UriKind.RelativeOrAbsolute, out Uri href);&#13;&#10;bool success = Uri.TryCreate(&quot;http:&#232;&quot;, UriKind.RelativeOrAbsolute, out Uri href);&#13;&#10;</code></pre><span data-ttu-id="c4152-104">若要重现 <xref:System.NullReferenceException>，以下各项必须为 true：</span><span class="sxs-lookup"><span data-stu-id="c4152-104">To reproduce the <xref:System.NullReferenceException>, the following items must be true:</span></span><ul><li><span data-ttu-id="c4152-105">必须将 URI 指定为相对，方法是在其前追加“http:”，且其后不跟“//”。</span><span class="sxs-lookup"><span data-stu-id="c4152-105">The URI must be specified as relative by prepending it with ‘http:’ and not following it with ‘//’.</span></span></li><li><span data-ttu-id="c4152-106">URI 必须包含百分比编码的 Unicode 或未保留的符号。</span><span class="sxs-lookup"><span data-stu-id="c4152-106">The URI must contain percent-encoded Unicode or unreserved symbols.</span></span></li></ul>|
|<span data-ttu-id="c4152-107">建议</span><span class="sxs-lookup"><span data-stu-id="c4152-107">Suggestion</span></span>|<span data-ttu-id="c4152-108">根据此行为禁用相对 URI 的用户应在创建 URI 时转而指定 <xref:System.UriKind.Absolute?displayProperty=nameWithType>。</span><span class="sxs-lookup"><span data-stu-id="c4152-108">Users depending on this behavior to disallow relative URIs should instead specify <xref:System.UriKind.Absolute?displayProperty=nameWithType> when creating a URI.</span></span>|
|<span data-ttu-id="c4152-109">范围</span><span class="sxs-lookup"><span data-stu-id="c4152-109">Scope</span></span>|<span data-ttu-id="c4152-110">边缘</span><span class="sxs-lookup"><span data-stu-id="c4152-110">Edge</span></span>|
|<span data-ttu-id="c4152-111">版本</span><span class="sxs-lookup"><span data-stu-id="c4152-111">Version</span></span>|<span data-ttu-id="c4152-112">4.7.2</span><span class="sxs-lookup"><span data-stu-id="c4152-112">4.7.2</span></span>|
|<span data-ttu-id="c4152-113">类型</span><span class="sxs-lookup"><span data-stu-id="c4152-113">Type</span></span>|<span data-ttu-id="c4152-114">运行时</span><span class="sxs-lookup"><span data-stu-id="c4152-114">Runtime</span></span>|
|<span data-ttu-id="c4152-115">受影响的 API</span><span class="sxs-lookup"><span data-stu-id="c4152-115">Affected APIs</span></span>|<ul><li><xref:System.Uri.TryCreate(System.Uri,System.Uri,System.Uri@)?displayProperty=nameWithType></li><li><xref:System.Uri.TryCreate(System.String,System.UriKind,System.Uri@)?displayProperty=nameWithType></li><li><xref:System.Uri.TryCreate(System.Uri,System.String,System.Uri@)?displayProperty=nameWithType></li></ul>|
