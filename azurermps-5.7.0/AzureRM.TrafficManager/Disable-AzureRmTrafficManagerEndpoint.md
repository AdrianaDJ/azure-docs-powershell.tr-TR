---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 8CC749F1-B961-4F8F-BAD4-2C0F4385D1C2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/disable-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 13b798da7b35a4721b35d2375cf4e25bb47fbb98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763204"
---
# <span data-ttu-id="de094-101">Disable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="de094-101">Disable-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="de094-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de094-102">SYNOPSIS</span></span>
<span data-ttu-id="de094-103">Traffic Manager profilindeki uç noktayı devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="de094-103">Disables an endpoint in a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de094-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="de094-104">SYNTAX</span></span>

### <span data-ttu-id="de094-105">Alanlardır</span><span class="sxs-lookup"><span data-stu-id="de094-105">Fields</span></span>
```
Disable-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="de094-106">Nesnelerini</span><span class="sxs-lookup"><span data-stu-id="de094-106">Object</span></span>
```
Disable-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de094-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="de094-107">DESCRIPTION</span></span>
<span data-ttu-id="de094-108">**Disable-AzureRmTrafficManagerEndpoint** cmdlet 'ı bir Azure Traffic Manager profilindeki uç noktayı devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="de094-108">The **Disable-AzureRmTrafficManagerEndpoint** cmdlet disables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="de094-109">**TrafficManagerEndpoint** nesnesini bu cmdlet 'e geçirmek için ardışık düzen işlecini kullanabilir ya da *TrafficManagerEndpoint* parametresini kullanarak **TrafficManagerEndpoint** nesnesini geçirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="de094-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can pass a **TrafficManagerEndpoint** object using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="de094-110">Alternatif olarak, *ProfilAdı* ve *Resourcegroupname* parametreleriyle *ad* ve *tür* parametrelerini kullanarak uç nokta adını ve türünü de belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="de094-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="de094-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="de094-111">EXAMPLES</span></span>

### <span data-ttu-id="de094-112">Örnek 1: uç noktayı adıyla devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="de094-112">Example 1: Disable an endpoint by name</span></span>
```
PS C:\> Disable-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="de094-113">Bu komut, kaynak grubu ResouceGroup11 ContosoProfile adlı profildeki contoso adlı dış uç noktasını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="de094-113">This command disables the external endpoint named contoso in the profile named ContosoProfile in resource group ResouceGroup11.</span></span>
<span data-ttu-id="de094-114">Komut sizden onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="de094-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="de094-115">Örnek 2: ardışık düzeni kullanarak uç noktayı devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="de094-115">Example 2: Disable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzureRmTrafficManagerEndpoint -Force
```

<span data-ttu-id="de094-116">Bu komut, ResourceGroup11 'daki ContosoProfile adlı profilden contoso adlı dış uç noktayı alır.</span><span class="sxs-lookup"><span data-stu-id="de094-116">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="de094-117">Komut daha sonra bu uç noktayı, ardışık düzen işlecini kullanarak **Disable-AzureRmTrafficManagerEndpoint** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="de094-117">The command then passes that endpoint to the **Disable-AzureRmTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="de094-118">Bu cmdlet uç noktayı devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="de094-118">That cmdlet disables that endpoint.</span></span>
<span data-ttu-id="de094-119">Komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="de094-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="de094-120">Bu nedenle sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="de094-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="de094-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="de094-121">PARAMETERS</span></span>

### <span data-ttu-id="de094-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de094-122">-DefaultProfile</span></span>
<span data-ttu-id="de094-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="de094-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de094-124">-Force</span><span class="sxs-lookup"><span data-stu-id="de094-124">-Force</span></span>
<span data-ttu-id="de094-125">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="de094-125">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de094-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="de094-126">-Name</span></span>
<span data-ttu-id="de094-127">Bu cmdlet 'in devre dışı olduğu Traffic Manager uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="de094-127">Specifies the name of the Traffic Manager endpoint that this cmdlet disables.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de094-128">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="de094-128">-ProfileName</span></span>
<span data-ttu-id="de094-129">Bu cmdlet 'in uç noktayı devre dışı bırakabildiği bir Traffic Manager profilinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="de094-129">Specifies the name of a Traffic Manager profile in which this cmdlet disables an endpoint.</span></span>
<span data-ttu-id="de094-130">Profil edinmek için Get-AzureRmTrafficManagerProfile cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="de094-130">To obtain a profile, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de094-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de094-131">-ResourceGroupName</span></span>
<span data-ttu-id="de094-132">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="de094-132">Specifies the name of a resource group.</span></span>
<span data-ttu-id="de094-133">Bu cmdlet, bu parametrenin belirttiği gruptaki bir Traffic Manager uç noktasını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="de094-133">This cmdlet disables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de094-134">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="de094-134">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="de094-135">Bu cmdlet 'in devre dışı olduğu Traffic Manager uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="de094-135">Specifies the Traffic Manager endpoint that this cmdlet disables.</span></span>
<span data-ttu-id="de094-136">**TrafficManagerEndpoint** nesnesi almak için Get-AzureRmTrafficManagerEndpoint cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="de094-136">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

```yaml
Type: TrafficManagerEndpoint
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de094-137">-Tür</span><span class="sxs-lookup"><span data-stu-id="de094-137">-Type</span></span>
<span data-ttu-id="de094-138">Bu cmdlet 'in Traffic Manager profiline eklediği uç nokta türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="de094-138">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="de094-139">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="de094-139">Valid values are:</span></span> 

- <span data-ttu-id="de094-140">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="de094-140">AzureEndpoints</span></span>
- <span data-ttu-id="de094-141">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="de094-141">ExternalEndpoints</span></span>
- <span data-ttu-id="de094-142">Nestedenvseçpuanlar</span><span class="sxs-lookup"><span data-stu-id="de094-142">NestedEndpoints</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de094-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="de094-143">-Confirm</span></span>
<span data-ttu-id="de094-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="de094-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de094-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de094-145">-WhatIf</span></span>
<span data-ttu-id="de094-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="de094-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de094-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="de094-147">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de094-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de094-148">CommonParameters</span></span>
<span data-ttu-id="de094-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="de094-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de094-150">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de094-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de094-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="de094-151">INPUTS</span></span>

### <span data-ttu-id="de094-152">TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="de094-152">TrafficManagerEndpoint</span></span>
<span data-ttu-id="de094-153">' TrafficManagerEndpoint ' parametresi ardışık düzen için ' TrafficManagerEndpoint ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="de094-153">Parameter 'TrafficManagerEndpoint' accepts value of type 'TrafficManagerEndpoint' from the pipeline</span></span>

## <span data-ttu-id="de094-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="de094-154">OUTPUTS</span></span>

### <span data-ttu-id="de094-155">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="de094-155">System.Boolean</span></span>

## <span data-ttu-id="de094-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="de094-156">NOTES</span></span>

## <span data-ttu-id="de094-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="de094-157">RELATED LINKS</span></span>

[<span data-ttu-id="de094-158">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="de094-158">Enable-AzureRmTrafficManagerEndpoint</span></span>](./Enable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="de094-159">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="de094-159">Get-AzureRmTrafficManagerEndpoint</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="de094-160">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="de094-160">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="de094-161">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="de094-161">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="de094-162">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="de094-162">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="de094-163">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="de094-163">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="de094-164">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="de094-164">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)

