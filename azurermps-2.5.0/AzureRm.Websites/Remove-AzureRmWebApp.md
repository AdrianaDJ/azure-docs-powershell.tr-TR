---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebapp
schema: 2.0.0
ms.openlocfilehash: e7c0d37dc56e1ff4c986aa66632dccddec283c83
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939830"
---
# <span data-ttu-id="f5c5c-101">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f5c5c-101">Remove-AzureRmWebApp</span></span>

## <span data-ttu-id="f5c5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5c5c-102">SYNOPSIS</span></span>
<span data-ttu-id="f5c5c-103">Azure Web App 'i kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f5c5c-103">Removes an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5c5c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f5c5c-104">SYNTAX</span></span>

### <span data-ttu-id="f5c5c-105">S1</span><span class="sxs-lookup"><span data-stu-id="f5c5c-105">S1</span></span>
```
Remove-AzureRmWebApp [-Force] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5c5c-106">S2</span><span class="sxs-lookup"><span data-stu-id="f5c5c-106">S2</span></span>
```
Remove-AzureRmWebApp [-Force] [-WebApp] <Site> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f5c5c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f5c5c-107">DESCRIPTION</span></span>
<span data-ttu-id="f5c5c-108">**Remove-AzureRmWebApp** cmdlet 'i, kaynak grubuna ve Web uygulaması adına sağlanan bir Azure Web uygulamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f5c5c-108">The **Remove-AzureRmWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="f5c5c-109">Bu cmdlet varsayılan olarak tüm yuvaları ve ölçümleri de kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f5c5c-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="f5c5c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f5c5c-110">EXAMPLES</span></span>

### <span data-ttu-id="f5c5c-111">Örnek 1: Web uygulamasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="f5c5c-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="f5c5c-112">Bu komut, varsayılan-Web-WestUS adlı kaynak grubuna ait olan ContosoSite adlı Azure Web uygulamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f5c5c-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="f5c5c-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f5c5c-113">PARAMETERS</span></span>

### <span data-ttu-id="f5c5c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5c5c-114">-DefaultProfile</span></span>
<span data-ttu-id="f5c5c-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f5c5c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5c5c-116">-Force</span><span class="sxs-lookup"><span data-stu-id="f5c5c-116">-Force</span></span>
<span data-ttu-id="f5c5c-117">Zorla Kaldır seçeneği</span><span class="sxs-lookup"><span data-stu-id="f5c5c-117">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="f5c5c-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="f5c5c-118">-Name</span></span>
<span data-ttu-id="f5c5c-119">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="f5c5c-119">WebApp Name</span></span>

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

### <span data-ttu-id="f5c5c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5c5c-120">-ResourceGroupName</span></span>
<span data-ttu-id="f5c5c-121">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="f5c5c-121">Resource Group Name</span></span>

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

### <span data-ttu-id="f5c5c-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="f5c5c-122">-WebApp</span></span>
<span data-ttu-id="f5c5c-123">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="f5c5c-123">WebApp Object</span></span>

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

### <span data-ttu-id="f5c5c-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="f5c5c-124">-Confirm</span></span>
<span data-ttu-id="f5c5c-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister. Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f5c5c-125">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5c5c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5c5c-126">-WhatIf</span></span>
<span data-ttu-id="f5c5c-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f5c5c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5c5c-128">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f5c5c-128">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5c5c-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f5c5c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5c5c-130">-Iş</span><span class="sxs-lookup"><span data-stu-id="f5c5c-130">-AsJob</span></span>
<span data-ttu-id="f5c5c-131">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="f5c5c-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f5c5c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5c5c-132">CommonParameters</span></span>
<span data-ttu-id="f5c5c-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f5c5c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5c5c-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5c5c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5c5c-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f5c5c-135">INPUTS</span></span>

### <span data-ttu-id="f5c5c-136">Bölge</span><span class="sxs-lookup"><span data-stu-id="f5c5c-136">Site</span></span>
<span data-ttu-id="f5c5c-137">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="f5c5c-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="f5c5c-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f5c5c-138">OUTPUTS</span></span>

## <span data-ttu-id="f5c5c-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f5c5c-139">NOTES</span></span>

## <span data-ttu-id="f5c5c-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f5c5c-140">RELATED LINKS</span></span>

[<span data-ttu-id="f5c5c-141">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f5c5c-141">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="f5c5c-142">Yeni-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f5c5c-142">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="f5c5c-143">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f5c5c-143">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="f5c5c-144">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f5c5c-144">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="f5c5c-145">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f5c5c-145">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


