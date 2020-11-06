---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 32263236-C207-4FE0-AB8A-018118FC7729
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/enable-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 2556715c321ddcc3f8acbc518ddbe6a3048353af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589988"
---
# <span data-ttu-id="21f58-101">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="21f58-101">Enable-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="21f58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21f58-102">SYNOPSIS</span></span>
<span data-ttu-id="21f58-103">Traffic Manager profilinde uç nokta etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="21f58-103">Enables an endpoint in a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21f58-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="21f58-104">SYNTAX</span></span>

### <span data-ttu-id="21f58-105">Alanlardır</span><span class="sxs-lookup"><span data-stu-id="21f58-105">Fields</span></span>
```
Enable-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21f58-106">Nesnelerini</span><span class="sxs-lookup"><span data-stu-id="21f58-106">Object</span></span>
```
Enable-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21f58-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="21f58-107">DESCRIPTION</span></span>
<span data-ttu-id="21f58-108">**Enable-AzureRmTrafficManagerEndpoint** cmdlet 'ı Azure Traffic Manager profilinde uç nokta etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="21f58-108">The **Enable-AzureRmTrafficManagerEndpoint** cmdlet enables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="21f58-109">**TrafficManagerEndpoint** nesnesini bu cmdlet 'e geçirmek için ardışık düzen işlecini kullanabilir veya *TrafficManagerEndpoint* parametresini kullanarak bir **TrafficManagerEndpoint** nesnesi belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="21f58-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="21f58-110">Alternatif olarak, *ProfilAdı* ve *Resourcegroupname* parametreleriyle *ad* ve *tür* parametrelerini kullanarak uç nokta adını ve türünü de belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="21f58-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="21f58-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="21f58-111">EXAMPLES</span></span>

### <span data-ttu-id="21f58-112">Örnek 1: profilden uç noktayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="21f58-112">Example 1: Enable an endpoint from a profile</span></span>
```
PS C:\>Enable-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="21f58-113">Bu komut, kaynak grup ResouceGroup11 ' da ContosoProfile adlı profildeki contoso adlı dış uç noktasını etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="21f58-113">This command enables the external endpoint named contoso in the profile named ContosoProfile in resource group ResouceGroup11.</span></span>

### <span data-ttu-id="21f58-114">Örnek 2: ardışık düzeni kullanarak uç noktayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="21f58-114">Example 2: Enable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzureRmTrafficManagerEndpoint
```

<span data-ttu-id="21f58-115">Bu komut, ResourceGroup11 'daki ContosoProfile adlı profilden contoso adlı dış uç noktayı alır.</span><span class="sxs-lookup"><span data-stu-id="21f58-115">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="21f58-116">Komut daha sonra bu uç noktayı **Enable-AzureRmTrafficManagerEndpoint** cmdlet 'ine ardışık düzen işlecini kullanarak geçirir.</span><span class="sxs-lookup"><span data-stu-id="21f58-116">The command then passes that endpoint to the **Enable-AzureRmTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="21f58-117">Bu cmdlet bu uç noktayı etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="21f58-117">That cmdlet enables that endpoint.</span></span>

## <span data-ttu-id="21f58-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="21f58-118">PARAMETERS</span></span>

### <span data-ttu-id="21f58-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21f58-119">-DefaultProfile</span></span>
<span data-ttu-id="21f58-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="21f58-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21f58-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="21f58-121">-Name</span></span>
<span data-ttu-id="21f58-122">Bu cmdlet 'in etkinleştirmesine sahip Traffic Manager uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="21f58-122">Specifies the name of the Traffic Manager endpoint that this cmdlet enables.</span></span>

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

### <span data-ttu-id="21f58-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="21f58-123">-ProfileName</span></span>
<span data-ttu-id="21f58-124">Bu cmdlet 'in uç noktayı etkinleştirmesine sahip bir Traffic Manager profilinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="21f58-124">Specifies the name of a Traffic Manager profile in which this cmdlet enables an endpoint.</span></span>
<span data-ttu-id="21f58-125">Profil edinmek için Get-AzureRmTrafficManagerProfile cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="21f58-125">To obtain a profile, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="21f58-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21f58-126">-ResourceGroupName</span></span>
<span data-ttu-id="21f58-127">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="21f58-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="21f58-128">Bu cmdlet, bu parametrenin belirttiği grupta bir Traffic Manager uç noktası belirler.</span><span class="sxs-lookup"><span data-stu-id="21f58-128">This cmdlet enables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="21f58-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="21f58-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="21f58-130">Bu cmdlet 'in izin belirttiği Traffic Manager uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="21f58-130">Specifies the Traffic Manager endpoint that this cmdlet enables.</span></span>
<span data-ttu-id="21f58-131">**TrafficManagerEndpoint** nesnesi almak için Get-AzureRmTrafficManagerEndpoint cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="21f58-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="21f58-132">-Tür</span><span class="sxs-lookup"><span data-stu-id="21f58-132">-Type</span></span>
<span data-ttu-id="21f58-133">Bu cmdlet 'in Traffic Manager profilinde devre dışı bırakacağını belirten uç nokta türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="21f58-133">Specifies the type of endpoint that this cmdlet disables in the Traffic Manager profile.</span></span>
<span data-ttu-id="21f58-134">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="21f58-134">Valid values are:</span></span> 

- <span data-ttu-id="21f58-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="21f58-135">AzureEndpoints</span></span>
- <span data-ttu-id="21f58-136">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="21f58-136">ExternalEndpoints</span></span>
- <span data-ttu-id="21f58-137">Nestedenvseçpuanlar</span><span class="sxs-lookup"><span data-stu-id="21f58-137">NestedEndpoints</span></span>

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

### <span data-ttu-id="21f58-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21f58-138">CommonParameters</span></span>
<span data-ttu-id="21f58-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="21f58-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21f58-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21f58-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21f58-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="21f58-141">INPUTS</span></span>

### <span data-ttu-id="21f58-142">TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="21f58-142">TrafficManagerEndpoint</span></span>
<span data-ttu-id="21f58-143">' TrafficManagerEndpoint ' parametresi ardışık düzen için ' TrafficManagerEndpoint ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="21f58-143">Parameter 'TrafficManagerEndpoint' accepts value of type 'TrafficManagerEndpoint' from the pipeline</span></span>

## <span data-ttu-id="21f58-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="21f58-144">OUTPUTS</span></span>

### <span data-ttu-id="21f58-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="21f58-145">System.Boolean</span></span>

## <span data-ttu-id="21f58-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="21f58-146">NOTES</span></span>

## <span data-ttu-id="21f58-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="21f58-147">RELATED LINKS</span></span>

[<span data-ttu-id="21f58-148">Disable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="21f58-148">Disable-AzureRmTrafficManagerEndpoint</span></span>](./Disable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="21f58-149">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="21f58-149">Get-AzureRmTrafficManagerEndpoint</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="21f58-150">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="21f58-150">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="21f58-151">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="21f58-151">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="21f58-152">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="21f58-152">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="21f58-153">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="21f58-153">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="21f58-154">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="21f58-154">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


