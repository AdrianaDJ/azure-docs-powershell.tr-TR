---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebApp.md
ms.openlocfilehash: b903e22a627ca2cb992b179e8f6956d556558b6b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594532"
---
# <span data-ttu-id="72f05-101">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="72f05-101">Remove-AzureRmWebApp</span></span>

## <span data-ttu-id="72f05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72f05-102">SYNOPSIS</span></span>
<span data-ttu-id="72f05-103">Azure Web App 'i kaldırır.</span><span class="sxs-lookup"><span data-stu-id="72f05-103">Removes an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72f05-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="72f05-104">SYNTAX</span></span>

### <span data-ttu-id="72f05-105">S1</span><span class="sxs-lookup"><span data-stu-id="72f05-105">S1</span></span>
```
Remove-AzureRmWebApp [-Force] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72f05-106">S2</span><span class="sxs-lookup"><span data-stu-id="72f05-106">S2</span></span>
```
Remove-AzureRmWebApp [-Force] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="72f05-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="72f05-107">DESCRIPTION</span></span>
<span data-ttu-id="72f05-108">**Remove-AzureRmWebApp** cmdlet 'i, kaynak grubuna ve Web uygulaması adına sağlanan bir Azure Web uygulamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="72f05-108">The **Remove-AzureRmWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="72f05-109">Bu cmdlet varsayılan olarak tüm yuvaları ve ölçümleri de kaldırır.</span><span class="sxs-lookup"><span data-stu-id="72f05-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="72f05-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="72f05-110">EXAMPLES</span></span>

### <span data-ttu-id="72f05-111">Örnek 1: Web uygulamasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="72f05-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="72f05-112">Bu komut, varsayılan-Web-WestUS adlı kaynak grubuna ait olan ContosoSite adlı Azure Web uygulamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="72f05-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="72f05-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="72f05-113">PARAMETERS</span></span>

### <span data-ttu-id="72f05-114">-Force</span><span class="sxs-lookup"><span data-stu-id="72f05-114">-Force</span></span>
<span data-ttu-id="72f05-115">Zorla Kaldır seçeneği</span><span class="sxs-lookup"><span data-stu-id="72f05-115">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="72f05-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="72f05-116">-Name</span></span>
<span data-ttu-id="72f05-117">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="72f05-117">WebApp Name</span></span>

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

### <span data-ttu-id="72f05-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72f05-118">-ResourceGroupName</span></span>
<span data-ttu-id="72f05-119">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="72f05-119">Resource Group Name</span></span>

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

### <span data-ttu-id="72f05-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="72f05-120">-WebApp</span></span>
<span data-ttu-id="72f05-121">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="72f05-121">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72f05-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="72f05-122">-Confirm</span></span>
<span data-ttu-id="72f05-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister. Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="72f05-123">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72f05-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72f05-124">-WhatIf</span></span>
<span data-ttu-id="72f05-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="72f05-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72f05-126">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="72f05-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72f05-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="72f05-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72f05-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72f05-128">-DefaultProfile</span></span>
<span data-ttu-id="72f05-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="72f05-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72f05-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72f05-130">CommonParameters</span></span>
<span data-ttu-id="72f05-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="72f05-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72f05-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72f05-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72f05-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="72f05-133">INPUTS</span></span>

### <span data-ttu-id="72f05-134">Bölge</span><span class="sxs-lookup"><span data-stu-id="72f05-134">Site</span></span>
<span data-ttu-id="72f05-135">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="72f05-135">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="72f05-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="72f05-136">OUTPUTS</span></span>

## <span data-ttu-id="72f05-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="72f05-137">NOTES</span></span>

## <span data-ttu-id="72f05-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="72f05-138">RELATED LINKS</span></span>

[<span data-ttu-id="72f05-139">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="72f05-139">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="72f05-140">Yeni-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="72f05-140">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="72f05-141">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="72f05-141">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="72f05-142">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="72f05-142">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="72f05-143">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="72f05-143">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


