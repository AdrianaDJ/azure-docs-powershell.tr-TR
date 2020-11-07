---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 00236BC2-61D8-49C2-91BE-923C567153F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpAddress.md
ms.openlocfilehash: e4392b609081bb320e508de75319c9d50af12cae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932257"
---
# <span data-ttu-id="6e840-101">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="6e840-101">Remove-AzPublicIpAddress</span></span>

## <span data-ttu-id="6e840-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e840-102">SYNOPSIS</span></span>
<span data-ttu-id="6e840-103">Genel IP adresini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6e840-103">Removes a public IP address.</span></span>

## <span data-ttu-id="6e840-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6e840-104">SYNTAX</span></span>

```
Remove-AzPublicIpAddress -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e840-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6e840-105">DESCRIPTION</span></span>
<span data-ttu-id="6e840-106">**Remove-Azpublicıpaddress** cmdlet 'ı bir Azure genel IP adresini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6e840-106">The **Remove-AzPublicIpAddress** cmdlet removes an Azure public IP address.</span></span>

## <span data-ttu-id="6e840-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6e840-107">EXAMPLES</span></span>

### <span data-ttu-id="6e840-108">1: genel IP adresi kaynağını kaldırma</span><span class="sxs-lookup"><span data-stu-id="6e840-108">1: Remove a public IP address resource</span></span>
```
Remove-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="6e840-109">Bu komut, kaynak grubundaki $publicIpName adlı ortak IP adresi kaynağını kaldırır $rgName.</span><span class="sxs-lookup"><span data-stu-id="6e840-109">This command removes the public IP address resource named $publicIpName in the resource group $rgName.</span></span>

## <span data-ttu-id="6e840-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6e840-110">PARAMETERS</span></span>

### <span data-ttu-id="6e840-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="6e840-111">-AsJob</span></span>
<span data-ttu-id="6e840-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="6e840-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6e840-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e840-113">-DefaultProfile</span></span>
<span data-ttu-id="6e840-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6e840-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e840-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6e840-115">-Force</span></span>
<span data-ttu-id="6e840-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="6e840-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6e840-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="6e840-117">-Name</span></span>
<span data-ttu-id="6e840-118">Bu cmdlet 'in kaldırdığı ortak IP adresinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6e840-118">Specifies the name of the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6e840-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="6e840-119">-PassThru</span></span>
<span data-ttu-id="6e840-120">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="6e840-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6e840-121">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="6e840-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6e840-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e840-122">-ResourceGroupName</span></span>
<span data-ttu-id="6e840-123">Bu cmdlet 'in kaldırıldığı ortak IP adresini içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6e840-123">Specifies the name of the resource group that contains the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6e840-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="6e840-124">-Confirm</span></span>
<span data-ttu-id="6e840-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6e840-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e840-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e840-126">-WhatIf</span></span>
<span data-ttu-id="6e840-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6e840-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e840-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6e840-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e840-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e840-129">CommonParameters</span></span>
<span data-ttu-id="6e840-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6e840-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e840-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e840-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e840-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6e840-132">INPUTS</span></span>

### <span data-ttu-id="6e840-133">System. String</span><span class="sxs-lookup"><span data-stu-id="6e840-133">System.String</span></span>

## <span data-ttu-id="6e840-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6e840-134">OUTPUTS</span></span>

### <span data-ttu-id="6e840-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6e840-135">System.Boolean</span></span>

## <span data-ttu-id="6e840-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6e840-136">NOTES</span></span>

## <span data-ttu-id="6e840-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6e840-137">RELATED LINKS</span></span>

[<span data-ttu-id="6e840-138">Get-Azpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="6e840-138">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="6e840-139">New-Azpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="6e840-139">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="6e840-140">Set-Azpublicıpadresi</span><span class="sxs-lookup"><span data-stu-id="6e840-140">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)


