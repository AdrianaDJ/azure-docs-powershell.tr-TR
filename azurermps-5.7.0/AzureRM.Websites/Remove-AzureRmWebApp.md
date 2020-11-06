---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebApp.md
ms.openlocfilehash: a984a9a76a41db93bee96acfa029ca05a30d85f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588682"
---
# <span data-ttu-id="88a31-101">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="88a31-101">Remove-AzureRmWebApp</span></span>

## <span data-ttu-id="88a31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88a31-102">SYNOPSIS</span></span>
<span data-ttu-id="88a31-103">Azure Web App 'i kaldırır.</span><span class="sxs-lookup"><span data-stu-id="88a31-103">Removes an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88a31-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="88a31-104">SYNTAX</span></span>

### <span data-ttu-id="88a31-105">S1</span><span class="sxs-lookup"><span data-stu-id="88a31-105">S1</span></span>
```
Remove-AzureRmWebApp [-Force] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88a31-106">S2</span><span class="sxs-lookup"><span data-stu-id="88a31-106">S2</span></span>
```
Remove-AzureRmWebApp [-Force] [-WebApp] <Site> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="88a31-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="88a31-107">DESCRIPTION</span></span>
<span data-ttu-id="88a31-108">**Remove-AzureRmWebApp** cmdlet 'i, kaynak grubuna ve Web uygulaması adına sağlanan bir Azure Web uygulamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="88a31-108">The **Remove-AzureRmWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="88a31-109">Bu cmdlet varsayılan olarak tüm yuvaları ve ölçümleri de kaldırır.</span><span class="sxs-lookup"><span data-stu-id="88a31-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="88a31-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="88a31-110">EXAMPLES</span></span>

### <span data-ttu-id="88a31-111">Örnek 1: Web uygulamasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="88a31-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="88a31-112">Bu komut, varsayılan-Web-WestUS adlı kaynak grubuna ait olan ContosoSite adlı Azure Web uygulamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="88a31-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="88a31-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="88a31-113">PARAMETERS</span></span>

### <span data-ttu-id="88a31-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88a31-114">-DefaultProfile</span></span>
<span data-ttu-id="88a31-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="88a31-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88a31-116">-Force</span><span class="sxs-lookup"><span data-stu-id="88a31-116">-Force</span></span>
<span data-ttu-id="88a31-117">Zorla Kaldır seçeneği</span><span class="sxs-lookup"><span data-stu-id="88a31-117">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="88a31-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="88a31-118">-Name</span></span>
<span data-ttu-id="88a31-119">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="88a31-119">WebApp Name</span></span>

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

### <span data-ttu-id="88a31-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88a31-120">-ResourceGroupName</span></span>
<span data-ttu-id="88a31-121">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="88a31-121">Resource Group Name</span></span>

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

### <span data-ttu-id="88a31-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="88a31-122">-WebApp</span></span>
<span data-ttu-id="88a31-123">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="88a31-123">WebApp Object</span></span>

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

### <span data-ttu-id="88a31-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="88a31-124">-Confirm</span></span>
<span data-ttu-id="88a31-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister. Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="88a31-125">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88a31-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88a31-126">-WhatIf</span></span>
<span data-ttu-id="88a31-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="88a31-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88a31-128">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="88a31-128">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88a31-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="88a31-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88a31-130">-Iş</span><span class="sxs-lookup"><span data-stu-id="88a31-130">-AsJob</span></span>
<span data-ttu-id="88a31-131">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="88a31-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="88a31-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88a31-132">CommonParameters</span></span>
<span data-ttu-id="88a31-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="88a31-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88a31-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88a31-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88a31-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="88a31-135">INPUTS</span></span>

### <span data-ttu-id="88a31-136">Bölge</span><span class="sxs-lookup"><span data-stu-id="88a31-136">Site</span></span>
<span data-ttu-id="88a31-137">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="88a31-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="88a31-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="88a31-138">OUTPUTS</span></span>

## <span data-ttu-id="88a31-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="88a31-139">NOTES</span></span>

## <span data-ttu-id="88a31-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="88a31-140">RELATED LINKS</span></span>

[<span data-ttu-id="88a31-141">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="88a31-141">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="88a31-142">Yeni-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="88a31-142">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="88a31-143">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="88a31-143">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="88a31-144">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="88a31-144">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="88a31-145">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="88a31-145">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


