---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 00236BC2-61D8-49C2-91BE-923C567153F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpAddress.md
ms.openlocfilehash: 8d3c71d1cf4df9483f379d8a689597a1a10c7ce7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267020"
---
# <span data-ttu-id="d4d56-101">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d4d56-101">Remove-AzPublicIpAddress</span></span>

## <span data-ttu-id="d4d56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4d56-102">SYNOPSIS</span></span>
<span data-ttu-id="d4d56-103">Genel IP adresini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d4d56-103">Removes a public IP address.</span></span>

## <span data-ttu-id="d4d56-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d4d56-104">SYNTAX</span></span>

```
Remove-AzPublicIpAddress -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4d56-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d4d56-105">DESCRIPTION</span></span>
<span data-ttu-id="d4d56-106">**Remove-Azpublicıpaddress** cmdlet 'ı bir Azure genel IP adresini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d4d56-106">The **Remove-AzPublicIpAddress** cmdlet removes an Azure public IP address.</span></span>

## <span data-ttu-id="d4d56-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d4d56-107">EXAMPLES</span></span>

### <span data-ttu-id="d4d56-108">1: genel IP adresi kaynağını kaldırma</span><span class="sxs-lookup"><span data-stu-id="d4d56-108">1: Remove a public IP address resource</span></span>
```
Remove-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="d4d56-109">Bu komut, kaynak grubundaki $publicIpName adlı ortak IP adresi kaynağını kaldırır $rgName.</span><span class="sxs-lookup"><span data-stu-id="d4d56-109">This command removes the public IP address resource named $publicIpName in the resource group $rgName.</span></span>

## <span data-ttu-id="d4d56-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d4d56-110">PARAMETERS</span></span>

### <span data-ttu-id="d4d56-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="d4d56-111">-AsJob</span></span>
<span data-ttu-id="d4d56-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="d4d56-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d4d56-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4d56-113">-DefaultProfile</span></span>
<span data-ttu-id="d4d56-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d4d56-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4d56-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d4d56-115">-Force</span></span>
<span data-ttu-id="d4d56-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="d4d56-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d4d56-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="d4d56-117">-Name</span></span>
<span data-ttu-id="d4d56-118">Bu cmdlet 'in kaldırdığı ortak IP adresinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4d56-118">Specifies the name of the public IP address that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4d56-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d4d56-119">-PassThru</span></span>
<span data-ttu-id="d4d56-120">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="d4d56-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d4d56-121">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="d4d56-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d4d56-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4d56-122">-ResourceGroupName</span></span>
<span data-ttu-id="d4d56-123">Bu cmdlet 'in kaldırıldığı ortak IP adresini içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4d56-123">Specifies the name of the resource group that contains the public IP address that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4d56-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="d4d56-124">-Confirm</span></span>
<span data-ttu-id="d4d56-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d4d56-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4d56-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4d56-126">-WhatIf</span></span>
<span data-ttu-id="d4d56-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d4d56-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4d56-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d4d56-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4d56-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4d56-129">CommonParameters</span></span>
<span data-ttu-id="d4d56-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d4d56-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4d56-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4d56-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4d56-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d4d56-132">INPUTS</span></span>

### <span data-ttu-id="d4d56-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d4d56-133">System.String</span></span>

## <span data-ttu-id="d4d56-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d4d56-134">OUTPUTS</span></span>

### <span data-ttu-id="d4d56-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d4d56-135">System.Boolean</span></span>

## <span data-ttu-id="d4d56-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d4d56-136">NOTES</span></span>

## <span data-ttu-id="d4d56-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d4d56-137">RELATED LINKS</span></span>

[<span data-ttu-id="d4d56-138">Get-Azpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="d4d56-138">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="d4d56-139">New-Azpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="d4d56-139">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="d4d56-140">Set-Azpublicıpadresi</span><span class="sxs-lookup"><span data-stu-id="d4d56-140">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)


