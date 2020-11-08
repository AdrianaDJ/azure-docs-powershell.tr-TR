---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilter.md
ms.openlocfilehash: 8be04cd9e483e990d73130866779710bbed879bb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098728"
---
# <span data-ttu-id="086e5-101">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="086e5-101">New-AzRouteFilter</span></span>

## <span data-ttu-id="086e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="086e5-102">SYNOPSIS</span></span>
<span data-ttu-id="086e5-103">Yol filtresi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="086e5-103">Creates a route filter.</span></span>

## <span data-ttu-id="086e5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="086e5-104">SYNTAX</span></span>

```
New-AzRouteFilter -Name <String> -ResourceGroupName <String> -Location <String> [-Rule <PSRouteFilterRule[]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="086e5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="086e5-105">DESCRIPTION</span></span>
<span data-ttu-id="086e5-106">New-AzRouteFilter cmdlet 'i Azure yol filtresi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="086e5-106">The New-AzRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="086e5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="086e5-107">EXAMPLES</span></span>

### <span data-ttu-id="086e5-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="086e5-108">Example 1</span></span>
```powershell
PS C:\> New-AzRouteFilter -Name "MyRouteFilter" -ResourceGroupName "MyResourceGroup" -Location "West US"
```

<span data-ttu-id="086e5-109">Komut yeni bir yol filtresi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="086e5-109">The command creates a new route filter.</span></span>

## <span data-ttu-id="086e5-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="086e5-110">PARAMETERS</span></span>

### <span data-ttu-id="086e5-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="086e5-111">-AsJob</span></span>
<span data-ttu-id="086e5-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="086e5-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="086e5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="086e5-113">-DefaultProfile</span></span>
<span data-ttu-id="086e5-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="086e5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="086e5-115">-Force</span><span class="sxs-lookup"><span data-stu-id="086e5-115">-Force</span></span>
<span data-ttu-id="086e5-116">Aynı ada sahip bir yol filtresi de olsa, bu cmdlet 'in yol tablosu oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="086e5-116">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

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

### <span data-ttu-id="086e5-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="086e5-117">-Location</span></span>
<span data-ttu-id="086e5-118">Bu cmdlet 'in yol filtresi oluşturduğu Azure bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="086e5-118">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="086e5-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="086e5-119">-Name</span></span>
<span data-ttu-id="086e5-120">Yol filtresi için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="086e5-120">Specifies a name for the route filter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="086e5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="086e5-121">-ResourceGroupName</span></span>
<span data-ttu-id="086e5-122">Bu cmdlet 'in yol filtresi oluşturduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="086e5-122">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="086e5-123">-Kural</span><span class="sxs-lookup"><span data-stu-id="086e5-123">-Rule</span></span>
<span data-ttu-id="086e5-124">Yol filtresi ile ilişkilendirilecek bir yol filtre kuralı nesneleri dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="086e5-124">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="086e5-125">Etiketli</span><span class="sxs-lookup"><span data-stu-id="086e5-125">-Tag</span></span>
<span data-ttu-id="086e5-126">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="086e5-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="086e5-127">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="086e5-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="086e5-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="086e5-128">-Confirm</span></span>
<span data-ttu-id="086e5-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="086e5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="086e5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="086e5-130">-WhatIf</span></span>
<span data-ttu-id="086e5-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="086e5-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="086e5-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="086e5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="086e5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="086e5-133">CommonParameters</span></span>
<span data-ttu-id="086e5-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="086e5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="086e5-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="086e5-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="086e5-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="086e5-136">INPUTS</span></span>

### <span data-ttu-id="086e5-137">System. String</span><span class="sxs-lookup"><span data-stu-id="086e5-137">System.String</span></span>

### <span data-ttu-id="086e5-138">Microsoft. Azure. Commands. Network. model. PSRouteFilterRule []</span><span class="sxs-lookup"><span data-stu-id="086e5-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule[]</span></span>

### <span data-ttu-id="086e5-139">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="086e5-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="086e5-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="086e5-140">OUTPUTS</span></span>

### <span data-ttu-id="086e5-141">Microsoft. Azure. Commands. Network. modeller. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="086e5-141">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="086e5-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="086e5-142">NOTES</span></span>
<span data-ttu-id="086e5-143">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="086e5-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="086e5-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="086e5-144">RELATED LINKS</span></span>

[<span data-ttu-id="086e5-145">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="086e5-145">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="086e5-146">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="086e5-146">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="086e5-147">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="086e5-147">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="086e5-148">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="086e5-148">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="086e5-149">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="086e5-149">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="086e5-150">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="086e5-150">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="086e5-151">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="086e5-151">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="086e5-152">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="086e5-152">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
