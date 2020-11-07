---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilter.md
ms.openlocfilehash: 9ba5f47427dc8f542e1475a8431f5d82c63c5974
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764429"
---
# <span data-ttu-id="61aac-101">New-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="61aac-101">New-AzureRmRouteFilter</span></span>

## <span data-ttu-id="61aac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61aac-102">SYNOPSIS</span></span>
<span data-ttu-id="61aac-103">Yol filtresi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="61aac-103">Creates a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61aac-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="61aac-104">SYNTAX</span></span>

```
New-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> -Location <String>
 [-Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="61aac-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="61aac-105">DESCRIPTION</span></span>
<span data-ttu-id="61aac-106">New-AzureRmRouteFilter cmdlet 'i Azure yol filtresi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="61aac-106">The New-AzureRmRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="61aac-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="61aac-107">EXAMPLES</span></span>

### <span data-ttu-id="61aac-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="61aac-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

 
<span data-ttu-id="61aac-109">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="61aac-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="61aac-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="61aac-110">PARAMETERS</span></span>

### <span data-ttu-id="61aac-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="61aac-111">-AsJob</span></span>
<span data-ttu-id="61aac-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="61aac-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="61aac-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61aac-113">-DefaultProfile</span></span>
<span data-ttu-id="61aac-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="61aac-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61aac-115">-Force</span><span class="sxs-lookup"><span data-stu-id="61aac-115">-Force</span></span>
<span data-ttu-id="61aac-116">Aynı ada sahip bir yol filtresi de olsa, bu cmdlet 'in yol tablosu oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="61aac-116">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

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

### <span data-ttu-id="61aac-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="61aac-117">-Location</span></span>
<span data-ttu-id="61aac-118">Bu cmdlet 'in yol filtresi oluşturduğu Azure bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="61aac-118">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="61aac-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="61aac-119">-Name</span></span>
<span data-ttu-id="61aac-120">Yol filtresi için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="61aac-120">Specifies a name for the route filter.</span></span>

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

### <span data-ttu-id="61aac-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61aac-121">-ResourceGroupName</span></span>
<span data-ttu-id="61aac-122">Bu cmdlet 'in yol filtresi oluşturduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61aac-122">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="61aac-123">-Kural</span><span class="sxs-lookup"><span data-stu-id="61aac-123">-Rule</span></span>
<span data-ttu-id="61aac-124">Yol filtresi ile ilişkilendirilecek bir yol filtre kuralı nesneleri dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="61aac-124">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

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

### <span data-ttu-id="61aac-125">Etiketli</span><span class="sxs-lookup"><span data-stu-id="61aac-125">-Tag</span></span>
<span data-ttu-id="61aac-126">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="61aac-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="61aac-127">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="61aac-127">For example:</span></span>

<span data-ttu-id="61aac-128">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="61aac-128">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="61aac-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="61aac-129">-Confirm</span></span>
<span data-ttu-id="61aac-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="61aac-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61aac-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61aac-131">-WhatIf</span></span>
<span data-ttu-id="61aac-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="61aac-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="61aac-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="61aac-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61aac-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61aac-134">CommonParameters</span></span>
<span data-ttu-id="61aac-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="61aac-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61aac-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61aac-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61aac-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="61aac-137">INPUTS</span></span>

### <span data-ttu-id="61aac-138">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="61aac-138">None</span></span>
<span data-ttu-id="61aac-139">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="61aac-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="61aac-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="61aac-140">OUTPUTS</span></span>

### <span data-ttu-id="61aac-141">Microsoft. Azure. Commands. Network. modeller. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="61aac-141">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="61aac-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="61aac-142">NOTES</span></span>
<span data-ttu-id="61aac-143">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="61aac-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="61aac-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="61aac-144">RELATED LINKS</span></span>

[<span data-ttu-id="61aac-145">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="61aac-145">Get-AzureRmRouteFilter</span></span>](./Get-AzureRmRouteFilter.md)

[<span data-ttu-id="61aac-146">Yeni-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="61aac-146">New-AzureRmRouteFilterRuleConfig</span></span>](./New-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="61aac-147">Remove-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="61aac-147">Remove-AzureRmRouteFilter</span></span>](./Remove-AzureRmRouteFilter.md)

[<span data-ttu-id="61aac-148">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="61aac-148">Set-AzureRmRouteFilter</span></span>](./Set-AzureRmRouteFilter.md)
