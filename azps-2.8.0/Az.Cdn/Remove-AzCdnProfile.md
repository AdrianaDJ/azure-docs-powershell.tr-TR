---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 3A4F8442-1268-44BC-91ED-47C03CD20C47
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnProfile.md
ms.openlocfilehash: 6b8a5d9bd25c6f79cbfd70c509c9683b80453fe9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753051"
---
# <span data-ttu-id="5c430-101">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="5c430-101">Remove-AzCdnProfile</span></span>

## <span data-ttu-id="5c430-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c430-102">SYNOPSIS</span></span>
<span data-ttu-id="5c430-103">CDN profilini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5c430-103">Removes a CDN profile.</span></span>

## <span data-ttu-id="5c430-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5c430-104">SYNTAX</span></span>

### <span data-ttu-id="5c430-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c430-105">ByFieldsParameterSet</span></span>
```
Remove-AzCdnProfile -ProfileName <String> -ResourceGroupName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c430-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c430-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnProfile -CdnProfile <PSProfile> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c430-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5c430-107">DESCRIPTION</span></span>
<span data-ttu-id="5c430-108">**Remove-AzCdnProfile** cmdlet 'i, bir Azure Içerik teslim ağı (CDN) profilini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5c430-108">The **Remove-AzCdnProfile** cmdlet removes a Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="5c430-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5c430-109">EXAMPLES</span></span>

## <span data-ttu-id="5c430-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5c430-110">PARAMETERS</span></span>

### <span data-ttu-id="5c430-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="5c430-111">-CdnProfile</span></span>
<span data-ttu-id="5c430-112">Bu cmdlet 'in kaldırdığı profili belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c430-112">Specifies the profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5c430-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c430-113">-DefaultProfile</span></span>
<span data-ttu-id="5c430-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="5c430-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c430-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5c430-115">-Force</span></span>
<span data-ttu-id="5c430-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="5c430-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5c430-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="5c430-117">-PassThru</span></span>
<span data-ttu-id="5c430-118">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="5c430-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5c430-119">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="5c430-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5c430-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="5c430-120">-ProfileName</span></span>
<span data-ttu-id="5c430-121">Bu cmdlet 'in kaldırdığı profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c430-121">Specifies the name of the profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5c430-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c430-122">-ResourceGroupName</span></span>
<span data-ttu-id="5c430-123">Profilin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c430-123">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="5c430-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="5c430-124">-Confirm</span></span>
<span data-ttu-id="5c430-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5c430-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c430-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c430-126">-WhatIf</span></span>
<span data-ttu-id="5c430-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5c430-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c430-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5c430-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c430-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c430-129">CommonParameters</span></span>
<span data-ttu-id="5c430-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5c430-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c430-131">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5c430-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c430-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5c430-132">INPUTS</span></span>

### <span data-ttu-id="5c430-133">Microsoft. Azure. Commands. CDN. model. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="5c430-133">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

### <span data-ttu-id="5c430-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5c430-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5c430-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5c430-135">OUTPUTS</span></span>

### <span data-ttu-id="5c430-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5c430-136">System.Boolean</span></span>

## <span data-ttu-id="5c430-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5c430-137">NOTES</span></span>

## <span data-ttu-id="5c430-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5c430-138">RELATED LINKS</span></span>

[<span data-ttu-id="5c430-139">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="5c430-139">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="5c430-140">New-Azcıdnprofile</span><span class="sxs-lookup"><span data-stu-id="5c430-140">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="5c430-141">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="5c430-141">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


