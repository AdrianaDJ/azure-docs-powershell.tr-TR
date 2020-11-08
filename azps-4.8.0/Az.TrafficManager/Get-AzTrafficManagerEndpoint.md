---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 4556C345-55D0-431C-B980-219D5ED14E5F
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/get-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 3a24063e7b3d74704aa8d409b5bec6d87e35d095
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109319"
---
# <span data-ttu-id="a7a23-101">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a7a23-101">Get-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="a7a23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7a23-102">SYNOPSIS</span></span>
<span data-ttu-id="a7a23-103">Traffic Manager profili için uç noktası alır.</span><span class="sxs-lookup"><span data-stu-id="a7a23-103">Gets an endpoint for a Traffic Manager profile.</span></span>

## <span data-ttu-id="a7a23-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a7a23-104">SYNTAX</span></span>

### <span data-ttu-id="a7a23-105">Alanlardır</span><span class="sxs-lookup"><span data-stu-id="a7a23-105">Fields</span></span>
```
Get-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7a23-106">Nesnelerini</span><span class="sxs-lookup"><span data-stu-id="a7a23-106">Object</span></span>
```
Get-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7a23-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a7a23-107">DESCRIPTION</span></span>
<span data-ttu-id="a7a23-108">**Get-AzTrafficManagerEndpoint** cmdlet 'ı bir Azure Traffic Manager profili için uç nokta alır.</span><span class="sxs-lookup"><span data-stu-id="a7a23-108">The **Get-AzTrafficManagerEndpoint** cmdlet gets an endpoint for an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="a7a23-109">Bu nesneyi yerel olarak değiştirebilir ve Set-AzTrafficManagerEndpoint cmdlet 'ini kullanarak değişiklikleri profile uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a7a23-109">You can modify this object locally, and then apply changes to the profile by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="a7a23-110">*Ad* ve *tür* parametrelerini kullanarak uç noktayı belirtin.</span><span class="sxs-lookup"><span data-stu-id="a7a23-110">Specify the endpoint by using the *Name* and *Type* parameters.</span></span>
<span data-ttu-id="a7a23-111">*ProfilAdı* ve *resourcegroupname* parametresini kullanarak veya bir **TrafficManagerProfile** nesnesi belirterek Traffic Manager profilini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a7a23-111">You can specify the Traffic Manager profile either by using the *ProfileName* and *ResourceGroupName* parameter, or by specifying a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="a7a23-112">Alternatif olarak, bu değeri ardışık düzeni kullanarak geçirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a7a23-112">Alternatively, you can pass that value by using the pipeline.</span></span>

## <span data-ttu-id="a7a23-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a7a23-113">EXAMPLES</span></span>

### <span data-ttu-id="a7a23-114">Örnek 1: uç nokta alma</span><span class="sxs-lookup"><span data-stu-id="a7a23-114">Example 1: Get an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="a7a23-115">Bu komut, ResourceGroup11 adlı kaynak grubundaki ContosoProfile adlı profilden contoso adlı Azure uç noktasını alır ve bu nesneyi $TrafficManagerEndpoint değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a7a23-115">This command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>

## <span data-ttu-id="a7a23-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a7a23-116">PARAMETERS</span></span>

### <span data-ttu-id="a7a23-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7a23-117">-DefaultProfile</span></span>
<span data-ttu-id="a7a23-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a7a23-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7a23-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="a7a23-119">-Name</span></span>
<span data-ttu-id="a7a23-120">Bu cmdlet 'in aldığı Traffic Manager uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a7a23-120">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a7a23-121">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="a7a23-121">-ProfileName</span></span>
<span data-ttu-id="a7a23-122">Bu cmdlet 'in aldığı Traffic Manager uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a7a23-122">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a7a23-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7a23-123">-ResourceGroupName</span></span>
<span data-ttu-id="a7a23-124">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a7a23-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="a7a23-125">Bu cmdlet, bu parametrenin belirttiği grupta bir Traffic Manager uç noktası alır.</span><span class="sxs-lookup"><span data-stu-id="a7a23-125">This cmdlet gets a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a7a23-126">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a7a23-126">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="a7a23-127">Bu cmdlet 'in aldığı Traffic Manager uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a7a23-127">Specifies the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a7a23-128">-Tür</span><span class="sxs-lookup"><span data-stu-id="a7a23-128">-Type</span></span>
<span data-ttu-id="a7a23-129">Bu cmdlet 'in Traffic Manager profiline eklediği uç nokta türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="a7a23-129">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="a7a23-130">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="a7a23-130">Valid values are:</span></span> 

- <span data-ttu-id="a7a23-131">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="a7a23-131">AzureEndpoints</span></span>
- <span data-ttu-id="a7a23-132">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="a7a23-132">ExternalEndpoints</span></span>
- <span data-ttu-id="a7a23-133">Nestedenvseçpuanlar</span><span class="sxs-lookup"><span data-stu-id="a7a23-133">NestedEndpoints</span></span>

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

### <span data-ttu-id="a7a23-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7a23-134">CommonParameters</span></span>
<span data-ttu-id="a7a23-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a7a23-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7a23-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7a23-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7a23-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a7a23-137">INPUTS</span></span>

### <span data-ttu-id="a7a23-138">Microsoft. Azure. Commands. TrafficManager. modeller. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a7a23-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="a7a23-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a7a23-139">OUTPUTS</span></span>

### <span data-ttu-id="a7a23-140">Microsoft. Azure. Commands. TrafficManager. modeller. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a7a23-140">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="a7a23-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a7a23-141">NOTES</span></span>

## <span data-ttu-id="a7a23-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a7a23-142">RELATED LINKS</span></span>

[<span data-ttu-id="a7a23-143">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a7a23-143">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="a7a23-144">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a7a23-144">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="a7a23-145">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a7a23-145">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="a7a23-146">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a7a23-146">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="a7a23-147">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a7a23-147">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)


