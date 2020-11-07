---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/remove-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzWebApp.md
ms.openlocfilehash: 40b14128ec2a1dc48cf098a2c0427728c34c7e22
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936086"
---
# <span data-ttu-id="cd9f5-101">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="cd9f5-101">Remove-AzWebApp</span></span>

## <span data-ttu-id="cd9f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd9f5-102">SYNOPSIS</span></span>
<span data-ttu-id="cd9f5-103">Azure Web App 'i kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cd9f5-103">Removes an Azure Web App.</span></span>

## <span data-ttu-id="cd9f5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cd9f5-104">SYNTAX</span></span>

### <span data-ttu-id="cd9f5-105">S1</span><span class="sxs-lookup"><span data-stu-id="cd9f5-105">S1</span></span>
```
Remove-AzWebApp [-Force] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd9f5-106">S2</span><span class="sxs-lookup"><span data-stu-id="cd9f5-106">S2</span></span>
```
Remove-AzWebApp [-Force] [-WebApp] <Site> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cd9f5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="cd9f5-107">DESCRIPTION</span></span>
<span data-ttu-id="cd9f5-108">**Remove-AzWebApp** cmdlet 'i, kaynak grubuna ve Web uygulaması adına sağlanan bir Azure Web uygulamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cd9f5-108">The **Remove-AzWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="cd9f5-109">Bu cmdlet varsayılan olarak tüm yuvaları ve ölçümleri de kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cd9f5-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="cd9f5-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cd9f5-110">EXAMPLES</span></span>

### <span data-ttu-id="cd9f5-111">Örnek 1: Web uygulamasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="cd9f5-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="cd9f5-112">Bu komut, varsayılan-Web-WestUS adlı kaynak grubuna ait olan ContosoSite adlı Azure Web uygulamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cd9f5-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="cd9f5-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cd9f5-113">PARAMETERS</span></span>

### <span data-ttu-id="cd9f5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd9f5-114">-DefaultProfile</span></span>
<span data-ttu-id="cd9f5-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cd9f5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd9f5-116">-Force</span><span class="sxs-lookup"><span data-stu-id="cd9f5-116">-Force</span></span>
<span data-ttu-id="cd9f5-117">Zorla Kaldır seçeneği</span><span class="sxs-lookup"><span data-stu-id="cd9f5-117">Forcefully Remove Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd9f5-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="cd9f5-118">-Name</span></span>
<span data-ttu-id="cd9f5-119">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="cd9f5-119">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd9f5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd9f5-120">-ResourceGroupName</span></span>
<span data-ttu-id="cd9f5-121">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="cd9f5-121">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd9f5-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="cd9f5-122">-WebApp</span></span>
<span data-ttu-id="cd9f5-123">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="cd9f5-123">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd9f5-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="cd9f5-124">-Confirm</span></span>
<span data-ttu-id="cd9f5-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister. Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cd9f5-125">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd9f5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd9f5-126">-WhatIf</span></span>
<span data-ttu-id="cd9f5-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cd9f5-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd9f5-128">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cd9f5-128">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd9f5-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cd9f5-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd9f5-130">-Iş</span><span class="sxs-lookup"><span data-stu-id="cd9f5-130">-AsJob</span></span>
<span data-ttu-id="cd9f5-131">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="cd9f5-131">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd9f5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd9f5-132">CommonParameters</span></span>
<span data-ttu-id="cd9f5-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cd9f5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd9f5-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd9f5-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd9f5-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cd9f5-135">INPUTS</span></span>

### <span data-ttu-id="cd9f5-136">Bölge</span><span class="sxs-lookup"><span data-stu-id="cd9f5-136">Site</span></span>
<span data-ttu-id="cd9f5-137">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="cd9f5-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="cd9f5-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cd9f5-138">OUTPUTS</span></span>

## <span data-ttu-id="cd9f5-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cd9f5-139">NOTES</span></span>

## <span data-ttu-id="cd9f5-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cd9f5-140">RELATED LINKS</span></span>

[<span data-ttu-id="cd9f5-141">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="cd9f5-141">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="cd9f5-142">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="cd9f5-142">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="cd9f5-143">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="cd9f5-143">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="cd9f5-144">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="cd9f5-144">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="cd9f5-145">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="cd9f5-145">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


