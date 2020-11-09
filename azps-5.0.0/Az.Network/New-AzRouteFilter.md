---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilter.md
ms.openlocfilehash: 8be04cd9e483e990d73130866779710bbed879bb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323737"
---
# <span data-ttu-id="b1a82-101">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b1a82-101">New-AzRouteFilter</span></span>

## <span data-ttu-id="b1a82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1a82-102">SYNOPSIS</span></span>
<span data-ttu-id="b1a82-103">Yol filtresi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b1a82-103">Creates a route filter.</span></span>

## <span data-ttu-id="b1a82-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b1a82-104">SYNTAX</span></span>

```
New-AzRouteFilter -Name <String> -ResourceGroupName <String> -Location <String> [-Rule <PSRouteFilterRule[]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b1a82-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b1a82-105">DESCRIPTION</span></span>
<span data-ttu-id="b1a82-106">New-AzRouteFilter cmdlet 'i Azure yol filtresi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b1a82-106">The New-AzRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="b1a82-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b1a82-107">EXAMPLES</span></span>

### <span data-ttu-id="b1a82-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b1a82-108">Example 1</span></span>
```powershell
PS C:\> New-AzRouteFilter -Name "MyRouteFilter" -ResourceGroupName "MyResourceGroup" -Location "West US"
```

<span data-ttu-id="b1a82-109">Komut yeni bir yol filtresi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b1a82-109">The command creates a new route filter.</span></span>

## <span data-ttu-id="b1a82-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b1a82-110">PARAMETERS</span></span>

### <span data-ttu-id="b1a82-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="b1a82-111">-AsJob</span></span>
<span data-ttu-id="b1a82-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="b1a82-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b1a82-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1a82-113">-DefaultProfile</span></span>
<span data-ttu-id="b1a82-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b1a82-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1a82-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b1a82-115">-Force</span></span>
<span data-ttu-id="b1a82-116">Aynı ada sahip bir yol filtresi de olsa, bu cmdlet 'in yol tablosu oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="b1a82-116">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

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

### <span data-ttu-id="b1a82-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="b1a82-117">-Location</span></span>
<span data-ttu-id="b1a82-118">Bu cmdlet 'in yol filtresi oluşturduğu Azure bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1a82-118">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="b1a82-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="b1a82-119">-Name</span></span>
<span data-ttu-id="b1a82-120">Yol filtresi için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1a82-120">Specifies a name for the route filter.</span></span>

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

### <span data-ttu-id="b1a82-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1a82-121">-ResourceGroupName</span></span>
<span data-ttu-id="b1a82-122">Bu cmdlet 'in yol filtresi oluşturduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1a82-122">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="b1a82-123">-Kural</span><span class="sxs-lookup"><span data-stu-id="b1a82-123">-Rule</span></span>
<span data-ttu-id="b1a82-124">Yol filtresi ile ilişkilendirilecek bir yol filtre kuralı nesneleri dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1a82-124">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

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

### <span data-ttu-id="b1a82-125">Etiketli</span><span class="sxs-lookup"><span data-stu-id="b1a82-125">-Tag</span></span>
<span data-ttu-id="b1a82-126">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="b1a82-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b1a82-127">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="b1a82-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b1a82-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="b1a82-128">-Confirm</span></span>
<span data-ttu-id="b1a82-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b1a82-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1a82-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1a82-130">-WhatIf</span></span>
<span data-ttu-id="b1a82-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b1a82-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b1a82-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b1a82-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1a82-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1a82-133">CommonParameters</span></span>
<span data-ttu-id="b1a82-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b1a82-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1a82-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1a82-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1a82-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b1a82-136">INPUTS</span></span>

### <span data-ttu-id="b1a82-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b1a82-137">System.String</span></span>

### <span data-ttu-id="b1a82-138">Microsoft. Azure. Commands. Network. model. PSRouteFilterRule []</span><span class="sxs-lookup"><span data-stu-id="b1a82-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule[]</span></span>

### <span data-ttu-id="b1a82-139">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b1a82-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b1a82-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b1a82-140">OUTPUTS</span></span>

### <span data-ttu-id="b1a82-141">Microsoft. Azure. Commands. Network. modeller. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b1a82-141">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="b1a82-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b1a82-142">NOTES</span></span>
<span data-ttu-id="b1a82-143">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="b1a82-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="b1a82-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b1a82-144">RELATED LINKS</span></span>

[<span data-ttu-id="b1a82-145">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b1a82-145">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="b1a82-146">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b1a82-146">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="b1a82-147">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b1a82-147">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="b1a82-148">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b1a82-148">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="b1a82-149">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b1a82-149">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="b1a82-150">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b1a82-150">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="b1a82-151">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b1a82-151">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="b1a82-152">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b1a82-152">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
