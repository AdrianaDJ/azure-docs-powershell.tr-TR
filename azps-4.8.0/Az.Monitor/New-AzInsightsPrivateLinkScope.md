---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 198d52678bceccfd1045522881dc3a62fdebf752
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274428"
---
# <span data-ttu-id="5b227-101">New-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="5b227-101">New-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="5b227-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b227-102">SYNOPSIS</span></span>
<span data-ttu-id="5b227-103">özel bağlantı kapsamı oluşturma</span><span class="sxs-lookup"><span data-stu-id="5b227-103">create private link scope</span></span>

## <span data-ttu-id="5b227-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5b227-104">SYNTAX</span></span>

```
New-AzInsightsPrivateLinkScope -Location <String> -ResourceGroupName <String> -Name <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b227-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5b227-105">DESCRIPTION</span></span>
<span data-ttu-id="5b227-106">özel bağlantı kapsamı oluşturma</span><span class="sxs-lookup"><span data-stu-id="5b227-106">create private link scope</span></span>

## <span data-ttu-id="5b227-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5b227-107">EXAMPLES</span></span>

### <span data-ttu-id="5b227-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5b227-108">Example 1</span></span>
```powershell
New-AzInsightsPrivateLinkScope -Location "eastus" -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="5b227-109">"eastus" kaynak rg_name grubu altındaki "scope_name" adlı özel bağlantı kapsamını oluşturma</span><span class="sxs-lookup"><span data-stu-id="5b227-109">create private link scope with name "scope_name" under resource group "rg_name" in location "eastus"</span></span>

## <span data-ttu-id="5b227-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5b227-110">PARAMETERS</span></span>

### <span data-ttu-id="5b227-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b227-111">-DefaultProfile</span></span>
<span data-ttu-id="5b227-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5b227-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b227-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="5b227-113">-Location</span></span>
<span data-ttu-id="5b227-114">Konumuyla</span><span class="sxs-lookup"><span data-stu-id="5b227-114">Location</span></span>

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

### <span data-ttu-id="5b227-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="5b227-115">-Name</span></span>
<span data-ttu-id="5b227-116">Özel bağlantı kapsamı adı</span><span class="sxs-lookup"><span data-stu-id="5b227-116">Private Link Scope Name</span></span>

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

### <span data-ttu-id="5b227-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b227-117">-ResourceGroupName</span></span>
<span data-ttu-id="5b227-118">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="5b227-118">Resource Group Name</span></span>

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

### <span data-ttu-id="5b227-119">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="5b227-119">-Tags</span></span>
<span data-ttu-id="5b227-120">Akıllı</span><span class="sxs-lookup"><span data-stu-id="5b227-120">Tags</span></span>

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

### <span data-ttu-id="5b227-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="5b227-121">-Confirm</span></span>
<span data-ttu-id="5b227-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5b227-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b227-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b227-123">-WhatIf</span></span>
<span data-ttu-id="5b227-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5b227-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b227-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5b227-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b227-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b227-126">CommonParameters</span></span>
<span data-ttu-id="5b227-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5b227-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b227-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5b227-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b227-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5b227-129">INPUTS</span></span>

### <span data-ttu-id="5b227-130">System. String</span><span class="sxs-lookup"><span data-stu-id="5b227-130">System.String</span></span>

## <span data-ttu-id="5b227-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5b227-131">OUTPUTS</span></span>

### <span data-ttu-id="5b227-132">Microsoft. Azure. Commands. Insights. OutputClasses. Psmte ıtorprivatelinkscope</span><span class="sxs-lookup"><span data-stu-id="5b227-132">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="5b227-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5b227-133">NOTES</span></span>

## <span data-ttu-id="5b227-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5b227-134">RELATED LINKS</span></span>
