---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: 0631492bf2574fed7a9bb755088d811483504763
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934440"
---
# <span data-ttu-id="92d75-101">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="92d75-101">Remove-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="92d75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92d75-102">SYNOPSIS</span></span>
<span data-ttu-id="92d75-103">Bir Azure Web uygulamasından erişim kısıtlama kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="92d75-103">Removes an Access Restriction rule from an Azure Web App.</span></span>

## <span data-ttu-id="92d75-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="92d75-104">SYNTAX</span></span>

```
Remove-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> -Name <String>
 [-TargetScmSite] [-SlotName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92d75-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="92d75-105">DESCRIPTION</span></span>
<span data-ttu-id="92d75-106">**Remove-AzWebAppAccessRestrictionRule** cmdlet 'ı bir Azure Web uygulamasından erişim kısıtlama kuralını kaldırır</span><span class="sxs-lookup"><span data-stu-id="92d75-106">The **Remove-AzWebAppAccessRestrictionRule** cmdlet removes an Access Restriction rule from an Azure Web App</span></span>

## <span data-ttu-id="92d75-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="92d75-107">EXAMPLES</span></span>

### <span data-ttu-id="92d75-108">Örnek 1: Web uygulaması erişim kısıtlaması kuralını kaldırma</span><span class="sxs-lookup"><span data-stu-id="92d75-108">Example 1: Remove a Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -Name IpRule
```

<span data-ttu-id="92d75-109">Bu komut, varsayılan-Web-WestUS adlı kaynak grubuna ait olan ContosoSite adlı Azure Web App 'ten ıprule erişim kısıtlama kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="92d75-109">This command removes the IpRule access restriction rule from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="92d75-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="92d75-110">PARAMETERS</span></span>

### <span data-ttu-id="92d75-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92d75-111">-DefaultProfile</span></span>
<span data-ttu-id="92d75-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="92d75-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92d75-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="92d75-113">-Name</span></span>
<span data-ttu-id="92d75-114">Erişim kısıtlama kuralı adı</span><span class="sxs-lookup"><span data-stu-id="92d75-114">Access Restriction Rule Name</span></span>

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

### <span data-ttu-id="92d75-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="92d75-115">-PassThru</span></span>
<span data-ttu-id="92d75-116">Erişim kısıtlama yapılandırması nesnesini döndür.</span><span class="sxs-lookup"><span data-stu-id="92d75-116">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="92d75-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92d75-117">-ResourceGroupName</span></span>
<span data-ttu-id="92d75-118">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="92d75-118">Resource Group Name</span></span>

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

### <span data-ttu-id="92d75-119">-SlotName</span><span class="sxs-lookup"><span data-stu-id="92d75-119">-SlotName</span></span>
<span data-ttu-id="92d75-120">Dağıtım yuvası adı.</span><span class="sxs-lookup"><span data-stu-id="92d75-120">Deployment Slot Name.</span></span>

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

### <span data-ttu-id="92d75-121">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="92d75-121">-TargetScmSite</span></span>
<span data-ttu-id="92d75-122">Kural ana siteye veya SCM sitesine yöneliktir.</span><span class="sxs-lookup"><span data-stu-id="92d75-122">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="92d75-123">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="92d75-123">-WebAppName</span></span>
<span data-ttu-id="92d75-124">Web uygulamasının adı.</span><span class="sxs-lookup"><span data-stu-id="92d75-124">The name of the web app.</span></span>

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

### <span data-ttu-id="92d75-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="92d75-125">-Confirm</span></span>
<span data-ttu-id="92d75-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="92d75-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92d75-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92d75-127">-WhatIf</span></span>
<span data-ttu-id="92d75-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="92d75-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="92d75-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="92d75-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92d75-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92d75-130">CommonParameters</span></span>
<span data-ttu-id="92d75-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="92d75-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92d75-132">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="92d75-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92d75-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="92d75-133">INPUTS</span></span>

### <span data-ttu-id="92d75-134">System. String</span><span class="sxs-lookup"><span data-stu-id="92d75-134">System.String</span></span>

## <span data-ttu-id="92d75-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="92d75-135">OUTPUTS</span></span>

### <span data-ttu-id="92d75-136">Microsoft. Azure. Commands. WebApps. modeller. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="92d75-136">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="92d75-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="92d75-137">NOTES</span></span>

## <span data-ttu-id="92d75-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="92d75-138">RELATED LINKS</span></span>

[<span data-ttu-id="92d75-139">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="92d75-139">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="92d75-140">Güncelleştirme-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="92d75-140">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="92d75-141">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="92d75-141">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)
