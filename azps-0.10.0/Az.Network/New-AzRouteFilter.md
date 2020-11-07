---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzRouteFilter.md
ms.openlocfilehash: 0b02c1bfbeee6fa3a628ea6ffacd04c15e96a440
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935363"
---
# <span data-ttu-id="c0aaa-101">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c0aaa-101">New-AzRouteFilter</span></span>

## <span data-ttu-id="c0aaa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0aaa-102">SYNOPSIS</span></span>
<span data-ttu-id="c0aaa-103">Yol filtresi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c0aaa-103">Creates a route filter.</span></span>

## <span data-ttu-id="c0aaa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c0aaa-104">SYNTAX</span></span>

```
New-AzRouteFilter -Name <String> -ResourceGroupName <String> -Location <String>
 [-Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c0aaa-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c0aaa-105">DESCRIPTION</span></span>
<span data-ttu-id="c0aaa-106">New-AzRouteFilter cmdlet 'i Azure yol filtresi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c0aaa-106">The New-AzRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="c0aaa-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c0aaa-107">EXAMPLES</span></span>

### <span data-ttu-id="c0aaa-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c0aaa-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

 
<span data-ttu-id="c0aaa-109">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="c0aaa-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="c0aaa-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c0aaa-110">PARAMETERS</span></span>

### <span data-ttu-id="c0aaa-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="c0aaa-111">-AsJob</span></span>
<span data-ttu-id="c0aaa-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="c0aaa-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0aaa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0aaa-113">-DefaultProfile</span></span>
<span data-ttu-id="c0aaa-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c0aaa-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0aaa-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c0aaa-115">-Force</span></span>
<span data-ttu-id="c0aaa-116">Aynı ada sahip bir yol filtresi de olsa, bu cmdlet 'in yol tablosu oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="c0aaa-116">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0aaa-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="c0aaa-117">-Location</span></span>
<span data-ttu-id="c0aaa-118">Bu cmdlet 'in yol filtresi oluşturduğu Azure bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c0aaa-118">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0aaa-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="c0aaa-119">-Name</span></span>
<span data-ttu-id="c0aaa-120">Yol filtresi için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="c0aaa-120">Specifies a name for the route filter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0aaa-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0aaa-121">-ResourceGroupName</span></span>
<span data-ttu-id="c0aaa-122">Bu cmdlet 'in yol filtresi oluşturduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c0aaa-122">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0aaa-123">-Kural</span><span class="sxs-lookup"><span data-stu-id="c0aaa-123">-Rule</span></span>
<span data-ttu-id="c0aaa-124">Yol filtresi ile ilişkilendirilecek bir yol filtre kuralı nesneleri dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="c0aaa-124">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0aaa-125">Etiketli</span><span class="sxs-lookup"><span data-stu-id="c0aaa-125">-Tag</span></span>
<span data-ttu-id="c0aaa-126">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="c0aaa-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c0aaa-127">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="c0aaa-127">For example:</span></span>

<span data-ttu-id="c0aaa-128">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="c0aaa-128">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0aaa-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="c0aaa-129">-Confirm</span></span>
<span data-ttu-id="c0aaa-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c0aaa-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0aaa-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0aaa-131">-WhatIf</span></span>
<span data-ttu-id="c0aaa-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c0aaa-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c0aaa-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c0aaa-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0aaa-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0aaa-134">CommonParameters</span></span>
<span data-ttu-id="c0aaa-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c0aaa-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0aaa-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0aaa-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0aaa-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c0aaa-137">INPUTS</span></span>

## <span data-ttu-id="c0aaa-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c0aaa-138">OUTPUTS</span></span>

### <span data-ttu-id="c0aaa-139">Microsoft. Azure. Commands. Network. modeller. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c0aaa-139">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="c0aaa-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c0aaa-140">NOTES</span></span>
<span data-ttu-id="c0aaa-141">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="c0aaa-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="c0aaa-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c0aaa-142">RELATED LINKS</span></span>

[<span data-ttu-id="c0aaa-143">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c0aaa-143">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="c0aaa-144">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c0aaa-144">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="c0aaa-145">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c0aaa-145">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="c0aaa-146">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c0aaa-146">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
