---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContext.md
ms.openlocfilehash: 0f306b7e42dbe5b37c1c814a9458a5e1fb81cc7d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751280"
---
# <span data-ttu-id="a0b17-101">Get-AzContext</span><span class="sxs-lookup"><span data-stu-id="a0b17-101">Get-AzContext</span></span>

## <span data-ttu-id="a0b17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0b17-102">SYNOPSIS</span></span>
<span data-ttu-id="a0b17-103">Azure Resource Manager isteklerinin kimlik doğrulaması için kullanılan meta verileri alır.</span><span class="sxs-lookup"><span data-stu-id="a0b17-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

## <span data-ttu-id="a0b17-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a0b17-104">SYNTAX</span></span>

### <span data-ttu-id="a0b17-105">GetSingleContext (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a0b17-105">GetSingleContext (Default)</span></span>
```
Get-AzContext [-DefaultProfile <IAzureContextContainer>] [[-Name] <String>] [<CommonParameters>]
```

### <span data-ttu-id="a0b17-106">Listallbağlamları</span><span class="sxs-lookup"><span data-stu-id="a0b17-106">ListAllContexts</span></span>
```
Get-AzContext [-ListAvailable] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0b17-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a0b17-107">DESCRIPTION</span></span>
<span data-ttu-id="a0b17-108">Get-AzContext cmdlet 'i, Azure Resource Manager isteklerinin kimlik doğrulaması için kullanılan geçerli meta verileri alır.</span><span class="sxs-lookup"><span data-stu-id="a0b17-108">The Get-AzContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>
<span data-ttu-id="a0b17-109">Bu cmdlet Active Directory hesabını, Active Directory kiracısı, Azure aboneliğini ve hedeflenen Azure ortamını alır.</span><span class="sxs-lookup"><span data-stu-id="a0b17-109">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="a0b17-110">Azure Resource Manager cmdlet 'leri Azure Resource Manager istekleri yaparken varsayılan olarak bu ayarları kullanın.</span><span class="sxs-lookup"><span data-stu-id="a0b17-110">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="a0b17-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a0b17-111">EXAMPLES</span></span>

### <span data-ttu-id="a0b17-112">Örnek 1: geçerli bağlamı alma</span><span class="sxs-lookup"><span data-stu-id="a0b17-112">Example 1: Getting the current context</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="a0b17-113">Bu örnekte, Connect-AzAccount öğesini kullanarak bir Azure aboneliğiyle hesabınıza oturum açıyoruz ve ardından Get-AzContext 'i çağırarak geçerli oturumun bağlamını alıyoruz.</span><span class="sxs-lookup"><span data-stu-id="a0b17-113">In this example we are logging into our account with an Azure subscription using Connect-AzAccount, and then we are getting the context of the current session by calling Get-AzContext.</span></span>

### <span data-ttu-id="a0b17-114">Örnek 2: kullanılabilir tüm bağlamların listelenmesi</span><span class="sxs-lookup"><span data-stu-id="a0b17-114">Example 2: Listing all available contexts</span></span>
```
PS C:\> Get-AzContext -ListAvailable

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
Subscription2 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription2       AzureCloud          xxxxxxxx-x...
Subscription3 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription3       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="a0b17-115">Bu örnekte, kullanılabilen tüm içerikler görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="a0b17-115">In this example, all currently available contexts are displayed.</span></span>  <span data-ttu-id="a0b17-116">Kullanıcı, select-AzContext kullanarak bu bağlamların birini seçebilir.</span><span class="sxs-lookup"><span data-stu-id="a0b17-116">The user may select one of these contexts using Select-AzContext.</span></span>

## <span data-ttu-id="a0b17-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a0b17-117">PARAMETERS</span></span>

### <span data-ttu-id="a0b17-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0b17-118">-DefaultProfile</span></span>
<span data-ttu-id="a0b17-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a0b17-119">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0b17-120">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="a0b17-120">-ListAvailable</span></span>
<span data-ttu-id="a0b17-121">Geçerli oturumdaki kullanılabilir tüm içeriği listeler.</span><span class="sxs-lookup"><span data-stu-id="a0b17-121">List all available contexts in the current session.</span></span>

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

### <span data-ttu-id="a0b17-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="a0b17-122">-Name</span></span>
<span data-ttu-id="a0b17-123">İçeriğin adı</span><span class="sxs-lookup"><span data-stu-id="a0b17-123">The name of the context</span></span>

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

### <span data-ttu-id="a0b17-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0b17-124">CommonParameters</span></span>
<span data-ttu-id="a0b17-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a0b17-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0b17-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0b17-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0b17-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a0b17-127">INPUTS</span></span>

### <span data-ttu-id="a0b17-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a0b17-128">None</span></span>

## <span data-ttu-id="a0b17-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a0b17-129">OUTPUTS</span></span>

### <span data-ttu-id="a0b17-130">Microsoft. Azure. Commands. Profile. modeller. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="a0b17-130">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="a0b17-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a0b17-131">NOTES</span></span>

## <span data-ttu-id="a0b17-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a0b17-132">RELATED LINKS</span></span>

[<span data-ttu-id="a0b17-133">Set-AzContext</span><span class="sxs-lookup"><span data-stu-id="a0b17-133">Set-AzContext</span></span>](./Set-AzContext.md)

