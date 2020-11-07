---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpAddress.md
ms.openlocfilehash: 1460b4497909d56e2d10d03e33df71518c52b796
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762430"
---
# <span data-ttu-id="c03a4-101">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c03a4-101">Set-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="c03a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c03a4-102">SYNOPSIS</span></span>
<span data-ttu-id="c03a4-103">Genel bir IP adresi için hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c03a4-103">Sets the goal state for a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c03a4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c03a4-104">SYNTAX</span></span>

```
Set-AzureRmPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c03a4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c03a4-105">DESCRIPTION</span></span>
<span data-ttu-id="c03a4-106">**Set-Azurermpublicıpaddress** cmdlet 'ı ortak IP adresi için hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c03a4-106">The **Set-AzureRmPublicIpAddress** cmdlet sets the goal state for a public IP address.</span></span>

## <span data-ttu-id="c03a4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c03a4-107">EXAMPLES</span></span>

### <span data-ttu-id="c03a4-108">1: genel IP adresinin ayırma yöntemini değiştirme</span><span class="sxs-lookup"><span data-stu-id="c03a4-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Dynamic"
    
PS C:\> Set-AzureRmPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="c03a4-109">İlk komut, kaynak grubundaki $rgName adı $publicIPName olan genel IP adresi kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="c03a4-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="c03a4-110">İkinci komut ortak IP adresi nesnesinin ayırma yöntemini "statik" olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c03a4-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="c03a4-111">Set-AzureRmPublicIPAddress komut ortak IP adresi kaynağını güncelleştirilmiş nesneyle güncelleştirir ve tahsisat yöntemini ' statik ' olarak değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c03a4-111">Set-AzureRmPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="c03a4-112">Genel bir IP adresi hemen tahsis edildi.</span><span class="sxs-lookup"><span data-stu-id="c03a4-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="c03a4-113">2: genel IP adresinin DNS etki alanı etiketini değiştirme</span><span class="sxs-lookup"><span data-stu-id="c03a4-113">2: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzureRmPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="c03a4-114">İlk komut, kaynak grubundaki $rgName adı $publicIPName olan genel IP adresi kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="c03a4-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="c03a4-115">İkinci komut, DomainNameLabel özelliğini gerekli DNS önekine ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c03a4-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="c03a4-116">Set-AzureRmPublicIPAddress komut ortak IP adresi kaynağını güncelleştirilmiş nesneyle güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c03a4-116">Set-AzureRmPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="c03a4-117">DomainNameLabel & FQDN beklendiği gibi değiştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="c03a4-117">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="c03a4-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c03a4-118">PARAMETERS</span></span>

### <span data-ttu-id="c03a4-119">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="c03a4-119">-PublicIpAddress</span></span>
<span data-ttu-id="c03a4-120">Genel IP adresinin ayarlanması gereken hedef durumu temsil eden **Publicıpaddress** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c03a4-120">Specifies a **PublicIpAddress** object that represents the goal state to which the public IP address should be set.</span></span>

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

### <span data-ttu-id="c03a4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c03a4-121">-DefaultProfile</span></span>
<span data-ttu-id="c03a4-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c03a4-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c03a4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c03a4-123">CommonParameters</span></span>
<span data-ttu-id="c03a4-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c03a4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c03a4-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c03a4-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c03a4-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c03a4-126">INPUTS</span></span>

### <span data-ttu-id="c03a4-127">Pspublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="c03a4-127">PSPublicIpAddress</span></span>
<span data-ttu-id="c03a4-128">' Publicıpaddress ' parametresi ardışık düzenin ' Pspublicıpaddress ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="c03a4-128">Parameter 'PublicIpAddress' accepts value of type 'PSPublicIpAddress' from the pipeline</span></span>

## <span data-ttu-id="c03a4-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c03a4-129">OUTPUTS</span></span>

### <span data-ttu-id="c03a4-130">Microsoft. Azure. Commands. Network. model. Pspublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="c03a4-130">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="c03a4-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c03a4-131">NOTES</span></span>

## <span data-ttu-id="c03a4-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c03a4-132">RELATED LINKS</span></span>

[<span data-ttu-id="c03a4-133">Get-Azurermpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="c03a4-133">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="c03a4-134">Get-Azurermpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="c03a4-134">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="c03a4-135">Yeni-Azurermpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="c03a4-135">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="c03a4-136">Remove-Azurermpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="c03a4-136">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)


