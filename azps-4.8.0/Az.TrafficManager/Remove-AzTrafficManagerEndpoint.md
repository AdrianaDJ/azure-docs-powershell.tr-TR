---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 2129C457-592B-484C-A148-828BFD5895D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 6f2884a6d4cefaf52b06ec653db85c9e9ae59f54
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267947"
---
# <span data-ttu-id="abc08-101">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="abc08-101">Remove-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="abc08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="abc08-102">SYNOPSIS</span></span>
<span data-ttu-id="abc08-103">Traffic Manager 'dan uç noktayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="abc08-103">Removes an endpoint from Traffic Manager.</span></span>

## <span data-ttu-id="abc08-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="abc08-104">SYNTAX</span></span>

### <span data-ttu-id="abc08-105">Alanlardır</span><span class="sxs-lookup"><span data-stu-id="abc08-105">Fields</span></span>
```
Remove-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abc08-106">Nesnelerini</span><span class="sxs-lookup"><span data-stu-id="abc08-106">Object</span></span>
```
Remove-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abc08-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="abc08-107">DESCRIPTION</span></span>
<span data-ttu-id="abc08-108">**Remove-AzTrafficManagerEndpoint** cmdlet 'ı Azure Traffic Manager 'dan bir uç noktayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="abc08-108">The **Remove-AzTrafficManagerEndpoint** cmdlet removes an endpoint from Azure Traffic Manager.</span></span>

<span data-ttu-id="abc08-109">Bu cmdlet, Traffic Manager hizmetine yapılan her değişikliği kaydeder.</span><span class="sxs-lookup"><span data-stu-id="abc08-109">This cmdlet commits each change to the Traffic Manager service.</span></span>
<span data-ttu-id="abc08-110">Yerel bir Traffic Manager profil nesnesinden birden fazla uç nokta kaldırmak ve değişiklikleri tek bir işlemde uygulamak için Remove-AzTrafficManagerEndpointConfig cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="abc08-110">To remove multiple endpoints from a local Traffic Manager profile object and commit changes in a single operation, use the Remove-AzTrafficManagerEndpointConfig cmdlet.</span></span>

<span data-ttu-id="abc08-111">**TrafficManagerEndpoint** nesnesini bu cmdlet 'e geçirmek için ardışık düzen işlecini kullanabilir veya *TrafficManagerEndpoint* parametresini kullanarak bir **TrafficManagerEndpoint** nesnesi belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="abc08-111">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="abc08-112">Alternatif olarak, *ProfilAdı* ve *Resourcegroupname* parametreleriyle *ad* ve *tür* parametrelerini kullanarak uç nokta adını ve türünü de belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="abc08-112">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="abc08-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="abc08-113">EXAMPLES</span></span>

### <span data-ttu-id="abc08-114">Örnek 1: profilden uç noktayı kaldırma</span><span class="sxs-lookup"><span data-stu-id="abc08-114">Example 1: Remove an endpoint from a profile</span></span>
```
PS C:\>Remove-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="abc08-115">Bu komut, contoso adlı Azure uç noktasını, ResourceGroup11 adlı kaynak grubundaki ContosoProfile adlı profilden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="abc08-115">This command removes the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="abc08-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="abc08-116">PARAMETERS</span></span>

### <span data-ttu-id="abc08-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abc08-117">-DefaultProfile</span></span>
<span data-ttu-id="abc08-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="abc08-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abc08-119">-Force</span><span class="sxs-lookup"><span data-stu-id="abc08-119">-Force</span></span>
<span data-ttu-id="abc08-120">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="abc08-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="abc08-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="abc08-121">-Name</span></span>
<span data-ttu-id="abc08-122">Bu cmdlet 'in kaldırdığı Traffic Manager uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="abc08-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="abc08-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="abc08-123">-ProfileName</span></span>
<span data-ttu-id="abc08-124">Bu cmdlet 'in uç noktayı kaldırdığı bir Traffic Manager profilinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="abc08-124">Specifies the name of a Traffic Manager profile from which this cmdlet removes an endpoint.</span></span>
<span data-ttu-id="abc08-125">Profil edinmek için Get-AzTrafficManagerProfile cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="abc08-125">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="abc08-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abc08-126">-ResourceGroupName</span></span>
<span data-ttu-id="abc08-127">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="abc08-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="abc08-128">Bu cmdlet, bu parametrenin belirttiği gruptaki bir Traffic Manager profilindeki Traffic Manager uç noktasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="abc08-128">This cmdlet removes a Traffic Manager endpoint from a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="abc08-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="abc08-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="abc08-130">Bu cmdlet 'in kaldırdığı Traffic Manager uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="abc08-130">Specifies the Traffic Manager endpoint that this cmdlet removes.</span></span>
<span data-ttu-id="abc08-131">**TrafficManagerEndpoint** nesnesi almak için Get-AzTrafficManagerEndpoint cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="abc08-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="abc08-132">-Tür</span><span class="sxs-lookup"><span data-stu-id="abc08-132">-Type</span></span>
<span data-ttu-id="abc08-133">Bu cmdlet 'in Traffic Manager profiline eklediği uç nokta türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="abc08-133">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="abc08-134">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="abc08-134">Valid values are:</span></span> 

- <span data-ttu-id="abc08-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="abc08-135">AzureEndpoints</span></span>
- <span data-ttu-id="abc08-136">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="abc08-136">ExternalEndpoints</span></span>
- <span data-ttu-id="abc08-137">Nestedenvseçpuanlar</span><span class="sxs-lookup"><span data-stu-id="abc08-137">NestedEndpoints</span></span>

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

### <span data-ttu-id="abc08-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="abc08-138">-Confirm</span></span>
<span data-ttu-id="abc08-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="abc08-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abc08-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abc08-140">-WhatIf</span></span>
<span data-ttu-id="abc08-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="abc08-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abc08-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="abc08-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abc08-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abc08-143">CommonParameters</span></span>
<span data-ttu-id="abc08-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="abc08-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abc08-145">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abc08-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abc08-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="abc08-146">INPUTS</span></span>

### <span data-ttu-id="abc08-147">Microsoft. Azure. Commands. TrafficManager. modeller. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="abc08-147">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="abc08-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="abc08-148">OUTPUTS</span></span>

### <span data-ttu-id="abc08-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="abc08-149">System.Boolean</span></span>

## <span data-ttu-id="abc08-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="abc08-150">NOTES</span></span>

## <span data-ttu-id="abc08-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="abc08-151">RELATED LINKS</span></span>

[<span data-ttu-id="abc08-152">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="abc08-152">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="abc08-153">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="abc08-153">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="abc08-154">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="abc08-154">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="abc08-155">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="abc08-155">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="abc08-156">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="abc08-156">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


