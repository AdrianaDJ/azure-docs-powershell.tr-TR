---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 4556C345-55D0-431C-B980-219D5ED14E5F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 50ad29e9c28b42b1459d66358b8c6c37e2e0f4ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591752"
---
# <span data-ttu-id="b6fcc-101">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b6fcc-101">Get-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="b6fcc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6fcc-102">SYNOPSIS</span></span>
<span data-ttu-id="b6fcc-103">Traffic Manager profili için uç noktası alır.</span><span class="sxs-lookup"><span data-stu-id="b6fcc-103">Gets an endpoint for a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6fcc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b6fcc-104">SYNTAX</span></span>

### <span data-ttu-id="b6fcc-105">Alanlardır</span><span class="sxs-lookup"><span data-stu-id="b6fcc-105">Fields</span></span>
```
Get-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6fcc-106">Nesnelerini</span><span class="sxs-lookup"><span data-stu-id="b6fcc-106">Object</span></span>
```
Get-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6fcc-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b6fcc-107">DESCRIPTION</span></span>
<span data-ttu-id="b6fcc-108">**Get-AzureRmTrafficManagerEndpoint** cmdlet 'ı bir Azure Traffic Manager profili için uç nokta alır.</span><span class="sxs-lookup"><span data-stu-id="b6fcc-108">The **Get-AzureRmTrafficManagerEndpoint** cmdlet gets an endpoint for an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="b6fcc-109">Bu nesneyi yerel olarak değiştirebilir ve Set-AzureRmTrafficManagerEndpoint cmdlet 'ini kullanarak değişiklikleri profile uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b6fcc-109">You can modify this object locally, and then apply changes to the profile by using the Set-AzureRmTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="b6fcc-110">*Ad* ve *tür* parametrelerini kullanarak uç noktayı belirtin.</span><span class="sxs-lookup"><span data-stu-id="b6fcc-110">Specify the endpoint by using the *Name* and *Type* parameters.</span></span>
<span data-ttu-id="b6fcc-111">*ProfilAdı* ve *resourcegroupname* parametresini kullanarak veya bir **TrafficManagerProfile** nesnesi belirterek Traffic Manager profilini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b6fcc-111">You can specify the Traffic Manager profile either by using the *ProfileName* and *ResourceGroupName* parameter, or by specifying a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="b6fcc-112">Alternatif olarak, bu değeri ardışık düzeni kullanarak geçirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b6fcc-112">Alternatively, you can pass that value by using the pipeline.</span></span>

## <span data-ttu-id="b6fcc-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b6fcc-113">EXAMPLES</span></span>

### <span data-ttu-id="b6fcc-114">Örnek 1: uç nokta alma</span><span class="sxs-lookup"><span data-stu-id="b6fcc-114">Example 1: Get an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="b6fcc-115">Bu komut, ResourceGroup11 adlı kaynak grubundaki ContosoProfile adlı profilden contoso adlı Azure uç noktasını alır ve bu nesneyi $TrafficManagerEndpoint değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b6fcc-115">This command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>

## <span data-ttu-id="b6fcc-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b6fcc-116">PARAMETERS</span></span>

### <span data-ttu-id="b6fcc-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="b6fcc-117">-Name</span></span>
<span data-ttu-id="b6fcc-118">Bu cmdlet 'in aldığı Traffic Manager uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b6fcc-118">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b6fcc-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="b6fcc-119">-ProfileName</span></span>
<span data-ttu-id="b6fcc-120">Bu cmdlet 'in aldığı Traffic Manager uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b6fcc-120">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b6fcc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6fcc-121">-ResourceGroupName</span></span>
<span data-ttu-id="b6fcc-122">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b6fcc-122">Specifies the name of a resource group.</span></span>
<span data-ttu-id="b6fcc-123">Bu cmdlet, bu parametrenin belirttiği grupta bir Traffic Manager uç noktası alır.</span><span class="sxs-lookup"><span data-stu-id="b6fcc-123">This cmdlet gets a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b6fcc-124">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b6fcc-124">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="b6fcc-125">Bu cmdlet 'in aldığı Traffic Manager uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b6fcc-125">Specifies the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b6fcc-126">-Tür</span><span class="sxs-lookup"><span data-stu-id="b6fcc-126">-Type</span></span>
<span data-ttu-id="b6fcc-127">Bu cmdlet 'in Traffic Manager profiline eklediği uç nokta türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="b6fcc-127">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="b6fcc-128">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="b6fcc-128">Valid values are:</span></span> 

- <span data-ttu-id="b6fcc-129">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="b6fcc-129">AzureEndpoints</span></span>
- <span data-ttu-id="b6fcc-130">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="b6fcc-130">ExternalEndpoints</span></span>
- <span data-ttu-id="b6fcc-131">Nestedenvseçpuanlar</span><span class="sxs-lookup"><span data-stu-id="b6fcc-131">NestedEndpoints</span></span>

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

### <span data-ttu-id="b6fcc-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6fcc-132">-DefaultProfile</span></span>
<span data-ttu-id="b6fcc-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b6fcc-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6fcc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6fcc-134">CommonParameters</span></span>
<span data-ttu-id="b6fcc-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b6fcc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6fcc-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6fcc-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6fcc-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b6fcc-137">INPUTS</span></span>

### <span data-ttu-id="b6fcc-138">TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b6fcc-138">TrafficManagerEndpoint</span></span>
<span data-ttu-id="b6fcc-139">' TrafficManagerEndpoint ' parametresi ardışık düzen için ' TrafficManagerEndpoint ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="b6fcc-139">Parameter 'TrafficManagerEndpoint' accepts value of type 'TrafficManagerEndpoint' from the pipeline</span></span>

## <span data-ttu-id="b6fcc-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b6fcc-140">OUTPUTS</span></span>

### <span data-ttu-id="b6fcc-141">Microsoft. Azure. Commands. TrafficManager. modeller. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b6fcc-141">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="b6fcc-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b6fcc-142">NOTES</span></span>

## <span data-ttu-id="b6fcc-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b6fcc-143">RELATED LINKS</span></span>

[<span data-ttu-id="b6fcc-144">Disable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b6fcc-144">Disable-AzureRmTrafficManagerEndpoint</span></span>](./Disable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="b6fcc-145">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b6fcc-145">Enable-AzureRmTrafficManagerEndpoint</span></span>](./Enable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="b6fcc-146">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b6fcc-146">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="b6fcc-147">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b6fcc-147">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="b6fcc-148">Set-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b6fcc-148">Set-AzureRmTrafficManagerEndpoint</span></span>](./Set-AzureRmTrafficManagerEndpoint.md)


