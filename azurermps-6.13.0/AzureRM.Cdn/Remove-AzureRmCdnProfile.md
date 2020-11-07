---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 3A4F8442-1268-44BC-91ED-47C03CD20C47
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/remove-azurermcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnProfile.md
ms.openlocfilehash: 0c39e6ee26faffc9c12e2fc3b5f00ccaadfa9389
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591385"
---
# <span data-ttu-id="a0621-101">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="a0621-101">Remove-AzureRmCdnProfile</span></span>

## <span data-ttu-id="a0621-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0621-102">SYNOPSIS</span></span>
<span data-ttu-id="a0621-103">CDN profilini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a0621-103">Removes a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0621-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a0621-104">SYNTAX</span></span>

### <span data-ttu-id="a0621-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0621-105">ByFieldsParameterSet</span></span>
```
Remove-AzureRmCdnProfile -ProfileName <String> -ResourceGroupName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0621-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0621-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmCdnProfile -CdnProfile <PSProfile> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0621-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a0621-107">DESCRIPTION</span></span>
<span data-ttu-id="a0621-108">**Remove-AzureRmCdnProfile** cmdlet 'ı, Azure Içerik teslim ağı (CDN) profilini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a0621-108">The **Remove-AzureRmCdnProfile** cmdlet removes a Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="a0621-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a0621-109">EXAMPLES</span></span>

## <span data-ttu-id="a0621-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a0621-110">PARAMETERS</span></span>

### <span data-ttu-id="a0621-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="a0621-111">-CdnProfile</span></span>
<span data-ttu-id="a0621-112">Bu cmdlet 'in kaldırdığı profili belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0621-112">Specifies the profile that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0621-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0621-113">-DefaultProfile</span></span>
<span data-ttu-id="a0621-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a0621-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0621-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a0621-115">-Force</span></span>
<span data-ttu-id="a0621-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="a0621-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a0621-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a0621-117">-PassThru</span></span>
<span data-ttu-id="a0621-118">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="a0621-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a0621-119">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="a0621-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0621-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="a0621-120">-ProfileName</span></span>
<span data-ttu-id="a0621-121">Bu cmdlet 'in kaldırdığı profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0621-121">Specifies the name of the profile that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0621-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0621-122">-ResourceGroupName</span></span>
<span data-ttu-id="a0621-123">Profilin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0621-123">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0621-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="a0621-124">-Confirm</span></span>
<span data-ttu-id="a0621-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a0621-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0621-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0621-126">-WhatIf</span></span>
<span data-ttu-id="a0621-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a0621-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0621-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a0621-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0621-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0621-129">CommonParameters</span></span>
<span data-ttu-id="a0621-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a0621-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0621-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0621-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0621-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a0621-132">INPUTS</span></span>

### <span data-ttu-id="a0621-133">Microsoft. Azure. Commands. CDN. model. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="a0621-133">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>
<span data-ttu-id="a0621-134">Parametreler: Cdnprofıle (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a0621-134">Parameters: CdnProfile (ByValue)</span></span>

### <span data-ttu-id="a0621-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a0621-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a0621-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a0621-136">OUTPUTS</span></span>

### <span data-ttu-id="a0621-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a0621-137">System.Boolean</span></span>

## <span data-ttu-id="a0621-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a0621-138">NOTES</span></span>

## <span data-ttu-id="a0621-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a0621-139">RELATED LINKS</span></span>

[<span data-ttu-id="a0621-140">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="a0621-140">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="a0621-141">Yeni-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="a0621-141">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="a0621-142">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="a0621-142">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)

