---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D341
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerIpAddressRange.md
ms.openlocfilehash: 184b949fa91c7c9993895c8150e21f56244f6e17
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753895"
---
# <span data-ttu-id="97cd5-101">Add-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="97cd5-101">Add-AzTrafficManagerIpAddressRange</span></span>

## <span data-ttu-id="97cd5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97cd5-102">SYNOPSIS</span></span>
<span data-ttu-id="97cd5-103">Yerel bir Traffic Manager uç noktası nesnesine adres aralığı veya alt ağ ekler.</span><span class="sxs-lookup"><span data-stu-id="97cd5-103">Adds an address range or subnet to a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="97cd5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="97cd5-104">SYNTAX</span></span>

```
Add-AzTrafficManagerIpAddressRange -First <String> [-Last <String>] [-Scope <Int32>]
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97cd5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="97cd5-105">DESCRIPTION</span></span>
<span data-ttu-id="97cd5-106">**Add-AzTrafficManagerIpAddressRange** cmdlet 'i yerel bir Azure Traffic Manager uç nokta nesnesine IP adresi aralığı ekler.</span><span class="sxs-lookup"><span data-stu-id="97cd5-106">The **Add-AzTrafficManagerIpAddressRange** cmdlet adds an IP address range to a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="97cd5-107">New-AzTrafficManagerEndpoint veya Get-AzTrafficManagerEndpoint cmdlet 'lerini kullanarak uç nokta alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="97cd5-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="97cd5-108">Bu cmdlet yerel son nokta nesnesinde çalışır.</span><span class="sxs-lookup"><span data-stu-id="97cd5-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="97cd5-109">Set-AzTrafficManagerEndpoint cmdlet 'ini kullanarak, akış Yöneticisi uç noktasına değişikliklerinizi kaydedin.</span><span class="sxs-lookup"><span data-stu-id="97cd5-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="97cd5-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="97cd5-110">EXAMPLES</span></span>

### <span data-ttu-id="97cd5-111">Örnek 1: uç noktaya IP adresi aralıkları ekleme</span><span class="sxs-lookup"><span data-stu-id="97cd5-111">Example 1: Add IP address ranges to an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4" -Last "5.6.7.8"
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "9.10.11.0" -Scope 24
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "12.13.14.0" -Last "12.13.14.31" -Scope 27
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "15.16.17.18"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="97cd5-112">İlk komut, **New-AzTrafficManagerEndpoint** cmdlet 'ini kullanarak bir Azure Traffic Manager uç noktası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="97cd5-112">The first command creates an Azure Traffic Manager endpoint by using the **New-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="97cd5-113">Komut, $TrafficManagerEndpoint değişkeninde Yerel uç noktayı depolar.</span><span class="sxs-lookup"><span data-stu-id="97cd5-113">The command stores the local endpoint in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="97cd5-114">İkinci komut $TrafficManagerEndpoint depolanan bitiş noktasına 5.6.7.8 'e 1.2.3.4 IP adresi aralığını ekler.</span><span class="sxs-lookup"><span data-stu-id="97cd5-114">The second command adds the IP address range 1.2.3.4 to 5.6.7.8 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="97cd5-115">Üçüncü komut, $TrafficManagerEndpoint depolanan bitiş noktasına 9.10.11.255 için 9.10.11.0 IP adresi aralığını ekler.</span><span class="sxs-lookup"><span data-stu-id="97cd5-115">The third command adds the IP address range 9.10.11.0 to 9.10.11.255 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="97cd5-116">Dördüncü komut, kapsamın aralığın boyutuyla eşleştiğini doğrular, ardından $TrafficManagerEndpoint depolanan bitiş noktasına 12.13.14.31 için 12.13.14.0 IP adresi aralığını ekler.</span><span class="sxs-lookup"><span data-stu-id="97cd5-116">The fourth command verifies that the scope matches the size of the range, then adds the IP address range 12.13.14.0 to 12.13.14.31 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="97cd5-117">Beşinci komut, $TrafficManagerEndpoint depolanan bitiş noktasına 15.16.17.18 için 15.16.17.18 IP adresi aralığını ekler.</span><span class="sxs-lookup"><span data-stu-id="97cd5-117">The fifth command adds the IP address range 15.16.17.18 to 15.16.17.18 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="97cd5-118">Son komutu, Traffic Manager 'daki yerel değeri $TrafficManagerEndpoint eşleşecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="97cd5-118">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="97cd5-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="97cd5-119">PARAMETERS</span></span>

### <span data-ttu-id="97cd5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97cd5-120">-DefaultProfile</span></span>
<span data-ttu-id="97cd5-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="97cd5-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97cd5-122">-Son</span><span class="sxs-lookup"><span data-stu-id="97cd5-122">-Last</span></span>
<span data-ttu-id="97cd5-123">Eklenecek aralıktaki son IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="97cd5-123">Specifies the last IP address in the range to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97cd5-124">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="97cd5-124">-Scope</span></span>
<span data-ttu-id="97cd5-125">Eklenecek IP adresi aralığının kapsamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="97cd5-125">Specifies the scope of the IP address range to be added.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97cd5-126">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="97cd5-126">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="97cd5-127">Yerel bir **TrafficManagerEndpoint** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="97cd5-127">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="97cd5-128">Bu cmdlet bu yerel nesneyi değiştirir.</span><span class="sxs-lookup"><span data-stu-id="97cd5-128">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="97cd5-129">**TrafficManagerEndpoint** nesnesi almak için Get-AzTrafficManagerEndpoint veya New-AzTrafficManagerEndpoint cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="97cd5-129">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="97cd5-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="97cd5-130">-Confirm</span></span>
<span data-ttu-id="97cd5-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="97cd5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97cd5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97cd5-132">-WhatIf</span></span>
<span data-ttu-id="97cd5-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="97cd5-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="97cd5-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="97cd5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97cd5-135">-Önce</span><span class="sxs-lookup"><span data-stu-id="97cd5-135">-First</span></span>
<span data-ttu-id="97cd5-136">Eklenecek aralıktaki ilk IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="97cd5-136">Specifies the first IP address in the range to be added.</span></span>

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

### <span data-ttu-id="97cd5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97cd5-137">CommonParameters</span></span>
<span data-ttu-id="97cd5-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="97cd5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97cd5-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97cd5-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97cd5-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="97cd5-140">INPUTS</span></span>

### <span data-ttu-id="97cd5-141">Microsoft. Azure. Commands. TrafficManager. modeller. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="97cd5-141">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="97cd5-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="97cd5-142">OUTPUTS</span></span>

### <span data-ttu-id="97cd5-143">Microsoft. Azure. Commands. TrafficManager. modeller. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="97cd5-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="97cd5-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="97cd5-144">NOTES</span></span>

## <span data-ttu-id="97cd5-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="97cd5-145">RELATED LINKS</span></span>

[<span data-ttu-id="97cd5-146">Remove-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="97cd5-146">Remove-AzTrafficManagerIpAddressRange</span></span>](./Remove-AzTrafficManagerIpAddressRange.md)

[<span data-ttu-id="97cd5-147">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="97cd5-147">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="97cd5-148">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="97cd5-148">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="97cd5-149">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="97cd5-149">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
