---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/get-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Get-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Get-AzSubscriptionAlias.md
ms.openlocfilehash: a76c993abb254b1e24200267bf0195cb613d8207
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277978"
---
# <span data-ttu-id="b482c-101">Get-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="b482c-101">Get-AzSubscriptionAlias</span></span>

## <span data-ttu-id="b482c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b482c-102">SYNOPSIS</span></span>
<span data-ttu-id="b482c-103">Abonelik diğer adı ayrıntılarını alır</span><span class="sxs-lookup"><span data-stu-id="b482c-103">Gets subscription alias details</span></span>

## <span data-ttu-id="b482c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b482c-104">SYNTAX</span></span>

```
Get-AzSubscriptionAlias [-AliasName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b482c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b482c-105">DESCRIPTION</span></span>
<span data-ttu-id="b482c-106">**Get-AzSubscriptionAlias** cmdlet 'i abonelik diğer adı ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="b482c-106">The **Get-AzSubscriptionAlias** cmdlet gets subscription alias details.</span></span>

## <span data-ttu-id="b482c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b482c-107">EXAMPLES</span></span>

### <span data-ttu-id="b482c-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b482c-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSubscriptionAlias -AliasName "ExistingAliasName"
```

<span data-ttu-id="b482c-109">Abonelik diğer adı ayrıntılarını alır</span><span class="sxs-lookup"><span data-stu-id="b482c-109">Gets subscription alias details</span></span>

## <span data-ttu-id="b482c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b482c-110">PARAMETERS</span></span>

### <span data-ttu-id="b482c-111">-Diğerad</span><span class="sxs-lookup"><span data-stu-id="b482c-111">-AliasName</span></span>
<span data-ttu-id="b482c-112">Abonelik için diğer ad</span><span class="sxs-lookup"><span data-stu-id="b482c-112">Alias for the subscription</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b482c-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="b482c-113">-AsJob</span></span>
<span data-ttu-id="b482c-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="b482c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b482c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b482c-115">-DefaultProfile</span></span>
<span data-ttu-id="b482c-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b482c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b482c-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="b482c-117">-Confirm</span></span>
<span data-ttu-id="b482c-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b482c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b482c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b482c-119">-WhatIf</span></span>
<span data-ttu-id="b482c-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b482c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b482c-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b482c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b482c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b482c-122">CommonParameters</span></span>
<span data-ttu-id="b482c-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b482c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b482c-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b482c-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b482c-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b482c-125">INPUTS</span></span>

### <span data-ttu-id="b482c-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b482c-126">None</span></span>

## <span data-ttu-id="b482c-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b482c-127">OUTPUTS</span></span>

### <span data-ttu-id="b482c-128">Microsoft. Azure. Commands. Subscription. modeller. psazuyeniden gönderme komutları</span><span class="sxs-lookup"><span data-stu-id="b482c-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="b482c-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b482c-129">NOTES</span></span>

## <span data-ttu-id="b482c-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b482c-130">RELATED LINKS</span></span>
