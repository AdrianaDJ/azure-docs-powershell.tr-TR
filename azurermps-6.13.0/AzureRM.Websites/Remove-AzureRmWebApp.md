---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebApp.md
ms.openlocfilehash: b06a5253ac5b26097d2dc4dea9c3d557c00a4d46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587083"
---
# <span data-ttu-id="fdd26-101">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="fdd26-101">Remove-AzureRmWebApp</span></span>

## <span data-ttu-id="fdd26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fdd26-102">SYNOPSIS</span></span>
<span data-ttu-id="fdd26-103">Azure Web App 'i kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fdd26-103">Removes an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdd26-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fdd26-104">SYNTAX</span></span>

### <span data-ttu-id="fdd26-105">S1</span><span class="sxs-lookup"><span data-stu-id="fdd26-105">S1</span></span>
```
Remove-AzureRmWebApp [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdd26-106">S2</span><span class="sxs-lookup"><span data-stu-id="fdd26-106">S2</span></span>
```
Remove-AzureRmWebApp [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdd26-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="fdd26-107">DESCRIPTION</span></span>
<span data-ttu-id="fdd26-108">**Remove-AzureRmWebApp** cmdlet 'i, kaynak grubuna ve Web uygulaması adına sağlanan bir Azure Web uygulamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fdd26-108">The **Remove-AzureRmWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="fdd26-109">Bu cmdlet varsayılan olarak tüm yuvaları ve ölçümleri de kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fdd26-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="fdd26-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fdd26-110">EXAMPLES</span></span>

### <span data-ttu-id="fdd26-111">Örnek 1: Web uygulamasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="fdd26-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="fdd26-112">Bu komut, varsayılan-Web-WestUS adlı kaynak grubuna ait olan ContosoSite adlı Azure Web uygulamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fdd26-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="fdd26-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fdd26-113">PARAMETERS</span></span>

### <span data-ttu-id="fdd26-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="fdd26-114">-AsJob</span></span>
<span data-ttu-id="fdd26-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="fdd26-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fdd26-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdd26-116">-DefaultProfile</span></span>
<span data-ttu-id="fdd26-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fdd26-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fdd26-118">-Force</span><span class="sxs-lookup"><span data-stu-id="fdd26-118">-Force</span></span>
<span data-ttu-id="fdd26-119">Zorla Kaldır seçeneği</span><span class="sxs-lookup"><span data-stu-id="fdd26-119">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="fdd26-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="fdd26-120">-Name</span></span>
<span data-ttu-id="fdd26-121">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="fdd26-121">WebApp Name</span></span>

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

### <span data-ttu-id="fdd26-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdd26-122">-ResourceGroupName</span></span>
<span data-ttu-id="fdd26-123">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="fdd26-123">Resource Group Name</span></span>

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

### <span data-ttu-id="fdd26-124">-WebApp</span><span class="sxs-lookup"><span data-stu-id="fdd26-124">-WebApp</span></span>
<span data-ttu-id="fdd26-125">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="fdd26-125">WebApp Object</span></span>

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

### <span data-ttu-id="fdd26-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="fdd26-126">-Confirm</span></span>
<span data-ttu-id="fdd26-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister. Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fdd26-127">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdd26-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdd26-128">-WhatIf</span></span>
<span data-ttu-id="fdd26-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fdd26-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fdd26-130">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fdd26-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fdd26-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fdd26-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdd26-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdd26-132">CommonParameters</span></span>
<span data-ttu-id="fdd26-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fdd26-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdd26-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdd26-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdd26-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fdd26-135">INPUTS</span></span>

### <span data-ttu-id="fdd26-136">System. String</span><span class="sxs-lookup"><span data-stu-id="fdd26-136">System.String</span></span>

### <span data-ttu-id="fdd26-137">Microsoft. Azure. Management. Web sitesi. modeller. site</span><span class="sxs-lookup"><span data-stu-id="fdd26-137">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="fdd26-138">Parametreler: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fdd26-138">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="fdd26-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fdd26-139">OUTPUTS</span></span>

### <span data-ttu-id="fdd26-140">System. void</span><span class="sxs-lookup"><span data-stu-id="fdd26-140">System.Void</span></span>

## <span data-ttu-id="fdd26-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fdd26-141">NOTES</span></span>

## <span data-ttu-id="fdd26-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fdd26-142">RELATED LINKS</span></span>

[<span data-ttu-id="fdd26-143">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="fdd26-143">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="fdd26-144">Yeni-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="fdd26-144">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="fdd26-145">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="fdd26-145">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="fdd26-146">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="fdd26-146">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="fdd26-147">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="fdd26-147">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


