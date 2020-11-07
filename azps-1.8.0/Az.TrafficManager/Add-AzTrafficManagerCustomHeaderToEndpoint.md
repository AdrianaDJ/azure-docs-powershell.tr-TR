---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33E
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagercustomheadertoendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToEndpoint.md
ms.openlocfilehash: 7e3661a827bb6864fbd43abde43c7ab2bb440ecb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753901"
---
# <span data-ttu-id="7bc13-101">Add-AzTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="7bc13-101">Add-AzTrafficManagerCustomHeaderToEndpoint</span></span>

## <span data-ttu-id="7bc13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bc13-102">SYNOPSIS</span></span>
<span data-ttu-id="7bc13-103">Yerel bir Traffic Manager uç noktası nesnesine özel üstbilgi bilgileri ekler.</span><span class="sxs-lookup"><span data-stu-id="7bc13-103">Adds custom header information to a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="7bc13-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7bc13-104">SYNTAX</span></span>

```
Add-AzTrafficManagerCustomHeaderToEndpoint -Name <String> -Value <String>
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bc13-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7bc13-105">DESCRIPTION</span></span>
<span data-ttu-id="7bc13-106">**Add-AzTrafficManagerCustomHeaderToEndpoint** cmdlet 'i yerel bir Azure Traffic Manager uç nokta nesnesine özel üstbilgi bilgileri ekler.</span><span class="sxs-lookup"><span data-stu-id="7bc13-106">The **Add-AzTrafficManagerCustomHeaderToEndpoint** cmdlet adds custom header information to a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="7bc13-107">New-AzTrafficManagerEndpoint veya Get-AzTrafficManagerEndpoint cmdlet 'lerini kullanarak uç nokta alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7bc13-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="7bc13-108">Bu cmdlet yerel son nokta nesnesinde çalışır.</span><span class="sxs-lookup"><span data-stu-id="7bc13-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="7bc13-109">Set-AzTrafficManagerEndpoint cmdlet 'ini kullanarak, akış Yöneticisi uç noktasına değişikliklerinizi kaydedin.</span><span class="sxs-lookup"><span data-stu-id="7bc13-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="7bc13-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7bc13-110">EXAMPLES</span></span>

### <span data-ttu-id="7bc13-111">Örnek 1: uç noktaya özel üstbilgi bilgileri ekleme</span><span class="sxs-lookup"><span data-stu-id="7bc13-111">Example 1: Add custom header information to an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzTrafficManagerCustomHeaderToEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="7bc13-112">İlk komut, **New-AzTrafficManagerEndpoint** cmdlet 'ini kullanarak bir Azure Traffic Manager uç noktası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7bc13-112">The first command creates an Azure Traffic Manager endpoint by using the **New-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="7bc13-113">Komut, $TrafficManagerEndpoint değişkeninde Yerel uç noktayı depolar.</span><span class="sxs-lookup"><span data-stu-id="7bc13-113">The command stores the local endpoint in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="7bc13-114">İkinci komut $TrafficManagerEndpoint depolanan bitiş noktasına özel üst bilgi bilgileri ekler.</span><span class="sxs-lookup"><span data-stu-id="7bc13-114">The second command adds custom header information to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="7bc13-115">Son komutu, Traffic Manager 'daki yerel değeri $TrafficManagerEndpoint eşleşecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="7bc13-115">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="7bc13-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7bc13-116">PARAMETERS</span></span>

### <span data-ttu-id="7bc13-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bc13-117">-DefaultProfile</span></span>
<span data-ttu-id="7bc13-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7bc13-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7bc13-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="7bc13-119">-Name</span></span>
<span data-ttu-id="7bc13-120">Eklenecek özel başlık bilgilerinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7bc13-120">Specifies the name of the custom header information to be added.</span></span>

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

### <span data-ttu-id="7bc13-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7bc13-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="7bc13-122">Yerel bir **TrafficManagerEndpoint** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="7bc13-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="7bc13-123">Bu cmdlet bu yerel nesneyi değiştirir.</span><span class="sxs-lookup"><span data-stu-id="7bc13-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="7bc13-124">**TrafficManagerEndpoint** nesnesi almak için Get-AzTrafficManagerEndpoint veya New-AzTrafficManagerEndpoint cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7bc13-124">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="7bc13-125">-Değer</span><span class="sxs-lookup"><span data-stu-id="7bc13-125">-Value</span></span>
<span data-ttu-id="7bc13-126">Eklenecek özel üstbilgi bilgilerinin değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7bc13-126">Specifies the value of the custom header information to be added.</span></span>

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

### <span data-ttu-id="7bc13-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="7bc13-127">-Confirm</span></span>
<span data-ttu-id="7bc13-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7bc13-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bc13-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bc13-129">-WhatIf</span></span>
<span data-ttu-id="7bc13-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7bc13-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7bc13-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7bc13-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bc13-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bc13-132">CommonParameters</span></span>
<span data-ttu-id="7bc13-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7bc13-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bc13-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bc13-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bc13-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7bc13-135">INPUTS</span></span>

### <span data-ttu-id="7bc13-136">Microsoft. Azure. Commands. TrafficManager. modeller. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7bc13-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="7bc13-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7bc13-137">OUTPUTS</span></span>

### <span data-ttu-id="7bc13-138">Microsoft. Azure. Commands. TrafficManager. modeller. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7bc13-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="7bc13-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7bc13-139">NOTES</span></span>

## <span data-ttu-id="7bc13-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7bc13-140">RELATED LINKS</span></span>

[<span data-ttu-id="7bc13-141">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="7bc13-141">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span></span>](./Remove-AzTrafficManagerCustomHeaderFromEndpoint.md)

[<span data-ttu-id="7bc13-142">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7bc13-142">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="7bc13-143">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7bc13-143">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="7bc13-144">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7bc13-144">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)