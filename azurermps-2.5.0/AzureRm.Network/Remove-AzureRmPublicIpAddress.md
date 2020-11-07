---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 00236BC2-61D8-49C2-91BE-923C567153F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermpublicipaddress
schema: 2.0.0
ms.openlocfilehash: af8a85c698a59a31516c6dee05bb57415a45ff62
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939273"
---
# <span data-ttu-id="8074e-101">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8074e-101">Remove-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="8074e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8074e-102">SYNOPSIS</span></span>
<span data-ttu-id="8074e-103">Genel IP adresini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8074e-103">Removes a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8074e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8074e-104">SYNTAX</span></span>

```
Remove-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8074e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8074e-105">DESCRIPTION</span></span>
<span data-ttu-id="8074e-106">**Remove-Azurermpublicıpaddress** cmdlet 'ı bir Azure genel IP adresini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8074e-106">The **Remove-AzureRmPublicIpAddress** cmdlet removes an Azure public IP address.</span></span>

## <span data-ttu-id="8074e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8074e-107">EXAMPLES</span></span>

### <span data-ttu-id="8074e-108">1: genel IP adresi kaynağını kaldırma</span><span class="sxs-lookup"><span data-stu-id="8074e-108">1: Remove a public IP address resource</span></span>
```
Remove-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="8074e-109">Bu komut, kaynak grubundaki $publicIpName adlı ortak IP adresi kaynağını kaldırır $rgName.</span><span class="sxs-lookup"><span data-stu-id="8074e-109">This command removes the public IP address resource named $publicIpName in the resource group $rgName.</span></span>

## <span data-ttu-id="8074e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8074e-110">PARAMETERS</span></span>

### <span data-ttu-id="8074e-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="8074e-111">-AsJob</span></span>
<span data-ttu-id="8074e-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="8074e-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8074e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8074e-113">-DefaultProfile</span></span>
<span data-ttu-id="8074e-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8074e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8074e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8074e-115">-Force</span></span>
<span data-ttu-id="8074e-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="8074e-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8074e-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="8074e-117">-Name</span></span>
<span data-ttu-id="8074e-118">Bu cmdlet 'in kaldırdığı ortak IP adresinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8074e-118">Specifies the name of the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8074e-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="8074e-119">-PassThru</span></span>
<span data-ttu-id="8074e-120">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="8074e-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8074e-121">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="8074e-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8074e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8074e-122">-ResourceGroupName</span></span>
<span data-ttu-id="8074e-123">Bu cmdlet 'in kaldırıldığı ortak IP adresini içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8074e-123">Specifies the name of the resource group that contains the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8074e-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="8074e-124">-Confirm</span></span>
<span data-ttu-id="8074e-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8074e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8074e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8074e-126">-WhatIf</span></span>
<span data-ttu-id="8074e-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8074e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8074e-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8074e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8074e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8074e-129">CommonParameters</span></span>
<span data-ttu-id="8074e-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8074e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8074e-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8074e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8074e-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8074e-132">INPUTS</span></span>

## <span data-ttu-id="8074e-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8074e-133">OUTPUTS</span></span>

## <span data-ttu-id="8074e-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8074e-134">NOTES</span></span>

## <span data-ttu-id="8074e-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8074e-135">RELATED LINKS</span></span>

[<span data-ttu-id="8074e-136">Get-Azurermpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="8074e-136">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="8074e-137">Yeni-Azurermpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="8074e-137">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="8074e-138">Set-Azurermpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="8074e-138">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)


