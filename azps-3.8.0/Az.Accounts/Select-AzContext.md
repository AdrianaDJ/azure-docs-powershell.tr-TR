---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/select-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Select-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Select-AzContext.md
ms.openlocfilehash: 6f3ff6868a34eefc9b7cd45cf371b6ef29dbf469
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097476"
---
# <span data-ttu-id="a76ed-101">Select-AzContext</span><span class="sxs-lookup"><span data-stu-id="a76ed-101">Select-AzContext</span></span>

## <span data-ttu-id="a76ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a76ed-102">SYNOPSIS</span></span>
<span data-ttu-id="a76ed-103">Azure PowerShell cmdlet 'leriyle hedef için bir abonelik ve hesap seçin</span><span class="sxs-lookup"><span data-stu-id="a76ed-103">Select a subscription and account to target in Azure PowerShell cmdlets</span></span>

## <span data-ttu-id="a76ed-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a76ed-104">SYNTAX</span></span>

### <span data-ttu-id="a76ed-105">SelectByInputObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a76ed-105">SelectByInputObject (Default)</span></span>
```
Select-AzContext -InputObject <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a76ed-106">SelectByName</span><span class="sxs-lookup"><span data-stu-id="a76ed-106">SelectByName</span></span>
```
Select-AzContext [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="a76ed-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a76ed-107">DESCRIPTION</span></span>
<span data-ttu-id="a76ed-108">Azure PowerShell cmdlet 'leriyle hedef (veya bir hesap veya kiracı) aboneliğini seçin.</span><span class="sxs-lookup"><span data-stu-id="a76ed-108">Select a  subscription to target (or account or tenant) in Azure PowerShell cmdlets.</span></span>  <span data-ttu-id="a76ed-109">Bu cmdlet 'in ardından, gelecekteki cmdlet 'ler seçilen içeriği hedefedecektir.</span><span class="sxs-lookup"><span data-stu-id="a76ed-109">After this cmdlet, future cmdlets will target the selected context.</span></span>

## <span data-ttu-id="a76ed-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a76ed-110">EXAMPLES</span></span>

### <span data-ttu-id="a76ed-111">Örnek 1: adlandırılmış bir bağlamı hedefleyin</span><span class="sxs-lookup"><span data-stu-id="a76ed-111">Example 1 : Target a named context</span></span>
```
PS C:\> Select-AzContext "Work"

Name    Account             SubscriptionName    Environment         TenantId
----    -------             ----------------    -----------         --------
Work    test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="a76ed-112">' Iş ' bağlamındaki hesap, kiracı ve abonelikteki gelecekteki Azure PowerShell cmdlet 'lerini hedefleyin.</span><span class="sxs-lookup"><span data-stu-id="a76ed-112">Target future Azure PowerShell cmdlets at the account, tenant, and subscription in the 'Work' context.</span></span>

## <span data-ttu-id="a76ed-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a76ed-113">PARAMETERS</span></span>

### <span data-ttu-id="a76ed-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a76ed-114">-DefaultProfile</span></span>
<span data-ttu-id="a76ed-115">Azure ile iletişimde kullanılan kimlik bilgileri, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a76ed-115">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a76ed-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a76ed-116">-InputObject</span></span>
<span data-ttu-id="a76ed-117">Normalde ardışık düzen aracılığıyla iletilen bir bağlam nesnesi.</span><span class="sxs-lookup"><span data-stu-id="a76ed-117">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: SelectByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a76ed-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="a76ed-118">-Name</span></span>
<span data-ttu-id="a76ed-119">İçeriğin adı</span><span class="sxs-lookup"><span data-stu-id="a76ed-119">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: SelectByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a76ed-120">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="a76ed-120">-Scope</span></span>
<span data-ttu-id="a76ed-121">Değişikliklerin kapsamını, örneğin değişikliklerin yalnızca geçerli işleme veya bu kullanıcı tarafından başlatılan tüm oturumlara uygulanmasını belirler</span><span class="sxs-lookup"><span data-stu-id="a76ed-121">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a76ed-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="a76ed-122">-Confirm</span></span>
<span data-ttu-id="a76ed-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a76ed-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a76ed-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a76ed-124">-WhatIf</span></span>
<span data-ttu-id="a76ed-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a76ed-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a76ed-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a76ed-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a76ed-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a76ed-127">CommonParameters</span></span>
<span data-ttu-id="a76ed-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a76ed-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a76ed-129">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a76ed-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a76ed-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a76ed-130">INPUTS</span></span>

### <span data-ttu-id="a76ed-131">Microsoft. Azure. Commands. Profile. modeller. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="a76ed-131">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="a76ed-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a76ed-132">OUTPUTS</span></span>

### <span data-ttu-id="a76ed-133">Microsoft. Azure. Commands. Profile. modeller. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="a76ed-133">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="a76ed-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a76ed-134">NOTES</span></span>

## <span data-ttu-id="a76ed-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a76ed-135">RELATED LINKS</span></span>
