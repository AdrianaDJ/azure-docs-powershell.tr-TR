---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpAddress.md
ms.openlocfilehash: ed3b2de22c5f71c0782724f99c8325de4dea98b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589420"
---
# <span data-ttu-id="7a6b0-101">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7a6b0-101">Set-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="7a6b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a6b0-102">SYNOPSIS</span></span>
<span data-ttu-id="7a6b0-103">Genel bir IP adresi için hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7a6b0-103">Sets the goal state for a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a6b0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7a6b0-104">SYNTAX</span></span>

```
Set-AzureRmPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a6b0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7a6b0-105">DESCRIPTION</span></span>
<span data-ttu-id="7a6b0-106">**Set-Azurermpublicıpaddress** cmdlet 'ı ortak IP adresi için hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7a6b0-106">The **Set-AzureRmPublicIpAddress** cmdlet sets the goal state for a public IP address.</span></span>

## <span data-ttu-id="7a6b0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7a6b0-107">EXAMPLES</span></span>

### <span data-ttu-id="7a6b0-108">1: genel IP adresinin ayırma yöntemini değiştirme</span><span class="sxs-lookup"><span data-stu-id="7a6b0-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Static"
    
PS C:\> Set-AzureRmPublicIpAddress -PublicIpAddress $publicIp

PS C:\> Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="7a6b0-109">İlk komut, kaynak grubundaki $rgName adı $publicIPName olan genel IP adresi kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="7a6b0-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="7a6b0-110">İkinci komut ortak IP adresi nesnesinin ayırma yöntemini "statik" olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7a6b0-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="7a6b0-111">Set-AzureRmPublicIPAddress komut ortak IP adresi kaynağını güncelleştirilmiş nesneyle güncelleştirir ve tahsisat yöntemini ' statik ' olarak değiştirir.</span><span class="sxs-lookup"><span data-stu-id="7a6b0-111">Set-AzureRmPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="7a6b0-112">Genel bir IP adresi hemen tahsis edildi.</span><span class="sxs-lookup"><span data-stu-id="7a6b0-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="7a6b0-113">2: genel IP adresinin DNS etki alanı etiketini değiştirme</span><span class="sxs-lookup"><span data-stu-id="7a6b0-113">2: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzureRmPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="7a6b0-114">İlk komut, kaynak grubundaki $rgName adı $publicIPName olan genel IP adresi kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="7a6b0-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="7a6b0-115">İkinci komut, DomainNameLabel özelliğini gerekli DNS önekine ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7a6b0-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="7a6b0-116">Set-AzureRmPublicIPAddress komut ortak IP adresi kaynağını güncelleştirilmiş nesneyle güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="7a6b0-116">Set-AzureRmPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="7a6b0-117">DomainNameLabel & FQDN beklendiği gibi değiştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="7a6b0-117">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="7a6b0-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7a6b0-118">PARAMETERS</span></span>

### <span data-ttu-id="7a6b0-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="7a6b0-119">-AsJob</span></span>
<span data-ttu-id="7a6b0-120">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="7a6b0-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7a6b0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a6b0-121">-DefaultProfile</span></span>
<span data-ttu-id="7a6b0-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7a6b0-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a6b0-123">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="7a6b0-123">-PublicIpAddress</span></span>
<span data-ttu-id="7a6b0-124">Genel IP adresinin ayarlanması gereken hedef durumu temsil eden **Publicıpaddress** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a6b0-124">Specifies a **PublicIpAddress** object that represents the goal state to which the public IP address should be set.</span></span>

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

### <span data-ttu-id="7a6b0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a6b0-125">CommonParameters</span></span>
<span data-ttu-id="7a6b0-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7a6b0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a6b0-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a6b0-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a6b0-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7a6b0-128">INPUTS</span></span>

### <span data-ttu-id="7a6b0-129">Microsoft. Azure. Commands. Network. model. Pspublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="7a6b0-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>
<span data-ttu-id="7a6b0-130">Parametreler: Publicıpaddress (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7a6b0-130">Parameters: PublicIpAddress (ByValue)</span></span>

## <span data-ttu-id="7a6b0-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7a6b0-131">OUTPUTS</span></span>

### <span data-ttu-id="7a6b0-132">Microsoft. Azure. Commands. Network. model. Pspublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="7a6b0-132">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="7a6b0-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7a6b0-133">NOTES</span></span>

## <span data-ttu-id="7a6b0-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7a6b0-134">RELATED LINKS</span></span>

[<span data-ttu-id="7a6b0-135">Get-Azurermpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="7a6b0-135">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="7a6b0-136">Yeni-Azurermpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="7a6b0-136">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="7a6b0-137">Remove-Azurermpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="7a6b0-137">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)


