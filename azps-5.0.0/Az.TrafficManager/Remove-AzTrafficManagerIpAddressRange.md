---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D345
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerIpAddressRange.md
ms.openlocfilehash: bfeef76b700eb408da89561464bc5457f94cdd4a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278442"
---
# <span data-ttu-id="9623e-101">Remove-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="9623e-101">Remove-AzTrafficManagerIpAddressRange</span></span>

## <span data-ttu-id="9623e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9623e-102">SYNOPSIS</span></span>
<span data-ttu-id="9623e-103">Yerel trafik Yöneticisi uç noktası nesnesinden bir adres aralığını veya alt ağı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9623e-103">Removes an address range or subnet from a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="9623e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9623e-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerIpAddressRange -First <String> -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9623e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9623e-105">DESCRIPTION</span></span>
<span data-ttu-id="9623e-106">**Remove-AzTrafficManagerIpAddressRange** cmdlet 'i yerel bir Azure Traffic Manager uç nokta nesnesinden IP adresi aralığını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9623e-106">The **Remove-AzTrafficManagerIpAddressRange** cmdlet removes an IP address range from a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="9623e-107">New-AzTrafficManagerEndpoint veya Get-AzTrafficManagerEndpoint cmdlet 'lerini kullanarak uç nokta alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9623e-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="9623e-108">Bu cmdlet yerel son nokta nesnesinde çalışır.</span><span class="sxs-lookup"><span data-stu-id="9623e-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="9623e-109">Set-AzTrafficManagerEndpoint cmdlet 'ini kullanarak, akış Yöneticisi uç noktasına değişikliklerinizi kaydedin.</span><span class="sxs-lookup"><span data-stu-id="9623e-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="9623e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9623e-110">EXAMPLES</span></span>

### <span data-ttu-id="9623e-111">Örnek 1: uç noktadan IP adresi aralıklarını kaldırma</span><span class="sxs-lookup"><span data-stu-id="9623e-111">Example 1: Remove IP address ranges from an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="9623e-112">İlk komut ResourceGroup11 adındaki kaynak grubundaki ContosoProfile adlı profilden contoso adlı Azure uç noktasını alır ve bu nesneyi $TrafficManagerEndpoint değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="9623e-112">The first command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="9623e-113">İkinci komut, $TrafficManagerEndpoint depolanan uç noktasından IP adresi aralığını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9623e-113">The second command removes an IP address range from the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="9623e-114">Son komutu, Traffic Manager 'daki yerel değeri $TrafficManagerEndpoint eşleşecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="9623e-114">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="9623e-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9623e-115">PARAMETERS</span></span>

### <span data-ttu-id="9623e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9623e-116">-DefaultProfile</span></span>
<span data-ttu-id="9623e-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9623e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9623e-118">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9623e-118">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="9623e-119">Yerel bir **TrafficManagerEndpoint** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="9623e-119">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="9623e-120">Bu cmdlet bu yerel nesneyi değiştirir.</span><span class="sxs-lookup"><span data-stu-id="9623e-120">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="9623e-121">**TrafficManagerEndpoint** nesnesi almak için Get-AzTrafficManagerEndpoint veya New-AzTrafficManagerEndpoint cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="9623e-121">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="9623e-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="9623e-122">-Confirm</span></span>
<span data-ttu-id="9623e-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9623e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9623e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9623e-124">-WhatIf</span></span>
<span data-ttu-id="9623e-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9623e-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9623e-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9623e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9623e-127">-Önce</span><span class="sxs-lookup"><span data-stu-id="9623e-127">-First</span></span>
<span data-ttu-id="9623e-128">Kaldırılacak aralıktaki ilk IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9623e-128">Specifies the first IP address in the range to be removed.</span></span>

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

### <span data-ttu-id="9623e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9623e-129">CommonParameters</span></span>
<span data-ttu-id="9623e-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9623e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9623e-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9623e-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9623e-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9623e-132">INPUTS</span></span>

### <span data-ttu-id="9623e-133">Microsoft. Azure. Commands. TrafficManager. modeller. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9623e-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="9623e-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9623e-134">OUTPUTS</span></span>

### <span data-ttu-id="9623e-135">Microsoft. Azure. Commands. TrafficManager. modeller. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9623e-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="9623e-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9623e-136">NOTES</span></span>

## <span data-ttu-id="9623e-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9623e-137">RELATED LINKS</span></span>

[<span data-ttu-id="9623e-138">Add-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="9623e-138">Add-AzTrafficManagerIpAddressRange</span></span>](./Add-AzTrafficManagerIpAddressRange.md)

[<span data-ttu-id="9623e-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9623e-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="9623e-140">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9623e-140">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="9623e-141">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9623e-141">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
