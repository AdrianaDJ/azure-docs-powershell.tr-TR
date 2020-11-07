---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 00236BC2-61D8-49C2-91BE-923C567153F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmPublicIpAddress.md
ms.openlocfilehash: 60c6a106acec84b3f43a3bd825e7be9b87fe8e70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593731"
---
# <span data-ttu-id="af882-101">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="af882-101">Remove-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="af882-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af882-102">SYNOPSIS</span></span>
<span data-ttu-id="af882-103">Genel IP adresini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="af882-103">Removes a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af882-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="af882-104">SYNTAX</span></span>

```
Remove-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af882-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="af882-105">DESCRIPTION</span></span>
<span data-ttu-id="af882-106">**Remove-Azurermpublicıpaddress** cmdlet 'ı bir Azure genel IP adresini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="af882-106">The **Remove-AzureRmPublicIpAddress** cmdlet removes an Azure public IP address.</span></span>

## <span data-ttu-id="af882-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="af882-107">EXAMPLES</span></span>

### <span data-ttu-id="af882-108">1: genel IP adresi kaynağını kaldırma</span><span class="sxs-lookup"><span data-stu-id="af882-108">1: Remove a public IP address resource</span></span>
```
Remove-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="af882-109">Bu komut, kaynak grubundaki $publicIpName adlı ortak IP adresi kaynağını kaldırır $rgName.</span><span class="sxs-lookup"><span data-stu-id="af882-109">This command removes the public IP address resource named $publicIpName in the resource group $rgName.</span></span>

## <span data-ttu-id="af882-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="af882-110">PARAMETERS</span></span>

### <span data-ttu-id="af882-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="af882-111">-AsJob</span></span>
<span data-ttu-id="af882-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="af882-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="af882-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af882-113">-DefaultProfile</span></span>
<span data-ttu-id="af882-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="af882-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af882-115">-Force</span><span class="sxs-lookup"><span data-stu-id="af882-115">-Force</span></span>
<span data-ttu-id="af882-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="af882-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="af882-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="af882-117">-Name</span></span>
<span data-ttu-id="af882-118">Bu cmdlet 'in kaldırdığı ortak IP adresinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="af882-118">Specifies the name of the public IP address that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af882-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="af882-119">-PassThru</span></span>
<span data-ttu-id="af882-120">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="af882-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="af882-121">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="af882-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="af882-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af882-122">-ResourceGroupName</span></span>
<span data-ttu-id="af882-123">Bu cmdlet 'in kaldırıldığı ortak IP adresini içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="af882-123">Specifies the name of the resource group that contains the public IP address that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af882-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="af882-124">-Confirm</span></span>
<span data-ttu-id="af882-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="af882-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af882-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af882-126">-WhatIf</span></span>
<span data-ttu-id="af882-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="af882-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af882-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="af882-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af882-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af882-129">CommonParameters</span></span>
<span data-ttu-id="af882-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="af882-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af882-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af882-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af882-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="af882-132">INPUTS</span></span>

### <span data-ttu-id="af882-133">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="af882-133">None</span></span>
<span data-ttu-id="af882-134">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="af882-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="af882-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="af882-135">OUTPUTS</span></span>

## <span data-ttu-id="af882-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="af882-136">NOTES</span></span>

## <span data-ttu-id="af882-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="af882-137">RELATED LINKS</span></span>

[<span data-ttu-id="af882-138">Get-Azurermpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="af882-138">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="af882-139">Yeni-Azurermpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="af882-139">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="af882-140">Set-Azurermpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="af882-140">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)

