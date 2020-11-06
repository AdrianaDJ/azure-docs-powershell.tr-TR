---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D345
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerIpAddressRange.md
ms.openlocfilehash: 5bb661dbc5a65b9a245fcfa35cdc194bbcded1eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587101"
---
# <span data-ttu-id="e4f73-101">Remove-AzureRmTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="e4f73-101">Remove-AzureRmTrafficManagerIpAddressRange</span></span>

## <span data-ttu-id="e4f73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4f73-102">SYNOPSIS</span></span>
<span data-ttu-id="e4f73-103">Yerel trafik Yöneticisi uç noktası nesnesinden bir adres aralığını veya alt ağı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e4f73-103">Removes an address range or subnet from a local Traffic Manager endpoint object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4f73-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e4f73-104">SYNTAX</span></span>

```
Remove-AzureRmTrafficManagerIpAddressRange -First <String> -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4f73-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e4f73-105">DESCRIPTION</span></span>
<span data-ttu-id="e4f73-106">**Remove-AzureRmTrafficManagerIpAddressRange** cmdlet 'i yerel bir Azure Traffic Manager uç nokta nesnesinden IP adresi aralığını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e4f73-106">The **Remove-AzureRmTrafficManagerIpAddressRange** cmdlet removes an IP address range from a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="e4f73-107">New-AzureRmTrafficManagerEndpoint veya Get-AzureRmTrafficManagerEndpoint cmdlet 'lerini kullanarak uç nokta alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e4f73-107">You can get an endpoint by using the New-AzureRmTrafficManagerEndpoint or Get-AzureRmTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="e4f73-108">Bu cmdlet yerel son nokta nesnesinde çalışır.</span><span class="sxs-lookup"><span data-stu-id="e4f73-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="e4f73-109">Set-AzureRmTrafficManagerEndpoint cmdlet 'ini kullanarak, akış Yöneticisi uç noktasına değişikliklerinizi kaydedin.</span><span class="sxs-lookup"><span data-stu-id="e4f73-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="e4f73-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e4f73-110">EXAMPLES</span></span>

### <span data-ttu-id="e4f73-111">Örnek 1: uç noktadan IP adresi aralıklarını kaldırma</span><span class="sxs-lookup"><span data-stu-id="e4f73-111">Example 1: Remove IP address ranges from an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4"
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="e4f73-112">İlk komut ResourceGroup11 adındaki kaynak grubundaki ContosoProfile adlı profilden contoso adlı Azure uç noktasını alır ve bu nesneyi $TrafficManagerEndpoint değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="e4f73-112">The first command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="e4f73-113">İkinci komut, $TrafficManagerEndpoint depolanan uç noktasından IP adresi aralığını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e4f73-113">The second command removes an IP address range from the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="e4f73-114">Son komutu, Traffic Manager 'daki yerel değeri $TrafficManagerEndpoint eşleşecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e4f73-114">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="e4f73-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e4f73-115">PARAMETERS</span></span>

### <span data-ttu-id="e4f73-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4f73-116">-DefaultProfile</span></span>
<span data-ttu-id="e4f73-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e4f73-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4f73-118">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e4f73-118">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="e4f73-119">Yerel bir **TrafficManagerEndpoint** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="e4f73-119">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="e4f73-120">Bu cmdlet bu yerel nesneyi değiştirir.</span><span class="sxs-lookup"><span data-stu-id="e4f73-120">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="e4f73-121">**TrafficManagerEndpoint** nesnesi almak için Get-AzureRmTrafficManagerEndpoint veya New-AzureRmTrafficManagerEndpoint cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e4f73-121">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint or New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4f73-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="e4f73-122">-Confirm</span></span>
<span data-ttu-id="e4f73-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e4f73-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4f73-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4f73-124">-WhatIf</span></span>
<span data-ttu-id="e4f73-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e4f73-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e4f73-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e4f73-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4f73-127">-Önce</span><span class="sxs-lookup"><span data-stu-id="e4f73-127">-First</span></span>
<span data-ttu-id="e4f73-128">Kaldırılacak aralıktaki ilk IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e4f73-128">Specifies the first IP address in the range to be removed.</span></span>

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

### <span data-ttu-id="e4f73-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4f73-129">CommonParameters</span></span>
<span data-ttu-id="e4f73-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e4f73-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4f73-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4f73-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4f73-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e4f73-132">INPUTS</span></span>

### <span data-ttu-id="e4f73-133">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e4f73-133">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="e4f73-134">Bu cmdlet, bu cmdlet 'e bir **TrafficManagerEndpoint** nesnesi kabul eder.</span><span class="sxs-lookup"><span data-stu-id="e4f73-134">This cmdlet accepts a **TrafficManagerEndpoint** object to this cmdlet.</span></span>

## <span data-ttu-id="e4f73-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e4f73-135">OUTPUTS</span></span>

### <span data-ttu-id="e4f73-136">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e4f73-136">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="e4f73-137">Bu cmdlet değiştirilmiş bir TrafficManagerEndpoint nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="e4f73-137">This cmdlet returns a modified TrafficManagerEndpoint object.</span></span>

## <span data-ttu-id="e4f73-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e4f73-138">NOTES</span></span>

## <span data-ttu-id="e4f73-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e4f73-139">RELATED LINKS</span></span>

[<span data-ttu-id="e4f73-140">Add-AzureRmTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="e4f73-140">Add-AzureRmTrafficManagerIpAddressRange</span></span>](./Add-AzureRmTrafficManagerIpAddressRange.md)

[<span data-ttu-id="e4f73-141">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e4f73-141">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="e4f73-142">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e4f73-142">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="e4f73-143">Set-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e4f73-143">Set-AzureRmTrafficManagerEndpoint</span></span>](./Set-AzureRmTrafficManagerEndpoint.md)
