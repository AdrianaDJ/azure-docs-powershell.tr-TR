---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 198d52678bceccfd1045522881dc3a62fdebf752
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937845"
---
# <span data-ttu-id="4ea8e-101">New-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="4ea8e-101">New-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="4ea8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ea8e-102">SYNOPSIS</span></span>
<span data-ttu-id="4ea8e-103">özel bağlantı kapsamı oluşturma</span><span class="sxs-lookup"><span data-stu-id="4ea8e-103">create private link scope</span></span>

## <span data-ttu-id="4ea8e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4ea8e-104">SYNTAX</span></span>

```
New-AzInsightsPrivateLinkScope -Location <String> -ResourceGroupName <String> -Name <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ea8e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4ea8e-105">DESCRIPTION</span></span>
<span data-ttu-id="4ea8e-106">özel bağlantı kapsamı oluşturma</span><span class="sxs-lookup"><span data-stu-id="4ea8e-106">create private link scope</span></span>

## <span data-ttu-id="4ea8e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4ea8e-107">EXAMPLES</span></span>

### <span data-ttu-id="4ea8e-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4ea8e-108">Example 1</span></span>
```powershell
New-AzInsightsPrivateLinkScope -Location "eastus" -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="4ea8e-109">"eastus" kaynak rg_name grubu altındaki "scope_name" adlı özel bağlantı kapsamını oluşturma</span><span class="sxs-lookup"><span data-stu-id="4ea8e-109">create private link scope with name "scope_name" under resource group "rg_name" in location "eastus"</span></span>

## <span data-ttu-id="4ea8e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4ea8e-110">PARAMETERS</span></span>

### <span data-ttu-id="4ea8e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ea8e-111">-DefaultProfile</span></span>
<span data-ttu-id="4ea8e-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4ea8e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ea8e-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="4ea8e-113">-Location</span></span>
<span data-ttu-id="4ea8e-114">Konumuyla</span><span class="sxs-lookup"><span data-stu-id="4ea8e-114">Location</span></span>

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

### <span data-ttu-id="4ea8e-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="4ea8e-115">-Name</span></span>
<span data-ttu-id="4ea8e-116">Özel bağlantı kapsamı adı</span><span class="sxs-lookup"><span data-stu-id="4ea8e-116">Private Link Scope Name</span></span>

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

### <span data-ttu-id="4ea8e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ea8e-117">-ResourceGroupName</span></span>
<span data-ttu-id="4ea8e-118">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="4ea8e-118">Resource Group Name</span></span>

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

### <span data-ttu-id="4ea8e-119">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="4ea8e-119">-Tags</span></span>
<span data-ttu-id="4ea8e-120">Akıllı</span><span class="sxs-lookup"><span data-stu-id="4ea8e-120">Tags</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ea8e-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="4ea8e-121">-Confirm</span></span>
<span data-ttu-id="4ea8e-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4ea8e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ea8e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ea8e-123">-WhatIf</span></span>
<span data-ttu-id="4ea8e-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4ea8e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ea8e-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4ea8e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ea8e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ea8e-126">CommonParameters</span></span>
<span data-ttu-id="4ea8e-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4ea8e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ea8e-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4ea8e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ea8e-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4ea8e-129">INPUTS</span></span>

### <span data-ttu-id="4ea8e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4ea8e-130">System.String</span></span>

## <span data-ttu-id="4ea8e-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4ea8e-131">OUTPUTS</span></span>

### <span data-ttu-id="4ea8e-132">Microsoft. Azure. Commands. Insights. OutputClasses. Psmte ıtorprivatelinkscope</span><span class="sxs-lookup"><span data-stu-id="4ea8e-132">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="4ea8e-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4ea8e-133">NOTES</span></span>

## <span data-ttu-id="4ea8e-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4ea8e-134">RELATED LINKS</span></span>