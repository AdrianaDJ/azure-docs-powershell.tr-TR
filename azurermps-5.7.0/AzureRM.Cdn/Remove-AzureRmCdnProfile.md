---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 3A4F8442-1268-44BC-91ED-47C03CD20C47
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/remove-azurermcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnProfile.md
ms.openlocfilehash: 76c1f255b2d8dc3275ec3a691337019a7fd1e3e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764489"
---
# <span data-ttu-id="528aa-101">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="528aa-101">Remove-AzureRmCdnProfile</span></span>

## <span data-ttu-id="528aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="528aa-102">SYNOPSIS</span></span>
<span data-ttu-id="528aa-103">CDN profilini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="528aa-103">Removes a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="528aa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="528aa-104">SYNTAX</span></span>

### <span data-ttu-id="528aa-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="528aa-105">ByFieldsParameterSet</span></span>
```
Remove-AzureRmCdnProfile -ProfileName <String> -ResourceGroupName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="528aa-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="528aa-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmCdnProfile -CdnProfile <PSProfile> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="528aa-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="528aa-107">DESCRIPTION</span></span>
<span data-ttu-id="528aa-108">**Remove-AzureRmCdnProfile** cmdlet 'ı, Azure Içerik teslim ağı (CDN) profilini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="528aa-108">The **Remove-AzureRmCdnProfile** cmdlet removes a Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="528aa-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="528aa-109">EXAMPLES</span></span>

## <span data-ttu-id="528aa-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="528aa-110">PARAMETERS</span></span>

### <span data-ttu-id="528aa-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="528aa-111">-CdnProfile</span></span>
<span data-ttu-id="528aa-112">Bu cmdlet 'in kaldırdığı profili belirtir.</span><span class="sxs-lookup"><span data-stu-id="528aa-112">Specifies the profile that this cmdlet removes.</span></span>

```yaml
Type: PSProfile
Parameter Sets: ByObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="528aa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="528aa-113">-DefaultProfile</span></span>
<span data-ttu-id="528aa-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="528aa-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="528aa-115">-Force</span><span class="sxs-lookup"><span data-stu-id="528aa-115">-Force</span></span>
<span data-ttu-id="528aa-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="528aa-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="528aa-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="528aa-117">-PassThru</span></span>
<span data-ttu-id="528aa-118">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="528aa-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="528aa-119">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="528aa-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="528aa-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="528aa-120">-ProfileName</span></span>
<span data-ttu-id="528aa-121">Bu cmdlet 'in kaldırdığı profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="528aa-121">Specifies the name of the profile that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="528aa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="528aa-122">-ResourceGroupName</span></span>
<span data-ttu-id="528aa-123">Profilin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="528aa-123">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="528aa-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="528aa-124">-Confirm</span></span>
<span data-ttu-id="528aa-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="528aa-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="528aa-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="528aa-126">-WhatIf</span></span>
<span data-ttu-id="528aa-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="528aa-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="528aa-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="528aa-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="528aa-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="528aa-129">CommonParameters</span></span>
<span data-ttu-id="528aa-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="528aa-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="528aa-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="528aa-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="528aa-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="528aa-132">INPUTS</span></span>

### <span data-ttu-id="528aa-133">PSProfile</span><span class="sxs-lookup"><span data-stu-id="528aa-133">PSProfile</span></span>
<span data-ttu-id="528aa-134">' CdnProfile ' parametresi ardışık düzenin ' PSProfile ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="528aa-134">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="528aa-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="528aa-135">OUTPUTS</span></span>

### <span data-ttu-id="528aa-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="528aa-136">System.Boolean</span></span>

## <span data-ttu-id="528aa-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="528aa-137">NOTES</span></span>

## <span data-ttu-id="528aa-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="528aa-138">RELATED LINKS</span></span>

[<span data-ttu-id="528aa-139">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="528aa-139">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="528aa-140">Yeni-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="528aa-140">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="528aa-141">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="528aa-141">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


