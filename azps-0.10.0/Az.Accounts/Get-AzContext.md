---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Get-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Get-AzContext.md
ms.openlocfilehash: e56452d14f9c0f17b4f744d08fdd5911fb39aff5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935261"
---
# <span data-ttu-id="f050c-101">Get-AzContext</span><span class="sxs-lookup"><span data-stu-id="f050c-101">Get-AzContext</span></span>

## <span data-ttu-id="f050c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f050c-102">SYNOPSIS</span></span>
<span data-ttu-id="f050c-103">Azure Resource Manager isteklerinin kimlik doğrulaması için kullanılan meta verileri alır.</span><span class="sxs-lookup"><span data-stu-id="f050c-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

## <span data-ttu-id="f050c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f050c-104">SYNTAX</span></span>

### <span data-ttu-id="f050c-105">GetSingleContext (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f050c-105">GetSingleContext (Default)</span></span>
```
Get-AzContext [-DefaultProfile <IAzureContextContainer>] [[-Name] <String>] [<CommonParameters>]
```

### <span data-ttu-id="f050c-106">Listallbağlamları</span><span class="sxs-lookup"><span data-stu-id="f050c-106">ListAllContexts</span></span>
```
Get-AzContext [-ListAvailable] [-RefreshContextFromTokenCache] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f050c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f050c-107">DESCRIPTION</span></span>
<span data-ttu-id="f050c-108">Get-AzContext cmdlet 'i, Azure Resource Manager isteklerinin kimlik doğrulaması için kullanılan geçerli meta verileri alır.</span><span class="sxs-lookup"><span data-stu-id="f050c-108">The Get-AzContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>
<span data-ttu-id="f050c-109">Bu cmdlet Active Directory hesabını, Active Directory kiracısı, Azure aboneliğini ve hedeflenen Azure ortamını alır.</span><span class="sxs-lookup"><span data-stu-id="f050c-109">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="f050c-110">Azure Resource Manager cmdlet 'leri Azure Resource Manager istekleri yaparken varsayılan olarak bu ayarları kullanın.</span><span class="sxs-lookup"><span data-stu-id="f050c-110">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="f050c-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f050c-111">EXAMPLES</span></span>

### <span data-ttu-id="f050c-112">Örnek 1: geçerli bağlamı alma</span><span class="sxs-lookup"><span data-stu-id="f050c-112">Example 1: Getting the current context</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="f050c-113">Bu örnekte, Connect-AzAccount öğesini kullanarak bir Azure aboneliğiyle hesabınıza oturum açıyoruz ve ardından Get-AzContext 'i çağırarak geçerli oturumun bağlamını alıyoruz.</span><span class="sxs-lookup"><span data-stu-id="f050c-113">In this example we are logging into our account with an Azure subscription using Connect-AzAccount, and then we are getting the context of the current session by calling Get-AzContext.</span></span>

### <span data-ttu-id="f050c-114">Örnek 2: kullanılabilir tüm bağlamların listelenmesi</span><span class="sxs-lookup"><span data-stu-id="f050c-114">Example 2: Listing all available contexts</span></span>
```
PS C:\> Get-AzContext -ListAvailable

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
Subscription2 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription2       AzureCloud          xxxxxxxx-x...
Subscription3 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription3       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="f050c-115">Bu örnekte, kullanılabilen tüm içerikler görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="f050c-115">In this example, all currently available contexts are displayed.</span></span>  <span data-ttu-id="f050c-116">Kullanıcı, select-AzContext kullanarak bu bağlamların birini seçebilir.</span><span class="sxs-lookup"><span data-stu-id="f050c-116">The user may select one of these contexts using Select-AzContext.</span></span>

## <span data-ttu-id="f050c-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f050c-117">PARAMETERS</span></span>

### <span data-ttu-id="f050c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f050c-118">-DefaultProfile</span></span>
<span data-ttu-id="f050c-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f050c-119">The credentials, account, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f050c-120">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="f050c-120">-ListAvailable</span></span>
<span data-ttu-id="f050c-121">Geçerli oturumdaki kullanılabilir tüm içeriği listeler.</span><span class="sxs-lookup"><span data-stu-id="f050c-121">List all available contexts in the current session.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAllContexts
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f050c-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="f050c-122">-Name</span></span>
<span data-ttu-id="f050c-123">İçeriğin adı</span><span class="sxs-lookup"><span data-stu-id="f050c-123">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: GetSingleContext
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f050c-124">-RefreshContextFromTokenCache</span><span class="sxs-lookup"><span data-stu-id="f050c-124">-RefreshContextFromTokenCache</span></span>
<span data-ttu-id="f050c-125">İçerik belirteci önbelleğinden yenileme</span><span class="sxs-lookup"><span data-stu-id="f050c-125">Refresh contexts from token cache</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAllContexts
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f050c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f050c-126">CommonParameters</span></span>
<span data-ttu-id="f050c-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f050c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f050c-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f050c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f050c-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f050c-129">INPUTS</span></span>

### <span data-ttu-id="f050c-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f050c-130">None</span></span>

## <span data-ttu-id="f050c-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f050c-131">OUTPUTS</span></span>

### <span data-ttu-id="f050c-132">Microsoft. Azure. Commands. Profile. modeller. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="f050c-132">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="f050c-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f050c-133">NOTES</span></span>

## <span data-ttu-id="f050c-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f050c-134">RELATED LINKS</span></span>

[<span data-ttu-id="f050c-135">Set-AzContext</span><span class="sxs-lookup"><span data-stu-id="f050c-135">Set-AzContext</span></span>](./Set-AzContext.md)

