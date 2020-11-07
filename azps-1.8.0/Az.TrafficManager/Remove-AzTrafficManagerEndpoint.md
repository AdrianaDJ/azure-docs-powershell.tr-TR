---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 2129C457-592B-484C-A148-828BFD5895D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 60ce16c9c9933d326013ce03b74637b0fce4a3b0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753867"
---
# <span data-ttu-id="e042e-101">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e042e-101">Remove-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="e042e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e042e-102">SYNOPSIS</span></span>
<span data-ttu-id="e042e-103">Traffic Manager 'dan uç noktayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e042e-103">Removes an endpoint from Traffic Manager.</span></span>

## <span data-ttu-id="e042e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e042e-104">SYNTAX</span></span>

### <span data-ttu-id="e042e-105">Alanlardır</span><span class="sxs-lookup"><span data-stu-id="e042e-105">Fields</span></span>
```
Remove-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e042e-106">Nesnelerini</span><span class="sxs-lookup"><span data-stu-id="e042e-106">Object</span></span>
```
Remove-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e042e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e042e-107">DESCRIPTION</span></span>
<span data-ttu-id="e042e-108">**Remove-AzTrafficManagerEndpoint** cmdlet 'ı Azure Traffic Manager 'dan bir uç noktayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e042e-108">The **Remove-AzTrafficManagerEndpoint** cmdlet removes an endpoint from Azure Traffic Manager.</span></span>

<span data-ttu-id="e042e-109">Bu cmdlet, Traffic Manager hizmetine yapılan her değişikliği kaydeder.</span><span class="sxs-lookup"><span data-stu-id="e042e-109">This cmdlet commits each change to the Traffic Manager service.</span></span>
<span data-ttu-id="e042e-110">Yerel bir Traffic Manager profil nesnesinden birden fazla uç nokta kaldırmak ve değişiklikleri tek bir işlemde uygulamak için Remove-AzTrafficManagerEndpointConfig cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e042e-110">To remove multiple endpoints from a local Traffic Manager profile object and commit changes in a single operation, use the Remove-AzTrafficManagerEndpointConfig cmdlet.</span></span>

<span data-ttu-id="e042e-111">**TrafficManagerEndpoint** nesnesini bu cmdlet 'e geçirmek için ardışık düzen işlecini kullanabilir veya *TrafficManagerEndpoint* parametresini kullanarak bir **TrafficManagerEndpoint** nesnesi belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e042e-111">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="e042e-112">Alternatif olarak, *ProfilAdı* ve *Resourcegroupname* parametreleriyle *ad* ve *tür* parametrelerini kullanarak uç nokta adını ve türünü de belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e042e-112">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="e042e-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e042e-113">EXAMPLES</span></span>

### <span data-ttu-id="e042e-114">Örnek 1: profilden uç noktayı kaldırma</span><span class="sxs-lookup"><span data-stu-id="e042e-114">Example 1: Remove an endpoint from a profile</span></span>
```
PS C:\>Remove-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="e042e-115">Bu komut, contoso adlı Azure uç noktasını, ResourceGroup11 adlı kaynak grubundaki ContosoProfile adlı profilden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e042e-115">This command removes the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="e042e-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e042e-116">PARAMETERS</span></span>

### <span data-ttu-id="e042e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e042e-117">-DefaultProfile</span></span>
<span data-ttu-id="e042e-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e042e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e042e-119">-Force</span><span class="sxs-lookup"><span data-stu-id="e042e-119">-Force</span></span>
<span data-ttu-id="e042e-120">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="e042e-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e042e-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="e042e-121">-Name</span></span>
<span data-ttu-id="e042e-122">Bu cmdlet 'in kaldırdığı Traffic Manager uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e042e-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e042e-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="e042e-123">-ProfileName</span></span>
<span data-ttu-id="e042e-124">Bu cmdlet 'in uç noktayı kaldırdığı bir Traffic Manager profilinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e042e-124">Specifies the name of a Traffic Manager profile from which this cmdlet removes an endpoint.</span></span>
<span data-ttu-id="e042e-125">Profil edinmek için Get-AzTrafficManagerProfile cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e042e-125">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="e042e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e042e-126">-ResourceGroupName</span></span>
<span data-ttu-id="e042e-127">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e042e-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="e042e-128">Bu cmdlet, bu parametrenin belirttiği gruptaki bir Traffic Manager profilindeki Traffic Manager uç noktasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e042e-128">This cmdlet removes a Traffic Manager endpoint from a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="e042e-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e042e-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="e042e-130">Bu cmdlet 'in kaldırdığı Traffic Manager uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e042e-130">Specifies the Traffic Manager endpoint that this cmdlet removes.</span></span>
<span data-ttu-id="e042e-131">**TrafficManagerEndpoint** nesnesi almak için Get-AzTrafficManagerEndpoint cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e042e-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="e042e-132">-Tür</span><span class="sxs-lookup"><span data-stu-id="e042e-132">-Type</span></span>
<span data-ttu-id="e042e-133">Bu cmdlet 'in Traffic Manager profiline eklediği uç nokta türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e042e-133">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="e042e-134">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="e042e-134">Valid values are:</span></span> 

- <span data-ttu-id="e042e-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="e042e-135">AzureEndpoints</span></span>
- <span data-ttu-id="e042e-136">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="e042e-136">ExternalEndpoints</span></span>
- <span data-ttu-id="e042e-137">Nestedenvseçpuanlar</span><span class="sxs-lookup"><span data-stu-id="e042e-137">NestedEndpoints</span></span>

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

### <span data-ttu-id="e042e-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="e042e-138">-Confirm</span></span>
<span data-ttu-id="e042e-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e042e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e042e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e042e-140">-WhatIf</span></span>
<span data-ttu-id="e042e-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e042e-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e042e-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e042e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e042e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e042e-143">CommonParameters</span></span>
<span data-ttu-id="e042e-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e042e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e042e-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e042e-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e042e-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e042e-146">INPUTS</span></span>

### <span data-ttu-id="e042e-147">Microsoft. Azure. Commands. TrafficManager. modeller. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e042e-147">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="e042e-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e042e-148">OUTPUTS</span></span>

### <span data-ttu-id="e042e-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e042e-149">System.Boolean</span></span>

## <span data-ttu-id="e042e-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e042e-150">NOTES</span></span>

## <span data-ttu-id="e042e-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e042e-151">RELATED LINKS</span></span>

[<span data-ttu-id="e042e-152">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e042e-152">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="e042e-153">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e042e-153">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="e042e-154">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e042e-154">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="e042e-155">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="e042e-155">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="e042e-156">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e042e-156">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)

