---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: ad0bdc95ea3d582a2f8b6b6b1f8bc772c795352c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109313"
---
# <span data-ttu-id="12121-101">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="12121-101">Remove-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="12121-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12121-102">SYNOPSIS</span></span>
<span data-ttu-id="12121-103">Bir Azure Web uygulamasından erişim kısıtlama kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="12121-103">Removes an Access Restriction rule from an Azure Web App.</span></span>

## <span data-ttu-id="12121-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="12121-104">SYNTAX</span></span>

```
Remove-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Action <String>] [-TargetScmSite] [-SlotName <String>] [-IpAddress <String>] [-SubnetName <String>]
 [-VirtualNetworkName <String>] [-SubnetId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12121-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="12121-105">DESCRIPTION</span></span>
<span data-ttu-id="12121-106">**Remove-AzWebAppAccessRestrictionRule** cmdlet 'ı bir Azure Web uygulamasından erişim kısıtlama kuralını kaldırır</span><span class="sxs-lookup"><span data-stu-id="12121-106">The **Remove-AzWebAppAccessRestrictionRule** cmdlet removes an Access Restriction rule from an Azure Web App</span></span>

## <span data-ttu-id="12121-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="12121-107">EXAMPLES</span></span>

### <span data-ttu-id="12121-108">Örnek 1: Web uygulaması erişim kısıtlaması kuralını kaldırma</span><span class="sxs-lookup"><span data-stu-id="12121-108">Example 1: Remove a Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -Name IpRule
```

<span data-ttu-id="12121-109">Bu komut, varsayılan-Web-WestUS adlı kaynak grubuna ait olan ContosoSite adlı Azure Web App 'ten ıprule erişim kısıtlama kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="12121-109">This command removes the IpRule access restriction rule from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="12121-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="12121-110">PARAMETERS</span></span>

### <span data-ttu-id="12121-111">-Eylem</span><span class="sxs-lookup"><span data-stu-id="12121-111">-Action</span></span>
<span data-ttu-id="12121-112">Kuralı engelle veya Reddet.</span><span class="sxs-lookup"><span data-stu-id="12121-112">Allow or Deny rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: Allow
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12121-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12121-113">-DefaultProfile</span></span>
<span data-ttu-id="12121-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="12121-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12121-115">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="12121-115">-IpAddress</span></span>
<span data-ttu-id="12121-116">IP adresi v4 veya V6 CıDR aralığı.</span><span class="sxs-lookup"><span data-stu-id="12121-116">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="12121-117">Örneğin: 192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="12121-117">E.g.: 192.168.0.0/24</span></span>

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

### <span data-ttu-id="12121-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="12121-118">-Name</span></span>
<span data-ttu-id="12121-119">Erişim kısıtlama kuralı adı</span><span class="sxs-lookup"><span data-stu-id="12121-119">Access Restriction Rule Name</span></span>

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

### <span data-ttu-id="12121-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="12121-120">-PassThru</span></span>
<span data-ttu-id="12121-121">Erişim kısıtlama yapılandırması nesnesini döndür.</span><span class="sxs-lookup"><span data-stu-id="12121-121">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="12121-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12121-122">-ResourceGroupName</span></span>
<span data-ttu-id="12121-123">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="12121-123">Resource Group Name</span></span>

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

### <span data-ttu-id="12121-124">-SlotName</span><span class="sxs-lookup"><span data-stu-id="12121-124">-SlotName</span></span>
<span data-ttu-id="12121-125">Dağıtım yuvası adı.</span><span class="sxs-lookup"><span data-stu-id="12121-125">Deployment Slot Name.</span></span>

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

### <span data-ttu-id="12121-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="12121-126">-SubnetId</span></span>
<span data-ttu-id="12121-127">Alt ağın RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="12121-127">ResourceId of Subnet.</span></span>

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

### <span data-ttu-id="12121-128">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="12121-128">-SubnetName</span></span>
<span data-ttu-id="12121-129">Alt ağ adı.</span><span class="sxs-lookup"><span data-stu-id="12121-129">Name of Subnet.</span></span>

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

### <span data-ttu-id="12121-130">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="12121-130">-TargetScmSite</span></span>
<span data-ttu-id="12121-131">Kural ana siteye veya SCM sitesine yöneliktir.</span><span class="sxs-lookup"><span data-stu-id="12121-131">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="12121-132">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="12121-132">-VirtualNetworkName</span></span>
<span data-ttu-id="12121-133">Sanal ağın adı (Web App ile aynı kaynak grubunda olmalıdır).</span><span class="sxs-lookup"><span data-stu-id="12121-133">Name of Virtual Network (must be in same resource group as Web App).</span></span>

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

### <span data-ttu-id="12121-134">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="12121-134">-WebAppName</span></span>
<span data-ttu-id="12121-135">Web uygulamasının adı.</span><span class="sxs-lookup"><span data-stu-id="12121-135">The name of the web app.</span></span>

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

### <span data-ttu-id="12121-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="12121-136">-Confirm</span></span>
<span data-ttu-id="12121-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="12121-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12121-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12121-138">-WhatIf</span></span>
<span data-ttu-id="12121-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="12121-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="12121-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="12121-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12121-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12121-141">CommonParameters</span></span>
<span data-ttu-id="12121-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="12121-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12121-143">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="12121-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12121-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="12121-144">INPUTS</span></span>

### <span data-ttu-id="12121-145">System. String</span><span class="sxs-lookup"><span data-stu-id="12121-145">System.String</span></span>

## <span data-ttu-id="12121-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="12121-146">OUTPUTS</span></span>

### <span data-ttu-id="12121-147">Microsoft. Azure. Commands. WebApps. modeller. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="12121-147">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="12121-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="12121-148">NOTES</span></span>

## <span data-ttu-id="12121-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="12121-149">RELATED LINKS</span></span>

[<span data-ttu-id="12121-150">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="12121-150">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="12121-151">Güncelleştirme-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="12121-151">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="12121-152">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="12121-152">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)
