---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 32263236-C207-4FE0-AB8A-018118FC7729
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/enable-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 5d7ef8e2fd778b5bcaaea1413bddd85eceb0582c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109320"
---
# <span data-ttu-id="9c79b-101">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9c79b-101">Enable-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="9c79b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c79b-102">SYNOPSIS</span></span>
<span data-ttu-id="9c79b-103">Traffic Manager profilinde uç nokta etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="9c79b-103">Enables an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="9c79b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9c79b-104">SYNTAX</span></span>

### <span data-ttu-id="9c79b-105">Alanlardır</span><span class="sxs-lookup"><span data-stu-id="9c79b-105">Fields</span></span>
```
Enable-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c79b-106">Nesnelerini</span><span class="sxs-lookup"><span data-stu-id="9c79b-106">Object</span></span>
```
Enable-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c79b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="9c79b-107">DESCRIPTION</span></span>
<span data-ttu-id="9c79b-108">**Enable-AzTrafficManagerEndpoint** cmdlet 'ı Azure Traffic Manager profilinde uç nokta etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="9c79b-108">The **Enable-AzTrafficManagerEndpoint** cmdlet enables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="9c79b-109">**TrafficManagerEndpoint** nesnesini bu cmdlet 'e geçirmek için ardışık düzen işlecini kullanabilir veya *TrafficManagerEndpoint* parametresini kullanarak bir **TrafficManagerEndpoint** nesnesi belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9c79b-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="9c79b-110">Alternatif olarak, *ProfilAdı* ve *Resourcegroupname* parametreleriyle *ad* ve *tür* parametrelerini kullanarak uç nokta adını ve türünü de belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9c79b-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="9c79b-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9c79b-111">EXAMPLES</span></span>

### <span data-ttu-id="9c79b-112">Örnek 1: profilden uç noktayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="9c79b-112">Example 1: Enable an endpoint from a profile</span></span>
```
PS C:\>Enable-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="9c79b-113">Bu komut, kaynak grup ResourceGroup11 ' da ContosoProfile adlı profildeki contoso adlı dış uç noktasını etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="9c79b-113">This command enables the external endpoint named contoso in the profile named ContosoProfile in resource group ResourceGroup11.</span></span>

### <span data-ttu-id="9c79b-114">Örnek 2: ardışık düzeni kullanarak uç noktayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="9c79b-114">Example 2: Enable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzTrafficManagerEndpoint
```

<span data-ttu-id="9c79b-115">Bu komut, ResourceGroup11 'daki ContosoProfile adlı profilden contoso adlı dış uç noktayı alır.</span><span class="sxs-lookup"><span data-stu-id="9c79b-115">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="9c79b-116">Komut daha sonra bu uç noktayı **Enable-AzTrafficManagerEndpoint** cmdlet 'ine ardışık düzen işlecini kullanarak geçirir.</span><span class="sxs-lookup"><span data-stu-id="9c79b-116">The command then passes that endpoint to the **Enable-AzTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9c79b-117">Bu cmdlet bu uç noktayı etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="9c79b-117">That cmdlet enables that endpoint.</span></span>

## <span data-ttu-id="9c79b-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9c79b-118">PARAMETERS</span></span>

### <span data-ttu-id="9c79b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c79b-119">-DefaultProfile</span></span>
<span data-ttu-id="9c79b-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9c79b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c79b-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="9c79b-121">-Name</span></span>
<span data-ttu-id="9c79b-122">Bu cmdlet 'in etkinleştirmesine sahip Traffic Manager uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c79b-122">Specifies the name of the Traffic Manager endpoint that this cmdlet enables.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c79b-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="9c79b-123">-ProfileName</span></span>
<span data-ttu-id="9c79b-124">Bu cmdlet 'in uç noktayı etkinleştirmesine sahip bir Traffic Manager profilinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c79b-124">Specifies the name of a Traffic Manager profile in which this cmdlet enables an endpoint.</span></span>
<span data-ttu-id="9c79b-125">Profil edinmek için Get-AzTrafficManagerProfile cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="9c79b-125">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c79b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c79b-126">-ResourceGroupName</span></span>
<span data-ttu-id="9c79b-127">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c79b-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="9c79b-128">Bu cmdlet, bu parametrenin belirttiği grupta bir Traffic Manager uç noktası belirler.</span><span class="sxs-lookup"><span data-stu-id="9c79b-128">This cmdlet enables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c79b-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9c79b-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="9c79b-130">Bu cmdlet 'in izin belirttiği Traffic Manager uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c79b-130">Specifies the Traffic Manager endpoint that this cmdlet enables.</span></span>
<span data-ttu-id="9c79b-131">**TrafficManagerEndpoint** nesnesi almak için Get-AzTrafficManagerEndpoint cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="9c79b-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c79b-132">-Tür</span><span class="sxs-lookup"><span data-stu-id="9c79b-132">-Type</span></span>
<span data-ttu-id="9c79b-133">Bu cmdlet 'in Traffic Manager profilinde devre dışı bırakacağını belirten uç nokta türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c79b-133">Specifies the type of endpoint that this cmdlet disables in the Traffic Manager profile.</span></span>
<span data-ttu-id="9c79b-134">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="9c79b-134">Valid values are:</span></span> 

- <span data-ttu-id="9c79b-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="9c79b-135">AzureEndpoints</span></span>
- <span data-ttu-id="9c79b-136">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="9c79b-136">ExternalEndpoints</span></span>
- <span data-ttu-id="9c79b-137">Nestedenvseçpuanlar</span><span class="sxs-lookup"><span data-stu-id="9c79b-137">NestedEndpoints</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c79b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c79b-138">CommonParameters</span></span>
<span data-ttu-id="9c79b-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9c79b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c79b-140">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c79b-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c79b-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9c79b-141">INPUTS</span></span>

### <span data-ttu-id="9c79b-142">Microsoft. Azure. Commands. TrafficManager. modeller. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9c79b-142">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="9c79b-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9c79b-143">OUTPUTS</span></span>

### <span data-ttu-id="9c79b-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9c79b-144">System.Boolean</span></span>

## <span data-ttu-id="9c79b-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9c79b-145">NOTES</span></span>

## <span data-ttu-id="9c79b-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9c79b-146">RELATED LINKS</span></span>

[<span data-ttu-id="9c79b-147">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9c79b-147">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="9c79b-148">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9c79b-148">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="9c79b-149">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9c79b-149">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="9c79b-150">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9c79b-150">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="9c79b-151">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9c79b-151">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="9c79b-152">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9c79b-152">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="9c79b-153">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9c79b-153">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


