---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 00236BC2-61D8-49C2-91BE-923C567153F3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmPublicIpAddress.md
ms.openlocfilehash: 396f603c4a4126b8d438f0048677da7a5dbd7492
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590726"
---
# <span data-ttu-id="72302-101">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="72302-101">Remove-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="72302-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72302-102">SYNOPSIS</span></span>
<span data-ttu-id="72302-103">Genel IP adresini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="72302-103">Removes a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72302-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="72302-104">SYNTAX</span></span>

```
Remove-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72302-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="72302-105">DESCRIPTION</span></span>
<span data-ttu-id="72302-106">**Remove-Azurermpublicıpaddress** cmdlet 'ı bir Azure genel IP adresini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="72302-106">The **Remove-AzureRmPublicIpAddress** cmdlet removes an Azure public IP address.</span></span>

## <span data-ttu-id="72302-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="72302-107">EXAMPLES</span></span>

### <span data-ttu-id="72302-108">1: genel IP adresi kaynağını kaldırma</span><span class="sxs-lookup"><span data-stu-id="72302-108">1: Remove a public IP address resource</span></span>
```
Remove-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="72302-109">Bu komut, kaynak grubundaki $publicIpName adlı ortak IP adresi kaynağını kaldırır $rgName.</span><span class="sxs-lookup"><span data-stu-id="72302-109">This command removes the public IP address resource named $publicIpName in the resource group $rgName.</span></span>

## <span data-ttu-id="72302-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="72302-110">PARAMETERS</span></span>

### <span data-ttu-id="72302-111">-Force</span><span class="sxs-lookup"><span data-stu-id="72302-111">-Force</span></span>
<span data-ttu-id="72302-112">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="72302-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="72302-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="72302-113">-Name</span></span>
<span data-ttu-id="72302-114">Bu cmdlet 'in kaldırdığı ortak IP adresinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="72302-114">Specifies the name of the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="72302-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="72302-115">-PassThru</span></span>
<span data-ttu-id="72302-116">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="72302-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="72302-117">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="72302-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="72302-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72302-118">-ResourceGroupName</span></span>
<span data-ttu-id="72302-119">Bu cmdlet 'in kaldırıldığı ortak IP adresini içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="72302-119">Specifies the name of the resource group that contains the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="72302-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="72302-120">-Confirm</span></span>
<span data-ttu-id="72302-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="72302-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72302-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72302-122">-WhatIf</span></span>
<span data-ttu-id="72302-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="72302-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72302-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="72302-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72302-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72302-125">-DefaultProfile</span></span>
<span data-ttu-id="72302-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="72302-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72302-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72302-127">CommonParameters</span></span>
<span data-ttu-id="72302-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="72302-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72302-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72302-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72302-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="72302-130">INPUTS</span></span>

## <span data-ttu-id="72302-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="72302-131">OUTPUTS</span></span>

## <span data-ttu-id="72302-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="72302-132">NOTES</span></span>

## <span data-ttu-id="72302-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="72302-133">RELATED LINKS</span></span>

[<span data-ttu-id="72302-134">Get-Azurermpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="72302-134">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="72302-135">Yeni-Azurermpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="72302-135">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="72302-136">Set-Azurermpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="72302-136">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)


