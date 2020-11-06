---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 2129C457-592B-484C-A148-828BFD5895D4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 04053050720f2639eeeb698dcfbffb3e156fe2c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589929"
---
# <span data-ttu-id="d2042-101">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d2042-101">Remove-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="d2042-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2042-102">SYNOPSIS</span></span>
<span data-ttu-id="d2042-103">Traffic Manager 'dan uç noktayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d2042-103">Removes an endpoint from Traffic Manager.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2042-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d2042-104">SYNTAX</span></span>

### <span data-ttu-id="d2042-105">Alanlardır</span><span class="sxs-lookup"><span data-stu-id="d2042-105">Fields</span></span>
```
Remove-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d2042-106">Nesnelerini</span><span class="sxs-lookup"><span data-stu-id="d2042-106">Object</span></span>
```
Remove-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2042-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d2042-107">DESCRIPTION</span></span>
<span data-ttu-id="d2042-108">**Remove-AzureRmTrafficManagerEndpoint** cmdlet 'ı Azure Traffic Manager 'dan bir uç noktayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d2042-108">The **Remove-AzureRmTrafficManagerEndpoint** cmdlet removes an endpoint from Azure Traffic Manager.</span></span>

<span data-ttu-id="d2042-109">Bu cmdlet, Traffic Manager hizmetine yapılan her değişikliği kaydeder.</span><span class="sxs-lookup"><span data-stu-id="d2042-109">This cmdlet commits each change to the Traffic Manager service.</span></span>
<span data-ttu-id="d2042-110">Yerel bir Traffic Manager profil nesnesinden birden fazla uç nokta kaldırmak ve değişiklikleri tek bir işlemde uygulamak için Remove-AzureRmTrafficManagerEndpointConfig cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d2042-110">To remove multiple endpoints from a local Traffic Manager profile object and commit changes in a single operation, use the Remove-AzureRmTrafficManagerEndpointConfig cmdlet.</span></span>

<span data-ttu-id="d2042-111">**TrafficManagerEndpoint** nesnesini bu cmdlet 'e geçirmek için ardışık düzen işlecini kullanabilir veya *TrafficManagerEndpoint* parametresini kullanarak bir **TrafficManagerEndpoint** nesnesi belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d2042-111">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="d2042-112">Alternatif olarak, *ProfilAdı* ve *Resourcegroupname* parametreleriyle *ad* ve *tür* parametrelerini kullanarak uç nokta adını ve türünü de belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d2042-112">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="d2042-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d2042-113">EXAMPLES</span></span>

### <span data-ttu-id="d2042-114">Örnek 1: profilden uç noktayı kaldırma</span><span class="sxs-lookup"><span data-stu-id="d2042-114">Example 1: Remove an endpoint from a profile</span></span>
```
PS C:\>Remove-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="d2042-115">Bu komut, contoso adlı Azure uç noktasını, ResourceGroup11 adlı kaynak grubundaki ContosoProfile adlı profilden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d2042-115">This command removes the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="d2042-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d2042-116">PARAMETERS</span></span>

### <span data-ttu-id="d2042-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d2042-117">-Force</span></span>
<span data-ttu-id="d2042-118">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="d2042-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d2042-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="d2042-119">-Name</span></span>
<span data-ttu-id="d2042-120">Bu cmdlet 'in kaldırdığı Traffic Manager uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d2042-120">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d2042-121">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="d2042-121">-ProfileName</span></span>
<span data-ttu-id="d2042-122">Bu cmdlet 'in uç noktayı kaldırdığı bir Traffic Manager profilinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d2042-122">Specifies the name of a Traffic Manager profile from which this cmdlet removes an endpoint.</span></span>
<span data-ttu-id="d2042-123">Profil edinmek için Get-AzureRmTrafficManagerProfile cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d2042-123">To obtain a profile, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="d2042-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2042-124">-ResourceGroupName</span></span>
<span data-ttu-id="d2042-125">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d2042-125">Specifies the name of a resource group.</span></span>
<span data-ttu-id="d2042-126">Bu cmdlet, bu parametrenin belirttiği gruptaki bir Traffic Manager profilindeki Traffic Manager uç noktasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d2042-126">This cmdlet removes a Traffic Manager endpoint from a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d2042-127">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d2042-127">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="d2042-128">Bu cmdlet 'in kaldırdığı Traffic Manager uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d2042-128">Specifies the Traffic Manager endpoint that this cmdlet removes.</span></span>
<span data-ttu-id="d2042-129">**TrafficManagerEndpoint** nesnesi almak için Get-AzureRmTrafficManagerEndpoint cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d2042-129">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="d2042-130">-Tür</span><span class="sxs-lookup"><span data-stu-id="d2042-130">-Type</span></span>
<span data-ttu-id="d2042-131">Bu cmdlet 'in Traffic Manager profiline eklediği uç nokta türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="d2042-131">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="d2042-132">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="d2042-132">Valid values are:</span></span> 

- <span data-ttu-id="d2042-133">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="d2042-133">AzureEndpoints</span></span>
- <span data-ttu-id="d2042-134">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="d2042-134">ExternalEndpoints</span></span>
- <span data-ttu-id="d2042-135">Nestedenvseçpuanlar</span><span class="sxs-lookup"><span data-stu-id="d2042-135">NestedEndpoints</span></span>

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

### <span data-ttu-id="d2042-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="d2042-136">-Confirm</span></span>
<span data-ttu-id="d2042-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d2042-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2042-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2042-138">-WhatIf</span></span>
<span data-ttu-id="d2042-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d2042-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2042-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d2042-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2042-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2042-141">-DefaultProfile</span></span>
<span data-ttu-id="d2042-142">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d2042-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2042-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2042-143">CommonParameters</span></span>
<span data-ttu-id="d2042-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d2042-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2042-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2042-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2042-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d2042-146">INPUTS</span></span>

### <span data-ttu-id="d2042-147">TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d2042-147">TrafficManagerEndpoint</span></span>
<span data-ttu-id="d2042-148">' TrafficManagerEndpoint ' parametresi ardışık düzen için ' TrafficManagerEndpoint ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="d2042-148">Parameter 'TrafficManagerEndpoint' accepts value of type 'TrafficManagerEndpoint' from the pipeline</span></span>

## <span data-ttu-id="d2042-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d2042-149">OUTPUTS</span></span>

### <span data-ttu-id="d2042-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d2042-150">System.Boolean</span></span>

## <span data-ttu-id="d2042-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d2042-151">NOTES</span></span>

## <span data-ttu-id="d2042-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d2042-152">RELATED LINKS</span></span>

[<span data-ttu-id="d2042-153">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d2042-153">Get-AzureRmTrafficManagerEndpoint</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="d2042-154">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d2042-154">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="d2042-155">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d2042-155">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="d2042-156">Remove-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="d2042-156">Remove-AzureRmTrafficManagerEndpointConfig</span></span>](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="d2042-157">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d2042-157">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


