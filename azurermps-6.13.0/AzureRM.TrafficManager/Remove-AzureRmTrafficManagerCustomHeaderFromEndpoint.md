---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D342
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagercustomheaderfromendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint.md
ms.openlocfilehash: 452e252b7bf9368ea89e81f2d37fd5a80ab079b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587105"
---
# <span data-ttu-id="80c45-101">Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="80c45-101">Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint</span></span>

## <span data-ttu-id="80c45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80c45-102">SYNOPSIS</span></span>
<span data-ttu-id="80c45-103">Yerel bir Traffic Manager uç nokta nesnesinden özel üst bilgi bilgilerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="80c45-103">Removes custom header information from a local Traffic Manager endpoint object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80c45-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="80c45-104">SYNTAX</span></span>

```
Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint -Name <String>
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80c45-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="80c45-105">DESCRIPTION</span></span>
<span data-ttu-id="80c45-106">**Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint** cmdlet 'i yerel bir Azure Traffic Manager uç nokta nesnesinden özel üst bilgi bilgilerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="80c45-106">The **Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint** cmdlet removes custom header information from a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="80c45-107">New-AzureRmTrafficManagerEndpoint veya Get-AzureRmTrafficManagerEndpoint cmdlet 'lerini kullanarak uç nokta alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="80c45-107">You can get an endpoint by using the New-AzureRmTrafficManagerEndpoint or Get-AzureRmTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="80c45-108">Bu cmdlet yerel son nokta nesnesinde çalışır.</span><span class="sxs-lookup"><span data-stu-id="80c45-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="80c45-109">Set-AzureRmTrafficManagerEndpoint cmdlet 'ini kullanarak, akış Yöneticisi uç noktasına değişikliklerinizi kaydedin.</span><span class="sxs-lookup"><span data-stu-id="80c45-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="80c45-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="80c45-110">EXAMPLES</span></span>

### <span data-ttu-id="80c45-111">Örnek 1: uç noktadan özel alt ağ bilgilerini kaldırma</span><span class="sxs-lookup"><span data-stu-id="80c45-111">Example 1: Remove custom subnet information from an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host"
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="80c45-112">İlk komut ResourceGroup11 adındaki kaynak grubundaki ContosoProfile adlı profilden contoso adlı Azure uç noktasını alır ve bu nesneyi $TrafficManagerEndpoint değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="80c45-112">The first command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="80c45-113">İkinci komut $TrafficManagerEndpoint uygulamasında depolanan bitiş noktasından özel başlık bilgilerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="80c45-113">The second command removes custom header information from the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="80c45-114">Son komutu, Traffic Manager 'daki yerel değeri $TrafficManagerEndpoint eşleşecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="80c45-114">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="80c45-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="80c45-115">PARAMETERS</span></span>

### <span data-ttu-id="80c45-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80c45-116">-DefaultProfile</span></span>
<span data-ttu-id="80c45-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="80c45-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80c45-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="80c45-118">-Name</span></span>
<span data-ttu-id="80c45-119">Kaldırılacak özel üstbilgi bilgilerinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="80c45-119">Specifies the name of the custom header information to be removed.</span></span>

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

### <span data-ttu-id="80c45-120">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="80c45-120">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="80c45-121">Yerel bir **TrafficManagerEndpoint** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="80c45-121">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="80c45-122">Bu cmdlet bu yerel nesneyi değiştirir.</span><span class="sxs-lookup"><span data-stu-id="80c45-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="80c45-123">**TrafficManagerEndpoint** nesnesi almak için Get-AzureRmTrafficManagerEndpoint veya New-AzureRmTrafficManagerEndpoint cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="80c45-123">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint or New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="80c45-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="80c45-124">-Confirm</span></span>
<span data-ttu-id="80c45-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="80c45-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80c45-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80c45-126">-WhatIf</span></span>
<span data-ttu-id="80c45-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="80c45-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="80c45-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="80c45-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80c45-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80c45-129">CommonParameters</span></span>
<span data-ttu-id="80c45-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="80c45-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80c45-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80c45-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80c45-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="80c45-132">INPUTS</span></span>

### <span data-ttu-id="80c45-133">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="80c45-133">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="80c45-134">Bu cmdlet, bu cmdlet 'e bir **TrafficManagerEndpoint** nesnesi kabul eder.</span><span class="sxs-lookup"><span data-stu-id="80c45-134">This cmdlet accepts a **TrafficManagerEndpoint** object to this cmdlet.</span></span>

## <span data-ttu-id="80c45-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="80c45-135">OUTPUTS</span></span>

### <span data-ttu-id="80c45-136">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="80c45-136">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="80c45-137">Bu cmdlet değiştirilmiş bir TrafficManagerEndpoint nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="80c45-137">This cmdlet returns a modified TrafficManagerEndpoint object.</span></span>

## <span data-ttu-id="80c45-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="80c45-138">NOTES</span></span>

## <span data-ttu-id="80c45-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="80c45-139">RELATED LINKS</span></span>

[<span data-ttu-id="80c45-140">Add-AzureRmTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="80c45-140">Add-AzureRmTrafficManagerCustomHeaderToEndpoint</span></span>](./Add-AzureRmTrafficManagerCustomHeaderToEndpoint.md)

[<span data-ttu-id="80c45-141">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="80c45-141">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="80c45-142">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="80c45-142">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="80c45-143">Set-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="80c45-143">Set-AzureRmTrafficManagerEndpoint</span></span>](./Set-AzureRmTrafficManagerEndpoint.md)
