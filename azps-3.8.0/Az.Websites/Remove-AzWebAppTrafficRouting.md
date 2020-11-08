---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppTrafficRouting.md
ms.openlocfilehash: 0dda79130d150265d8050fcb5ba951cd243bebda
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098396"
---
# <span data-ttu-id="de85b-101">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="de85b-101">Remove-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="de85b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de85b-102">SYNOPSIS</span></span>
<span data-ttu-id="de85b-103">Bir yönlendirme kuralını yuvadan kaldırın.</span><span class="sxs-lookup"><span data-stu-id="de85b-103">Remove a routing Rule from the Slot.</span></span>

## <span data-ttu-id="de85b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="de85b-104">SYNTAX</span></span>

```
Remove-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RuleName <String>
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de85b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="de85b-105">DESCRIPTION</span></span>
<span data-ttu-id="de85b-106">**Remove-AzWebAppTrafficRouting** cmdlet 'ı, Azure Web App yuvasından yönlendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="de85b-106">The **Remove-AzWebAppTrafficRouting** cmdlet removes a routing rule from an Azure Web App Slot.</span></span>

## <span data-ttu-id="de85b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="de85b-107">EXAMPLES</span></span>

### <span data-ttu-id="de85b-108">Örnek 1 belirli yönlendirme kuralını WebApp yuvasından kaldırır</span><span class="sxs-lookup"><span data-stu-id="de85b-108">Example 1 Removes the specific routing rule from webapp slot</span></span>
```powershell
PS C:\> Remove-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite"  -RuleName 'Stg'
```

<span data-ttu-id="de85b-109">Bu komut, belirli bir WebApp yuvasının yönlendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="de85b-109">This command removes a routing rule for a given webapp slot.</span></span>

## <span data-ttu-id="de85b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="de85b-110">PARAMETERS</span></span>

### <span data-ttu-id="de85b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de85b-111">-DefaultProfile</span></span>
<span data-ttu-id="de85b-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="de85b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de85b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de85b-113">-ResourceGroupName</span></span>
<span data-ttu-id="de85b-114">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="de85b-114">Resource Group Name</span></span>

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

### <span data-ttu-id="de85b-115">-RuleName</span><span class="sxs-lookup"><span data-stu-id="de85b-115">-RuleName</span></span>
<span data-ttu-id="de85b-116">Kural adı</span><span class="sxs-lookup"><span data-stu-id="de85b-116">Rule Name</span></span>

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

### <span data-ttu-id="de85b-117">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="de85b-117">-WebAppName</span></span>
<span data-ttu-id="de85b-118">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="de85b-118">WebApp Name</span></span>

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

### <span data-ttu-id="de85b-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="de85b-119">-PassThru</span></span>
<span data-ttu-id="de85b-120">Erişim kısıtlama yapılandırması nesnesini döndür.</span><span class="sxs-lookup"><span data-stu-id="de85b-120">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="de85b-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="de85b-121">-Confirm</span></span>
<span data-ttu-id="de85b-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="de85b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de85b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de85b-123">-WhatIf</span></span>
<span data-ttu-id="de85b-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="de85b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de85b-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="de85b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de85b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de85b-126">CommonParameters</span></span>
<span data-ttu-id="de85b-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="de85b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de85b-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="de85b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de85b-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="de85b-129">INPUTS</span></span>

### <span data-ttu-id="de85b-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="de85b-130">None</span></span>

## <span data-ttu-id="de85b-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="de85b-131">OUTPUTS</span></span>

### <span data-ttu-id="de85b-132">Microsoft. Azure. Management. Web sitesi. modeller. RampUpRule</span><span class="sxs-lookup"><span data-stu-id="de85b-132">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="de85b-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="de85b-133">NOTES</span></span>

## <span data-ttu-id="de85b-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="de85b-134">RELATED LINKS</span></span>
[<span data-ttu-id="de85b-135">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="de85b-135">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="de85b-136">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="de85b-136">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="de85b-137">Güncelleştirme-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="de85b-137">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)