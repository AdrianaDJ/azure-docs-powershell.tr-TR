---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/remove-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Remove-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Remove-AzSubscriptionAlias.md
ms.openlocfilehash: 02a32b3e6c39ae66aea8efc37213a6fb3bca0848
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277973"
---
# <span data-ttu-id="1b4de-101">Remove-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="1b4de-101">Remove-AzSubscriptionAlias</span></span>

## <span data-ttu-id="1b4de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b4de-102">SYNOPSIS</span></span>
<span data-ttu-id="1b4de-103">Abonelik diğer adını siler</span><span class="sxs-lookup"><span data-stu-id="1b4de-103">Deletes the subscription alias</span></span>

## <span data-ttu-id="1b4de-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1b4de-104">SYNTAX</span></span>

```
Remove-AzSubscriptionAlias -AliasName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b4de-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1b4de-105">DESCRIPTION</span></span>
<span data-ttu-id="1b4de-106">**Remove-AzSubscriptionAlias** cmdlet 'i, abonelik diğer adını kaldırır</span><span class="sxs-lookup"><span data-stu-id="1b4de-106">The **Remove-AzSubscriptionAlias** cmdlet removes the subscription alias</span></span>

## <span data-ttu-id="1b4de-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1b4de-107">EXAMPLES</span></span>

### <span data-ttu-id="1b4de-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1b4de-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzSubscriptionAlias -AliasName "ExistingAliasName"
```

<span data-ttu-id="1b4de-109">Abonelik diğer adını siler</span><span class="sxs-lookup"><span data-stu-id="1b4de-109">Deletes the subscription alias</span></span>

## <span data-ttu-id="1b4de-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1b4de-110">PARAMETERS</span></span>

### <span data-ttu-id="1b4de-111">-Diğerad</span><span class="sxs-lookup"><span data-stu-id="1b4de-111">-AliasName</span></span>
<span data-ttu-id="1b4de-112">Abonelik için diğer ad</span><span class="sxs-lookup"><span data-stu-id="1b4de-112">Alias for the subscription</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b4de-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="1b4de-113">-AsJob</span></span>
<span data-ttu-id="1b4de-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="1b4de-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b4de-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b4de-115">-DefaultProfile</span></span>
<span data-ttu-id="1b4de-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1b4de-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b4de-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="1b4de-117">-Confirm</span></span>
<span data-ttu-id="1b4de-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1b4de-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b4de-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b4de-119">-WhatIf</span></span>
<span data-ttu-id="1b4de-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1b4de-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b4de-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1b4de-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b4de-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b4de-122">CommonParameters</span></span>
<span data-ttu-id="1b4de-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1b4de-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b4de-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1b4de-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b4de-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1b4de-125">INPUTS</span></span>

### <span data-ttu-id="1b4de-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1b4de-126">None</span></span>

## <span data-ttu-id="1b4de-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1b4de-127">OUTPUTS</span></span>

### <span data-ttu-id="1b4de-128">Microsoft. Azure. Commands. Subscription. modeller. psazuyeniden gönderme komutları</span><span class="sxs-lookup"><span data-stu-id="1b4de-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="1b4de-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1b4de-129">NOTES</span></span>

## <span data-ttu-id="1b4de-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1b4de-130">RELATED LINKS</span></span>
