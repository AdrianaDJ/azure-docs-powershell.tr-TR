---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppAccessRestrictionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppAccessRestrictionConfig.md
ms.openlocfilehash: 7c3caf3dfc033e6edefaf81b5f6bf5729ae86126
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934412"
---
# <span data-ttu-id="efa6e-101">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="efa6e-101">Update-AzWebAppAccessRestrictionConfig</span></span>

## <span data-ttu-id="efa6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efa6e-102">SYNOPSIS</span></span>
<span data-ttu-id="efa6e-103">Bir Azure Web uygulaması için ana site erişimi alt site yapılandırması 'nı SCM sitesine devralma işlemini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="efa6e-103">Updates the inheritance of Main site Access Restiction config to SCM Site for an Azure Web App.</span></span>

## <span data-ttu-id="efa6e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="efa6e-104">SYNTAX</span></span>

### <span data-ttu-id="efa6e-105">Inputvaluesparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="efa6e-105">InputValuesParameterSet (Default)</span></span>
```
Update-AzWebAppAccessRestrictionConfig [-ResourceGroupName] <String> [-Name] <String>
 [-ScmSiteUseMainSiteRestrictionConfig] [-SlotName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efa6e-106">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="efa6e-106">InputObjectParameterSet</span></span>
```
Update-AzWebAppAccessRestrictionConfig [-PassThru] -InputObject <PSAccessRestrictionConfig>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efa6e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="efa6e-107">DESCRIPTION</span></span>
<span data-ttu-id="efa6e-108">**Update-AzWebAppAccessRestrictionConfig** cmdlet 'ı bir Azure Web App Için erişim kısıtlama config 'i güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="efa6e-108">The **Update-AzWebAppAccessRestrictionConfig** cmdlet updates Access Restriction config for an Azure Web App.</span></span>

## <span data-ttu-id="efa6e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="efa6e-109">EXAMPLES</span></span>

### <span data-ttu-id="efa6e-110">Örnek 1: Web uygulaması SCM sitesini, ana siteden erişim kısıtlamalarını kullanacak şekilde güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="efa6e-110">Example 1: Update a Web App SCM Site to use Access Restrictions from Main Site</span></span>
```
PS C:\>Set-AzWebAppAccessRestriction -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -ScmSiteUseMainSiteRestrictionConfig
```

<span data-ttu-id="efa6e-111">Bu komut, varsayılan-Web-WestUS kaynak grubuna ait olan ContosoSite adlı bir Web uygulamasını, SCM sitesindeki ana sitenin erişim kısıtlama yapılandırmasını kullanacak şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="efa6e-111">This command updates a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS to use access restriction config of main site on the scm site.</span></span>

## <span data-ttu-id="efa6e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="efa6e-112">PARAMETERS</span></span>

### <span data-ttu-id="efa6e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efa6e-113">-DefaultProfile</span></span>
<span data-ttu-id="efa6e-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="efa6e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="efa6e-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="efa6e-115">-InputObject</span></span>
<span data-ttu-id="efa6e-116">Erişim kısıtlama yapılandırması nesnesi</span><span class="sxs-lookup"><span data-stu-id="efa6e-116">The access restriction config object</span></span>

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

### <span data-ttu-id="efa6e-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="efa6e-117">-Name</span></span>
<span data-ttu-id="efa6e-118">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="efa6e-118">WebApp Name</span></span>

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

### <span data-ttu-id="efa6e-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="efa6e-119">-PassThru</span></span>
<span data-ttu-id="efa6e-120">Erişim kısıtlama yapılandırması nesnesini döndür.</span><span class="sxs-lookup"><span data-stu-id="efa6e-120">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="efa6e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efa6e-121">-ResourceGroupName</span></span>
<span data-ttu-id="efa6e-122">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="efa6e-122">Resource Group Name</span></span>

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

### <span data-ttu-id="efa6e-123">-ScmSiteUseMainSiteRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="efa6e-123">-ScmSiteUseMainSiteRestrictionConfig</span></span>
<span data-ttu-id="efa6e-124">SCM sitesi, ana sitede ayarlanan kuralları devralır.</span><span class="sxs-lookup"><span data-stu-id="efa6e-124">Scm site inherits rules set on Main site.</span></span>

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

### <span data-ttu-id="efa6e-125">-SlotName</span><span class="sxs-lookup"><span data-stu-id="efa6e-125">-SlotName</span></span>
<span data-ttu-id="efa6e-126">Dağıtım yuvası adı.</span><span class="sxs-lookup"><span data-stu-id="efa6e-126">Deployment Slot name.</span></span>

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

### <span data-ttu-id="efa6e-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="efa6e-127">-Confirm</span></span>
<span data-ttu-id="efa6e-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="efa6e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efa6e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efa6e-129">-WhatIf</span></span>
<span data-ttu-id="efa6e-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="efa6e-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="efa6e-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="efa6e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efa6e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efa6e-132">CommonParameters</span></span>
<span data-ttu-id="efa6e-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="efa6e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efa6e-134">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="efa6e-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efa6e-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="efa6e-135">INPUTS</span></span>

### <span data-ttu-id="efa6e-136">System. String</span><span class="sxs-lookup"><span data-stu-id="efa6e-136">System.String</span></span>

### <span data-ttu-id="efa6e-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="efa6e-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="efa6e-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="efa6e-138">OUTPUTS</span></span>

### <span data-ttu-id="efa6e-139">Microsoft. Azure. Commands. WebApps. modeller. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="efa6e-139">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="efa6e-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="efa6e-140">NOTES</span></span>

## <span data-ttu-id="efa6e-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="efa6e-141">RELATED LINKS</span></span>

[<span data-ttu-id="efa6e-142">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="efa6e-142">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="efa6e-143">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="efa6e-143">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

[<span data-ttu-id="efa6e-144">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="efa6e-144">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
