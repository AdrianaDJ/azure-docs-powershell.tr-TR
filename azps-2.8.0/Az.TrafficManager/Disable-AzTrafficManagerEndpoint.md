---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8CC749F1-B961-4F8F-BAD4-2C0F4385D1C2
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/disable-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerEndpoint.md
ms.openlocfilehash: ed3468e6064aa28595ddbcb5f4c296976dd5fbb9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934359"
---
# <span data-ttu-id="fb42a-101">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fb42a-101">Disable-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="fb42a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb42a-102">SYNOPSIS</span></span>
<span data-ttu-id="fb42a-103">Traffic Manager profilindeki uç noktayı devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="fb42a-103">Disables an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="fb42a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fb42a-104">SYNTAX</span></span>

### <span data-ttu-id="fb42a-105">Alanlardır</span><span class="sxs-lookup"><span data-stu-id="fb42a-105">Fields</span></span>
```
Disable-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fb42a-106">Nesnelerini</span><span class="sxs-lookup"><span data-stu-id="fb42a-106">Object</span></span>
```
Disable-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb42a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="fb42a-107">DESCRIPTION</span></span>
<span data-ttu-id="fb42a-108">**Disable-AzTrafficManagerEndpoint** cmdlet 'ı bir Azure Traffic Manager profilindeki uç noktayı devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="fb42a-108">The **Disable-AzTrafficManagerEndpoint** cmdlet disables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="fb42a-109">**TrafficManagerEndpoint** nesnesini bu cmdlet 'e geçirmek için ardışık düzen işlecini kullanabilir ya da *TrafficManagerEndpoint* parametresini kullanarak **TrafficManagerEndpoint** nesnesini geçirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fb42a-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can pass a **TrafficManagerEndpoint** object using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="fb42a-110">Alternatif olarak, *ProfilAdı* ve *Resourcegroupname* parametreleriyle *ad* ve *tür* parametrelerini kullanarak uç nokta adını ve türünü de belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fb42a-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="fb42a-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fb42a-111">EXAMPLES</span></span>

### <span data-ttu-id="fb42a-112">Örnek 1: uç noktayı adıyla devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="fb42a-112">Example 1: Disable an endpoint by name</span></span>
```
PS C:\> Disable-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="fb42a-113">Bu komut, kaynak grubu ResourceGroup11 ContosoProfile adlı profildeki contoso adlı dış uç noktasını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="fb42a-113">This command disables the external endpoint named contoso in the profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="fb42a-114">Komut sizden onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fb42a-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="fb42a-115">Örnek 2: ardışık düzeni kullanarak uç noktayı devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="fb42a-115">Example 2: Disable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzTrafficManagerEndpoint -Force
```

<span data-ttu-id="fb42a-116">Bu komut, ResourceGroup11 'daki ContosoProfile adlı profilden contoso adlı dış uç noktayı alır.</span><span class="sxs-lookup"><span data-stu-id="fb42a-116">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="fb42a-117">Komut daha sonra bu uç noktayı, ardışık düzen işlecini kullanarak **Disable-AzTrafficManagerEndpoint** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="fb42a-117">The command then passes that endpoint to the **Disable-AzTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="fb42a-118">Bu cmdlet uç noktayı devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="fb42a-118">That cmdlet disables that endpoint.</span></span>
<span data-ttu-id="fb42a-119">Komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fb42a-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="fb42a-120">Bu nedenle sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="fb42a-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="fb42a-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fb42a-121">PARAMETERS</span></span>

### <span data-ttu-id="fb42a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb42a-122">-DefaultProfile</span></span>
<span data-ttu-id="fb42a-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fb42a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb42a-124">-Force</span><span class="sxs-lookup"><span data-stu-id="fb42a-124">-Force</span></span>
<span data-ttu-id="fb42a-125">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="fb42a-125">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb42a-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="fb42a-126">-Name</span></span>
<span data-ttu-id="fb42a-127">Bu cmdlet 'in devre dışı olduğu Traffic Manager uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fb42a-127">Specifies the name of the Traffic Manager endpoint that this cmdlet disables.</span></span>

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

### <span data-ttu-id="fb42a-128">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="fb42a-128">-ProfileName</span></span>
<span data-ttu-id="fb42a-129">Bu cmdlet 'in uç noktayı devre dışı bırakabildiği bir Traffic Manager profilinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fb42a-129">Specifies the name of a Traffic Manager profile in which this cmdlet disables an endpoint.</span></span>
<span data-ttu-id="fb42a-130">Profil edinmek için Get-AzTrafficManagerProfile cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="fb42a-130">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="fb42a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb42a-131">-ResourceGroupName</span></span>
<span data-ttu-id="fb42a-132">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fb42a-132">Specifies the name of a resource group.</span></span>
<span data-ttu-id="fb42a-133">Bu cmdlet, bu parametrenin belirttiği gruptaki bir Traffic Manager uç noktasını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="fb42a-133">This cmdlet disables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="fb42a-134">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fb42a-134">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="fb42a-135">Bu cmdlet 'in devre dışı olduğu Traffic Manager uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fb42a-135">Specifies the Traffic Manager endpoint that this cmdlet disables.</span></span>
<span data-ttu-id="fb42a-136">**TrafficManagerEndpoint** nesnesi almak için Get-AzTrafficManagerEndpoint cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="fb42a-136">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="fb42a-137">-Tür</span><span class="sxs-lookup"><span data-stu-id="fb42a-137">-Type</span></span>
<span data-ttu-id="fb42a-138">Bu cmdlet 'in Traffic Manager profiline eklediği uç nokta türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="fb42a-138">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="fb42a-139">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="fb42a-139">Valid values are:</span></span> 

- <span data-ttu-id="fb42a-140">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="fb42a-140">AzureEndpoints</span></span>
- <span data-ttu-id="fb42a-141">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="fb42a-141">ExternalEndpoints</span></span>
- <span data-ttu-id="fb42a-142">Nestedenvseçpuanlar</span><span class="sxs-lookup"><span data-stu-id="fb42a-142">NestedEndpoints</span></span>

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

### <span data-ttu-id="fb42a-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="fb42a-143">-Confirm</span></span>
<span data-ttu-id="fb42a-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fb42a-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb42a-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb42a-145">-WhatIf</span></span>
<span data-ttu-id="fb42a-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fb42a-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb42a-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fb42a-147">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb42a-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb42a-148">CommonParameters</span></span>
<span data-ttu-id="fb42a-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fb42a-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb42a-150">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb42a-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb42a-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fb42a-151">INPUTS</span></span>

### <span data-ttu-id="fb42a-152">Microsoft. Azure. Commands. TrafficManager. modeller. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fb42a-152">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="fb42a-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fb42a-153">OUTPUTS</span></span>

### <span data-ttu-id="fb42a-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fb42a-154">System.Boolean</span></span>

## <span data-ttu-id="fb42a-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fb42a-155">NOTES</span></span>

## <span data-ttu-id="fb42a-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fb42a-156">RELATED LINKS</span></span>

[<span data-ttu-id="fb42a-157">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fb42a-157">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="fb42a-158">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fb42a-158">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="fb42a-159">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fb42a-159">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="fb42a-160">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fb42a-160">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="fb42a-161">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fb42a-161">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="fb42a-162">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fb42a-162">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="fb42a-163">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fb42a-163">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


