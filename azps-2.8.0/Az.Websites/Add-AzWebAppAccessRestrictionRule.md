---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: bbb68888634b53d333f1c085443db8b205773e06
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934382"
---
# <span data-ttu-id="3d80b-101">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="3d80b-101">Add-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="3d80b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d80b-102">SYNOPSIS</span></span>
<span data-ttu-id="3d80b-103">Bir Azure Web uygulamasına bir Access randevu kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="3d80b-103">Adds an Access Restiction rule to an Azure Web App.</span></span>

## <span data-ttu-id="3d80b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3d80b-104">SYNTAX</span></span>

### <span data-ttu-id="3d80b-105">IpAddressParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3d80b-105">IpAddressParameterSet (Default)</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> -Name <String>
 [-Description <String>] -Priority <UInt32> -Action <String> [-SlotName <String>] [-TargetScmSite]
 -IpAddress <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3d80b-106">SubnetNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d80b-106">SubnetNameParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> -Name <String>
 [-Description <String>] -Priority <UInt32> -Action <String> [-SlotName <String>] [-TargetScmSite]
 -SubnetName <String> -VirtualNetworkName <String> [-IgnoreMissingServiceEndpoint] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d80b-107">Subnetıvseçparameterset</span><span class="sxs-lookup"><span data-stu-id="3d80b-107">SubnetIdParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> -Name <String>
 [-Description <String>] -Priority <UInt32> -Action <String> [-SlotName <String>] [-TargetScmSite]
 -SubnetId <String> [-IgnoreMissingServiceEndpoint] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d80b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3d80b-108">DESCRIPTION</span></span>
<span data-ttu-id="3d80b-109">**Add-AzWebAppAccessRestrictionRule** cmdlet 'ı bir Azure Web uygulamasına erişim kısıtlama kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="3d80b-109">The **Add-AzWebAppAccessRestrictionRule** cmdlet adds an Access Restriction rule to an Azure Web App.</span></span>

## <span data-ttu-id="3d80b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3d80b-110">EXAMPLES</span></span>

### <span data-ttu-id="3d80b-111">Örnek 1: Web uygulamasına IPAddress erişim kısıtlama kuralı ekleme</span><span class="sxs-lookup"><span data-stu-id="3d80b-111">Example 1: Add IpAddress Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name IpRule -Priority 200 -Action Allow -IpAddress 10.10.0.0/8
```

<span data-ttu-id="3d80b-112">Bu komut, varsayılan-Web-WestUS kaynak grubuna ait olan ContosoSite adlı Web uygulamasına öncelik 200 ve IP aralığı içeren bir erişim kısıtlama kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="3d80b-112">This command adds an access restriction rule with priority 200 and ip range to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="3d80b-113">Örnek 2: Web uygulamasına alt ağ hizmeti uç noktası erişim kısıtlama kuralı ekleme</span><span class="sxs-lookup"><span data-stu-id="3d80b-113">Example 2: Add Subnet Service Endpoint Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name SubnetRule -Priority 300 -Action Allow -SubnetName appgw-subnet -VirtualNetworkName corp-vnet
```

<span data-ttu-id="3d80b-114">Bu komut, öncelik 300 ve Corp-VNET içindeki alt ağ appgw-subnet 'i olan bir erişim kısıtlama kuralı ekleyerek, varsayılan-Web-WestUS kaynak grubuna ait olan ContosoSite adlı bir Web uygulamasına.</span><span class="sxs-lookup"><span data-stu-id="3d80b-114">This command adds an access restriction rule with priority 300 and with subnet appgw-subnet in corp-vnet to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="3d80b-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3d80b-115">PARAMETERS</span></span>

### <span data-ttu-id="3d80b-116">-Eylem</span><span class="sxs-lookup"><span data-stu-id="3d80b-116">-Action</span></span>
<span data-ttu-id="3d80b-117">Kuralı engelle veya Reddet.</span><span class="sxs-lookup"><span data-stu-id="3d80b-117">Allow or Deny rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d80b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d80b-118">-DefaultProfile</span></span>
<span data-ttu-id="3d80b-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3d80b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d80b-120">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="3d80b-120">-Description</span></span>
<span data-ttu-id="3d80b-121">Erişim kısıtlaması açıklaması.</span><span class="sxs-lookup"><span data-stu-id="3d80b-121">Access Restriction description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d80b-122">-Ignoremissingserviceendpoint</span><span class="sxs-lookup"><span data-stu-id="3d80b-122">-IgnoreMissingServiceEndpoint</span></span>
<span data-ttu-id="3d80b-123">Alt ağda hizmet uç noktası kaydının doğrulanıp doğrulanmayacağını belirtin.</span><span class="sxs-lookup"><span data-stu-id="3d80b-123">Specify if Service Endpoint registration at Subnet should be validated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SubnetNameParameterSet, SubnetIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d80b-124">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="3d80b-124">-IpAddress</span></span>
<span data-ttu-id="3d80b-125">IP adresi v4 veya V6 CıDR aralığı.</span><span class="sxs-lookup"><span data-stu-id="3d80b-125">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="3d80b-126">Örneğin: 192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="3d80b-126">E.g.: 192.168.0.0/24</span></span>

