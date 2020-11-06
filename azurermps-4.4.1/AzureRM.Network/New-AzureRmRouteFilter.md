---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilter.md
ms.openlocfilehash: 6cc420ccb2ba2c7e555956d711fe0e30d02ef62f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589253"
---
# <span data-ttu-id="fcc29-101">New-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="fcc29-101">New-AzureRmRouteFilter</span></span>

## <span data-ttu-id="fcc29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcc29-102">SYNOPSIS</span></span>
<span data-ttu-id="fcc29-103">Yol filtresi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fcc29-103">Creates a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fcc29-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fcc29-104">SYNTAX</span></span>

```
New-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> -Location <String>
 [-Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule]>]
 [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fcc29-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fcc29-105">DESCRIPTION</span></span>
<span data-ttu-id="fcc29-106">New-AzureRmRouteFilter cmdlet 'i Azure yol filtresi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fcc29-106">The New-AzureRmRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="fcc29-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fcc29-107">EXAMPLES</span></span>

### <span data-ttu-id="fcc29-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fcc29-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

 
<span data-ttu-id="fcc29-109">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="fcc29-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="fcc29-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fcc29-110">PARAMETERS</span></span>

### <span data-ttu-id="fcc29-111">-Force</span><span class="sxs-lookup"><span data-stu-id="fcc29-111">-Force</span></span>
<span data-ttu-id="fcc29-112">Aynı ada sahip bir yol filtresi de olsa, bu cmdlet 'in yol tablosu oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="fcc29-112">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

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

### <span data-ttu-id="fcc29-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="fcc29-113">-Location</span></span>
<span data-ttu-id="fcc29-114">Bu cmdlet 'in yol filtresi oluşturduğu Azure bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fcc29-114">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="fcc29-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="fcc29-115">-Name</span></span>
<span data-ttu-id="fcc29-116">Yol filtresi için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="fcc29-116">Specifies a name for the route filter.</span></span>

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

### <span data-ttu-id="fcc29-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcc29-117">-ResourceGroupName</span></span>
<span data-ttu-id="fcc29-118">Bu cmdlet 'in yol filtresi oluşturduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fcc29-118">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="fcc29-119">-Kural</span><span class="sxs-lookup"><span data-stu-id="fcc29-119">-Rule</span></span>
<span data-ttu-id="fcc29-120">Yol filtresi ile ilişkilendirilecek bir yol filtre kuralı nesneleri dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="fcc29-120">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

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

### <span data-ttu-id="fcc29-121">Etiketli</span><span class="sxs-lookup"><span data-stu-id="fcc29-121">-Tag</span></span>
<span data-ttu-id="fcc29-122">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="fcc29-122">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="fcc29-123">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="fcc29-123">For example:</span></span>

<span data-ttu-id="fcc29-124">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="fcc29-124">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="fcc29-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="fcc29-125">-Confirm</span></span>
<span data-ttu-id="fcc29-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fcc29-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcc29-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcc29-127">-WhatIf</span></span>
<span data-ttu-id="fcc29-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fcc29-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fcc29-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fcc29-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcc29-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcc29-130">-DefaultProfile</span></span>
<span data-ttu-id="fcc29-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fcc29-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcc29-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcc29-132">CommonParameters</span></span>
<span data-ttu-id="fcc29-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fcc29-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcc29-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcc29-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcc29-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fcc29-135">INPUTS</span></span>

## <span data-ttu-id="fcc29-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fcc29-136">OUTPUTS</span></span>

### <span data-ttu-id="fcc29-137">Microsoft. Azure. Commands. Network. modeller. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="fcc29-137">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="fcc29-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fcc29-138">NOTES</span></span>
<span data-ttu-id="fcc29-139">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="fcc29-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="fcc29-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fcc29-140">RELATED LINKS</span></span>

[<span data-ttu-id="fcc29-141">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="fcc29-141">Get-AzureRmRouteFilter</span></span>](./Get-AzureRmRouteFilter.md)

[<span data-ttu-id="fcc29-142">Yeni-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fcc29-142">New-AzureRmRouteFilterRuleConfig</span></span>](./New-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="fcc29-143">Remove-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="fcc29-143">Remove-AzureRmRouteFilter</span></span>](./Remove-AzureRmRouteFilter.md)

[<span data-ttu-id="fcc29-144">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="fcc29-144">Set-AzureRmRouteFilter</span></span>](./Set-AzureRmRouteFilter.md)
