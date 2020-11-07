---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 00236BC2-61D8-49C2-91BE-923C567153F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzPublicIpAddress.md
ms.openlocfilehash: 299e27d0d4824dfe06a6f1982f4eda1a04eeb1c4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936612"
---
# <span data-ttu-id="4da02-101">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="4da02-101">Remove-AzPublicIpAddress</span></span>

## <span data-ttu-id="4da02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4da02-102">SYNOPSIS</span></span>
<span data-ttu-id="4da02-103">Genel IP adresini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4da02-103">Removes a public IP address.</span></span>

## <span data-ttu-id="4da02-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4da02-104">SYNTAX</span></span>

```
Remove-AzPublicIpAddress -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4da02-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4da02-105">DESCRIPTION</span></span>
<span data-ttu-id="4da02-106">**Remove-Azpublicıpaddress** cmdlet 'ı bir Azure genel IP adresini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4da02-106">The **Remove-AzPublicIpAddress** cmdlet removes an Azure public IP address.</span></span>

## <span data-ttu-id="4da02-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4da02-107">EXAMPLES</span></span>

### <span data-ttu-id="4da02-108">1: genel IP adresi kaynağını kaldırma</span><span class="sxs-lookup"><span data-stu-id="4da02-108">1: Remove a public IP address resource</span></span>
```
Remove-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="4da02-109">Bu komut, kaynak grubundaki $publicIpName adlı ortak IP adresi kaynağını kaldırır $rgName.</span><span class="sxs-lookup"><span data-stu-id="4da02-109">This command removes the public IP address resource named $publicIpName in the resource group $rgName.</span></span>

## <span data-ttu-id="4da02-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4da02-110">PARAMETERS</span></span>

### <span data-ttu-id="4da02-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="4da02-111">-AsJob</span></span>
<span data-ttu-id="4da02-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="4da02-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4da02-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4da02-113">-DefaultProfile</span></span>
<span data-ttu-id="4da02-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4da02-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4da02-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4da02-115">-Force</span></span>
<span data-ttu-id="4da02-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="4da02-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4da02-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="4da02-117">-Name</span></span>
<span data-ttu-id="4da02-118">Bu cmdlet 'in kaldırdığı ortak IP adresinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4da02-118">Specifies the name of the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4da02-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="4da02-119">-PassThru</span></span>
<span data-ttu-id="4da02-120">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="4da02-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4da02-121">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="4da02-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4da02-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4da02-122">-ResourceGroupName</span></span>
<span data-ttu-id="4da02-123">Bu cmdlet 'in kaldırıldığı ortak IP adresini içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4da02-123">Specifies the name of the resource group that contains the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4da02-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="4da02-124">-Confirm</span></span>
<span data-ttu-id="4da02-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4da02-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4da02-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4da02-126">-WhatIf</span></span>
<span data-ttu-id="4da02-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4da02-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4da02-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4da02-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4da02-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4da02-129">CommonParameters</span></span>
<span data-ttu-id="4da02-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4da02-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4da02-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4da02-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4da02-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4da02-132">INPUTS</span></span>

## <span data-ttu-id="4da02-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4da02-133">OUTPUTS</span></span>

## <span data-ttu-id="4da02-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4da02-134">NOTES</span></span>

## <span data-ttu-id="4da02-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4da02-135">RELATED LINKS</span></span>

[<span data-ttu-id="4da02-136">Get-Azpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="4da02-136">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="4da02-137">New-Azpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="4da02-137">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="4da02-138">Set-Azpublicıpadresi</span><span class="sxs-lookup"><span data-stu-id="4da02-138">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)


