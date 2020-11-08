---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
ms.openlocfilehash: 4cb7d3a48d1783e834b9ecdd53d86969b4e1e6cb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274323"
---
# <span data-ttu-id="34295-101">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="34295-101">Set-AzPublicIpAddress</span></span>

## <span data-ttu-id="34295-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34295-102">SYNOPSIS</span></span>
<span data-ttu-id="34295-103">Genel bir IP adresini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="34295-103">Updates a public IP address.</span></span>

## <span data-ttu-id="34295-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="34295-104">SYNTAX</span></span>

```
Set-AzPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="34295-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="34295-105">DESCRIPTION</span></span>
<span data-ttu-id="34295-106">**Set-Azpublicıpaddress** cmdlet 'i ortak bir IP adresini günceller.</span><span class="sxs-lookup"><span data-stu-id="34295-106">The **Set-AzPublicIpAddress** cmdlet updates a public IP address.</span></span>

## <span data-ttu-id="34295-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="34295-107">EXAMPLES</span></span>

### <span data-ttu-id="34295-108">1: genel IP adresinin ayırma yöntemini değiştirme</span><span class="sxs-lookup"><span data-stu-id="34295-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Static"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="34295-109">İlk komut, kaynak grubundaki $rgName adı $publicIPName olan genel IP adresi kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="34295-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="34295-110">İkinci komut ortak IP adresi nesnesinin ayırma yöntemini "statik" olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="34295-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="34295-111">Set-AzPublicIPAddress komut ortak IP adresi kaynağını güncelleştirilmiş nesneyle güncelleştirir ve tahsisat yöntemini ' statik ' olarak değiştirir.</span><span class="sxs-lookup"><span data-stu-id="34295-111">Set-AzPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="34295-112">Genel bir IP adresi hemen tahsis edildi.</span><span class="sxs-lookup"><span data-stu-id="34295-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="34295-113">2: genel IP adresinin DNS etki alanı etiketini ekleme</span><span class="sxs-lookup"><span data-stu-id="34295-113">2: Add DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings = @{"DomainNameLabel" = "newdnsprefix"}
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="34295-114">İlk komut, kaynak grubundaki $rgName adı $publicIPName olan genel IP adresi kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="34295-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="34295-115">İkinci komut, DomainNameLabel özelliğini gerekli DNS önekine ayarlar.</span><span class="sxs-lookup"><span data-stu-id="34295-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="34295-116">Set-AzPublicIPAddress komut ortak IP adresi kaynağını güncelleştirilmiş nesneyle güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="34295-116">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="34295-117">DomainNameLabel & FQDN beklendiği gibi değiştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="34295-117">DomainNameLabel & Fqdn are modified as expected.</span></span>
    
### <span data-ttu-id="34295-118">3: genel IP adresinin DNS etki alanı etiketini değiştirme</span><span class="sxs-lookup"><span data-stu-id="34295-118">3: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="34295-119">İlk komut, kaynak grubundaki $rgName adı $publicIPName olan genel IP adresi kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="34295-119">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="34295-120">İkinci komut, DomainNameLabel özelliğini gerekli DNS önekine ayarlar.</span><span class="sxs-lookup"><span data-stu-id="34295-120">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="34295-121">Set-AzPublicIPAddress komut ortak IP adresi kaynağını güncelleştirilmiş nesneyle güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="34295-121">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="34295-122">DomainNameLabel & FQDN beklendiği gibi değiştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="34295-122">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="34295-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="34295-123">PARAMETERS</span></span>

### <span data-ttu-id="34295-124">-Iş</span><span class="sxs-lookup"><span data-stu-id="34295-124">-AsJob</span></span>
<span data-ttu-id="34295-125">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="34295-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="34295-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34295-126">-DefaultProfile</span></span>
<span data-ttu-id="34295-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="34295-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34295-128">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="34295-128">-PublicIpAddress</span></span>
<span data-ttu-id="34295-129">Genel IP adresinin ayarlanması gereken durumu temsil eden genel IP adresi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="34295-129">Specifies a public IP address object representing the state to which the public IP address should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34295-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34295-130">CommonParameters</span></span>
<span data-ttu-id="34295-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="34295-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34295-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34295-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34295-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="34295-133">INPUTS</span></span>

### <span data-ttu-id="34295-134">Microsoft. Azure. Commands. Network. model. Pspublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="34295-134">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="34295-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="34295-135">OUTPUTS</span></span>

### <span data-ttu-id="34295-136">Microsoft. Azure. Commands. Network. model. Pspublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="34295-136">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="34295-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="34295-137">NOTES</span></span>

## <span data-ttu-id="34295-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="34295-138">RELATED LINKS</span></span>

[<span data-ttu-id="34295-139">Get-Azpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="34295-139">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="34295-140">New-Azpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="34295-140">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="34295-141">Remove-Azpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="34295-141">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)


