---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D342
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagercustomheaderfromendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromEndpoint.md
ms.openlocfilehash: 35ab92add873e603101400f77e813fb115386fd4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098531"
---
# <span data-ttu-id="ce381-101">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="ce381-101">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span></span>

## <span data-ttu-id="ce381-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce381-102">SYNOPSIS</span></span>
<span data-ttu-id="ce381-103">Yerel bir Traffic Manager uç nokta nesnesinden özel üst bilgi bilgilerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ce381-103">Removes custom header information from a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="ce381-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ce381-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerCustomHeaderFromEndpoint -Name <String> -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce381-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ce381-105">DESCRIPTION</span></span>
<span data-ttu-id="ce381-106">**Remove-AzTrafficManagerCustomHeaderFromEndpoint** cmdlet 'i yerel bir Azure Traffic Manager uç nokta nesnesinden özel üst bilgi bilgilerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ce381-106">The **Remove-AzTrafficManagerCustomHeaderFromEndpoint** cmdlet removes custom header information from a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="ce381-107">New-AzTrafficManagerEndpoint veya Get-AzTrafficManagerEndpoint cmdlet 'lerini kullanarak uç nokta alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ce381-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="ce381-108">Bu cmdlet yerel son nokta nesnesinde çalışır.</span><span class="sxs-lookup"><span data-stu-id="ce381-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="ce381-109">Set-AzTrafficManagerEndpoint cmdlet 'ini kullanarak, akış Yöneticisi uç noktasına değişikliklerinizi kaydedin.</span><span class="sxs-lookup"><span data-stu-id="ce381-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="ce381-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ce381-110">EXAMPLES</span></span>

### <span data-ttu-id="ce381-111">Örnek 1: uç noktadan özel alt ağ bilgilerini kaldırma</span><span class="sxs-lookup"><span data-stu-id="ce381-111">Example 1: Remove custom subnet information from an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzTrafficManagerCustomHeaderFromEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="ce381-112">İlk komut ResourceGroup11 adındaki kaynak grubundaki ContosoProfile adlı profilden contoso adlı Azure uç noktasını alır ve bu nesneyi $TrafficManagerEndpoint değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ce381-112">The first command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="ce381-113">İkinci komut $TrafficManagerEndpoint uygulamasında depolanan bitiş noktasından özel başlık bilgilerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ce381-113">The second command removes custom header information from the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="ce381-114">Son komutu, Traffic Manager 'daki yerel değeri $TrafficManagerEndpoint eşleşecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ce381-114">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="ce381-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ce381-115">PARAMETERS</span></span>

### <span data-ttu-id="ce381-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce381-116">-DefaultProfile</span></span>
<span data-ttu-id="ce381-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ce381-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce381-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="ce381-118">-Name</span></span>
<span data-ttu-id="ce381-119">Kaldırılacak özel üstbilgi bilgilerinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ce381-119">Specifies the name of the custom header information to be removed.</span></span>

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

### <span data-ttu-id="ce381-120">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ce381-120">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="ce381-121">Yerel bir **TrafficManagerEndpoint** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="ce381-121">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="ce381-122">Bu cmdlet bu yerel nesneyi değiştirir.</span><span class="sxs-lookup"><span data-stu-id="ce381-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="ce381-123">**TrafficManagerEndpoint** nesnesi almak için Get-AzTrafficManagerEndpoint veya New-AzTrafficManagerEndpoint cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ce381-123">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="ce381-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="ce381-124">-Confirm</span></span>
<span data-ttu-id="ce381-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ce381-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce381-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce381-126">-WhatIf</span></span>
<span data-ttu-id="ce381-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ce381-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ce381-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ce381-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce381-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce381-129">CommonParameters</span></span>
<span data-ttu-id="ce381-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ce381-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce381-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce381-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce381-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ce381-132">INPUTS</span></span>

### <span data-ttu-id="ce381-133">Microsoft. Azure. Commands. TrafficManager. modeller. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ce381-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="ce381-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ce381-134">OUTPUTS</span></span>

### <span data-ttu-id="ce381-135">Microsoft. Azure. Commands. TrafficManager. modeller. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ce381-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="ce381-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ce381-136">NOTES</span></span>

## <span data-ttu-id="ce381-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ce381-137">RELATED LINKS</span></span>

[<span data-ttu-id="ce381-138">Add-AzTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="ce381-138">Add-AzTrafficManagerCustomHeaderToEndpoint</span></span>](./Add-AzTrafficManagerCustomHeaderToEndpoint.md)

[<span data-ttu-id="ce381-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ce381-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="ce381-140">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ce381-140">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="ce381-141">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ce381-141">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
