---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 2129C457-592B-484C-A148-828BFD5895D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: da42677edbb9083df3c9a5a11b4d4910eda7dc84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593600"
---
# <span data-ttu-id="3f441-101">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3f441-101">Remove-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="3f441-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f441-102">SYNOPSIS</span></span>
<span data-ttu-id="3f441-103">Traffic Manager 'dan uç noktayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3f441-103">Removes an endpoint from Traffic Manager.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f441-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3f441-104">SYNTAX</span></span>

### <span data-ttu-id="3f441-105">Alanlardır</span><span class="sxs-lookup"><span data-stu-id="3f441-105">Fields</span></span>
```
Remove-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3f441-106">Nesnelerini</span><span class="sxs-lookup"><span data-stu-id="3f441-106">Object</span></span>
```
Remove-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f441-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3f441-107">DESCRIPTION</span></span>
<span data-ttu-id="3f441-108">**Remove-AzureRmTrafficManagerEndpoint** cmdlet 'ı Azure Traffic Manager 'dan bir uç noktayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3f441-108">The **Remove-AzureRmTrafficManagerEndpoint** cmdlet removes an endpoint from Azure Traffic Manager.</span></span>

<span data-ttu-id="3f441-109">Bu cmdlet, Traffic Manager hizmetine yapılan her değişikliği kaydeder.</span><span class="sxs-lookup"><span data-stu-id="3f441-109">This cmdlet commits each change to the Traffic Manager service.</span></span>
<span data-ttu-id="3f441-110">Yerel bir Traffic Manager profil nesnesinden birden fazla uç nokta kaldırmak ve değişiklikleri tek bir işlemde uygulamak için Remove-AzureRmTrafficManagerEndpointConfig cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="3f441-110">To remove multiple endpoints from a local Traffic Manager profile object and commit changes in a single operation, use the Remove-AzureRmTrafficManagerEndpointConfig cmdlet.</span></span>

<span data-ttu-id="3f441-111">**TrafficManagerEndpoint** nesnesini bu cmdlet 'e geçirmek için ardışık düzen işlecini kullanabilir veya *TrafficManagerEndpoint* parametresini kullanarak bir **TrafficManagerEndpoint** nesnesi belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3f441-111">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="3f441-112">Alternatif olarak, *ProfilAdı* ve *Resourcegroupname* parametreleriyle *ad* ve *tür* parametrelerini kullanarak uç nokta adını ve türünü de belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3f441-112">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="3f441-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3f441-113">EXAMPLES</span></span>

### <span data-ttu-id="3f441-114">Örnek 1: profilden uç noktayı kaldırma</span><span class="sxs-lookup"><span data-stu-id="3f441-114">Example 1: Remove an endpoint from a profile</span></span>
```
PS C:\>Remove-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="3f441-115">Bu komut, contoso adlı Azure uç noktasını, ResourceGroup11 adlı kaynak grubundaki ContosoProfile adlı profilden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3f441-115">This command removes the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="3f441-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3f441-116">PARAMETERS</span></span>

### <span data-ttu-id="3f441-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f441-117">-DefaultProfile</span></span>
<span data-ttu-id="3f441-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3f441-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f441-119">-Force</span><span class="sxs-lookup"><span data-stu-id="3f441-119">-Force</span></span>
<span data-ttu-id="3f441-120">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="3f441-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3f441-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="3f441-121">-Name</span></span>
<span data-ttu-id="3f441-122">Bu cmdlet 'in kaldırdığı Traffic Manager uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f441-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3f441-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="3f441-123">-ProfileName</span></span>
<span data-ttu-id="3f441-124">Bu cmdlet 'in uç noktayı kaldırdığı bir Traffic Manager profilinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f441-124">Specifies the name of a Traffic Manager profile from which this cmdlet removes an endpoint.</span></span>
<span data-ttu-id="3f441-125">Profil edinmek için Get-AzureRmTrafficManagerProfile cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="3f441-125">To obtain a profile, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="3f441-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f441-126">-ResourceGroupName</span></span>
<span data-ttu-id="3f441-127">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f441-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="3f441-128">Bu cmdlet, bu parametrenin belirttiği gruptaki bir Traffic Manager profilindeki Traffic Manager uç noktasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3f441-128">This cmdlet removes a Traffic Manager endpoint from a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3f441-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3f441-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="3f441-130">Bu cmdlet 'in kaldırdığı Traffic Manager uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f441-130">Specifies the Traffic Manager endpoint that this cmdlet removes.</span></span>
<span data-ttu-id="3f441-131">**TrafficManagerEndpoint** nesnesi almak için Get-AzureRmTrafficManagerEndpoint cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="3f441-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="3f441-132">-Tür</span><span class="sxs-lookup"><span data-stu-id="3f441-132">-Type</span></span>
<span data-ttu-id="3f441-133">Bu cmdlet 'in Traffic Manager profiline eklediği uç nokta türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f441-133">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="3f441-134">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="3f441-134">Valid values are:</span></span> 

- <span data-ttu-id="3f441-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="3f441-135">AzureEndpoints</span></span>
- <span data-ttu-id="3f441-136">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="3f441-136">ExternalEndpoints</span></span>
- <span data-ttu-id="3f441-137">Nestedenvseçpuanlar</span><span class="sxs-lookup"><span data-stu-id="3f441-137">NestedEndpoints</span></span>

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

### <span data-ttu-id="3f441-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="3f441-138">-Confirm</span></span>
<span data-ttu-id="3f441-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3f441-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f441-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f441-140">-WhatIf</span></span>
<span data-ttu-id="3f441-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3f441-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f441-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3f441-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f441-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f441-143">CommonParameters</span></span>
<span data-ttu-id="3f441-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3f441-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f441-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f441-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f441-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3f441-146">INPUTS</span></span>

### <span data-ttu-id="3f441-147">TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3f441-147">TrafficManagerEndpoint</span></span>
<span data-ttu-id="3f441-148">' TrafficManagerEndpoint ' parametresi ardışık düzen için ' TrafficManagerEndpoint ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="3f441-148">Parameter 'TrafficManagerEndpoint' accepts value of type 'TrafficManagerEndpoint' from the pipeline</span></span>

## <span data-ttu-id="3f441-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3f441-149">OUTPUTS</span></span>

### <span data-ttu-id="3f441-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3f441-150">System.Boolean</span></span>

## <span data-ttu-id="3f441-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3f441-151">NOTES</span></span>

## <span data-ttu-id="3f441-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3f441-152">RELATED LINKS</span></span>

[<span data-ttu-id="3f441-153">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3f441-153">Get-AzureRmTrafficManagerEndpoint</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="3f441-154">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3f441-154">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="3f441-155">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3f441-155">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="3f441-156">Remove-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="3f441-156">Remove-AzureRmTrafficManagerEndpointConfig</span></span>](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="3f441-157">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3f441-157">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


