---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
ms.openlocfilehash: c91e5ff71a916e28e199a1c64fde2d69f0193fd1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934441"
---
# <span data-ttu-id="86591-101">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="86591-101">Remove-AzWebApp</span></span>

## <span data-ttu-id="86591-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86591-102">SYNOPSIS</span></span>
<span data-ttu-id="86591-103">Azure Web App 'i kaldırır.</span><span class="sxs-lookup"><span data-stu-id="86591-103">Removes an Azure Web App.</span></span>

## <span data-ttu-id="86591-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="86591-104">SYNTAX</span></span>

### <span data-ttu-id="86591-105">S1</span><span class="sxs-lookup"><span data-stu-id="86591-105">S1</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86591-106">S2</span><span class="sxs-lookup"><span data-stu-id="86591-106">S2</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86591-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="86591-107">DESCRIPTION</span></span>
<span data-ttu-id="86591-108">**Remove-AzWebApp** cmdlet 'i, kaynak grubuna ve Web uygulaması adına sağlanan bir Azure Web uygulamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="86591-108">The **Remove-AzWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="86591-109">Bu cmdlet varsayılan olarak tüm yuvaları ve ölçümleri de kaldırır.</span><span class="sxs-lookup"><span data-stu-id="86591-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="86591-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="86591-110">EXAMPLES</span></span>

### <span data-ttu-id="86591-111">Örnek 1: Web uygulamasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="86591-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="86591-112">Bu komut, varsayılan-Web-WestUS adlı kaynak grubuna ait olan ContosoSite adlı Azure Web uygulamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="86591-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="86591-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="86591-113">PARAMETERS</span></span>

### <span data-ttu-id="86591-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="86591-114">-AsJob</span></span>
<span data-ttu-id="86591-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="86591-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="86591-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86591-116">-DefaultProfile</span></span>
<span data-ttu-id="86591-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="86591-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86591-118">-Force</span><span class="sxs-lookup"><span data-stu-id="86591-118">-Force</span></span>
<span data-ttu-id="86591-119">Zorla Kaldır seçeneği</span><span class="sxs-lookup"><span data-stu-id="86591-119">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="86591-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="86591-120">-Name</span></span>
<span data-ttu-id="86591-121">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="86591-121">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86591-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86591-122">-ResourceGroupName</span></span>
<span data-ttu-id="86591-123">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="86591-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86591-124">-WebApp</span><span class="sxs-lookup"><span data-stu-id="86591-124">-WebApp</span></span>
<span data-ttu-id="86591-125">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="86591-125">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86591-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="86591-126">-Confirm</span></span>
<span data-ttu-id="86591-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister. Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="86591-127">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86591-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86591-128">-WhatIf</span></span>
<span data-ttu-id="86591-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="86591-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86591-130">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="86591-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86591-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="86591-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86591-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86591-132">CommonParameters</span></span>
<span data-ttu-id="86591-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="86591-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86591-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86591-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86591-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="86591-135">INPUTS</span></span>

### <span data-ttu-id="86591-136">System. String</span><span class="sxs-lookup"><span data-stu-id="86591-136">System.String</span></span>

### <span data-ttu-id="86591-137">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="86591-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="86591-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="86591-138">OUTPUTS</span></span>

### <span data-ttu-id="86591-139">System. void</span><span class="sxs-lookup"><span data-stu-id="86591-139">System.Void</span></span>

## <span data-ttu-id="86591-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="86591-140">NOTES</span></span>

## <span data-ttu-id="86591-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="86591-141">RELATED LINKS</span></span>

[<span data-ttu-id="86591-142">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="86591-142">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="86591-143">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="86591-143">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="86591-144">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="86591-144">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="86591-145">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="86591-145">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="86591-146">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="86591-146">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

