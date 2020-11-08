---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppAccessRestrictionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppAccessRestrictionConfig.md
ms.openlocfilehash: b2d2a2eb24fce89c65561c9d86f18072d4ac4e0a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107437"
---
# <span data-ttu-id="f52b8-101">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="f52b8-101">Update-AzWebAppAccessRestrictionConfig</span></span>

## <span data-ttu-id="f52b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f52b8-102">SYNOPSIS</span></span>
<span data-ttu-id="f52b8-103">Bir Azure Web uygulaması için ana site erişimi alt site yapılandırması 'nı SCM sitesine devralma işlemini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f52b8-103">Updates the inheritance of Main site Access Restiction config to SCM Site for an Azure Web App.</span></span>

## <span data-ttu-id="f52b8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f52b8-104">SYNTAX</span></span>

### <span data-ttu-id="f52b8-105">Inputvaluesparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f52b8-105">InputValuesParameterSet (Default)</span></span>
```
Update-AzWebAppAccessRestrictionConfig [-ResourceGroupName] <String> [-Name] <String>
 [-ScmSiteUseMainSiteRestrictionConfig] [-SlotName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f52b8-106">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="f52b8-106">InputObjectParameterSet</span></span>
```
Update-AzWebAppAccessRestrictionConfig [-PassThru] -InputObject <PSAccessRestrictionConfig>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f52b8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f52b8-107">DESCRIPTION</span></span>
<span data-ttu-id="f52b8-108">**Update-AzWebAppAccessRestrictionConfig** cmdlet 'ı bir Azure Web App Için erişim kısıtlama config 'i güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f52b8-108">The **Update-AzWebAppAccessRestrictionConfig** cmdlet updates Access Restriction config for an Azure Web App.</span></span>

## <span data-ttu-id="f52b8-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f52b8-109">EXAMPLES</span></span>

### <span data-ttu-id="f52b8-110">Örnek 1: Web uygulaması SCM sitesini, ana siteden erişim kısıtlamalarını kullanacak şekilde güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="f52b8-110">Example 1: Update a Web App SCM Site to use Access Restrictions from Main Site</span></span>

<span data-ttu-id="f52b8-111">Aşağıdaki örnek, SCM sitesindeki ana sitenin erişim kısıtlama yapılandırmasını kullanmak için MyResourceGroup kaynak grubuna ait ıprule adlı bir Web uygulamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f52b8-111">The following example updates a Web App named IpRule that belongs to the resource group MyResourceGroup to use access restriction config of main site on the scm site.</span></span>

```powershell <!-- Aladdin Generated Example --> 
Update-AzWebAppAccessRestrictionConfig -Name IpRule -ResourceGroupName MyResourceGroup -ScmSiteUseMainSiteRestrictionConfig
```

## <span data-ttu-id="f52b8-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f52b8-112">PARAMETERS</span></span>

### <span data-ttu-id="f52b8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f52b8-113">-DefaultProfile</span></span>
<span data-ttu-id="f52b8-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f52b8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f52b8-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f52b8-115">-InputObject</span></span>
<span data-ttu-id="f52b8-116">Erişim kısıtlama yapılandırması nesnesi</span><span class="sxs-lookup"><span data-stu-id="f52b8-116">The access restriction config object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f52b8-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="f52b8-117">-Name</span></span>
<span data-ttu-id="f52b8-118">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="f52b8-118">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f52b8-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f52b8-119">-PassThru</span></span>
<span data-ttu-id="f52b8-120">Erişim kısıtlama yapılandırması nesnesini döndür.</span><span class="sxs-lookup"><span data-stu-id="f52b8-120">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="f52b8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f52b8-121">-ResourceGroupName</span></span>
<span data-ttu-id="f52b8-122">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="f52b8-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f52b8-123">-ScmSiteUseMainSiteRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="f52b8-123">-ScmSiteUseMainSiteRestrictionConfig</span></span>
<span data-ttu-id="f52b8-124">SCM sitesi, ana sitede ayarlanan kuralları devralır.</span><span class="sxs-lookup"><span data-stu-id="f52b8-124">Scm site inherits rules set on Main site.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f52b8-125">-SlotName</span><span class="sxs-lookup"><span data-stu-id="f52b8-125">-SlotName</span></span>
<span data-ttu-id="f52b8-126">Dağıtım yuvası adı.</span><span class="sxs-lookup"><span data-stu-id="f52b8-126">Deployment Slot name.</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f52b8-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="f52b8-127">-Confirm</span></span>
<span data-ttu-id="f52b8-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f52b8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f52b8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f52b8-129">-WhatIf</span></span>
<span data-ttu-id="f52b8-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f52b8-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f52b8-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f52b8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f52b8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f52b8-132">CommonParameters</span></span>
<span data-ttu-id="f52b8-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f52b8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f52b8-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f52b8-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f52b8-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f52b8-135">INPUTS</span></span>

### <span data-ttu-id="f52b8-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f52b8-136">System.String</span></span>

### <span data-ttu-id="f52b8-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f52b8-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f52b8-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f52b8-138">OUTPUTS</span></span>

### <span data-ttu-id="f52b8-139">Microsoft. Azure. Commands. WebApps. modeller. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="f52b8-139">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="f52b8-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f52b8-140">NOTES</span></span>

## <span data-ttu-id="f52b8-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f52b8-141">RELATED LINKS</span></span>

[<span data-ttu-id="f52b8-142">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="f52b8-142">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="f52b8-143">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="f52b8-143">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

[<span data-ttu-id="f52b8-144">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="f52b8-144">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