```yaml
Type: System.String
Parameter Sets: IpAddressParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d80b-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="3d80b-127">-Name</span></span>
<span data-ttu-id="3d80b-128">Kural adı</span><span class="sxs-lookup"><span data-stu-id="3d80b-128">Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d80b-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="3d80b-129">-PassThru</span></span>
<span data-ttu-id="3d80b-130">Erişim kısıtlama yapılandırması nesnesini döndür.</span><span class="sxs-lookup"><span data-stu-id="3d80b-130">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="3d80b-131">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="3d80b-131">-Priority</span></span>
<span data-ttu-id="3d80b-132">Erişim kısıtlama önceliği.</span><span class="sxs-lookup"><span data-stu-id="3d80b-132">Access Restriction priority.</span></span> <span data-ttu-id="3d80b-133">Örneğin: 500.</span><span class="sxs-lookup"><span data-stu-id="3d80b-133">E.g.: 500.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d80b-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d80b-134">-ResourceGroupName</span></span>
<span data-ttu-id="3d80b-135">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="3d80b-135">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d80b-136">-SlotName</span><span class="sxs-lookup"><span data-stu-id="3d80b-136">-SlotName</span></span>
<span data-ttu-id="3d80b-137">Dağıtım yuvası adı.</span><span class="sxs-lookup"><span data-stu-id="3d80b-137">Deployment Slot name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d80b-138">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="3d80b-138">-SubnetId</span></span>
<span data-ttu-id="3d80b-139">Alt ağın RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="3d80b-139">ResourceId of Subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: SubnetIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d80b-140">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="3d80b-140">-SubnetName</span></span>
<span data-ttu-id="3d80b-141">Alt ağ adı.</span><span class="sxs-lookup"><span data-stu-id="3d80b-141">Name of Subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d80b-142">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="3d80b-142">-TargetScmSite</span></span>
<span data-ttu-id="3d80b-143">Kural ana siteye veya SCM sitesine yöneliktir.</span><span class="sxs-lookup"><span data-stu-id="3d80b-143">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="3d80b-144">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="3d80b-144">-VirtualNetworkName</span></span>
<span data-ttu-id="3d80b-145">Sanal ağın adı.</span><span class="sxs-lookup"><span data-stu-id="3d80b-145">Name of Virtual Network.</span></span>

```yaml
Type: System.String
Parameter Sets: SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d80b-146">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="3d80b-146">-WebAppName</span></span>
<span data-ttu-id="3d80b-147">Web uygulamasının adı.</span><span class="sxs-lookup"><span data-stu-id="3d80b-147">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d80b-148">-Onay</span><span class="sxs-lookup"><span data-stu-id="3d80b-148">-Confirm</span></span>
<span data-ttu-id="3d80b-149">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3d80b-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d80b-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d80b-150">-WhatIf</span></span>
<span data-ttu-id="3d80b-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3d80b-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3d80b-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3d80b-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d80b-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d80b-153">CommonParameters</span></span>
<span data-ttu-id="3d80b-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3d80b-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d80b-155">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3d80b-155">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d80b-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3d80b-156">INPUTS</span></span>

### <span data-ttu-id="3d80b-157">System. String</span><span class="sxs-lookup"><span data-stu-id="3d80b-157">System.String</span></span>

## <span data-ttu-id="3d80b-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3d80b-158">OUTPUTS</span></span>

### <span data-ttu-id="3d80b-159">Microsoft. Azure. Commands. WebApps. modeller. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="3d80b-159">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="3d80b-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3d80b-160">NOTES</span></span>

## <span data-ttu-id="3d80b-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3d80b-161">RELATED LINKS</span></span>

[<span data-ttu-id="3d80b-162">Güncelleştirme-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="3d80b-162">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="3d80b-163">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="3d80b-163">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="3d80b-164">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="3d80b-164">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)