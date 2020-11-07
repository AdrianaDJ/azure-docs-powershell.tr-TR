---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
ms.openlocfilehash: cc2ef6f016047bd20beba1671129a15c3dfa06f6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932754"
---
# <span data-ttu-id="fda9a-101">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="fda9a-101">Set-AzPublicIpAddress</span></span>

## <span data-ttu-id="fda9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fda9a-102">SYNOPSIS</span></span>
<span data-ttu-id="fda9a-103">Genel bir IP adresini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="fda9a-103">Updates a public IP address.</span></span>

## <span data-ttu-id="fda9a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fda9a-104">SYNTAX</span></span>

```
Set-AzPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fda9a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fda9a-105">DESCRIPTION</span></span>
<span data-ttu-id="fda9a-106">**Set-Azpublicıpaddress** cmdlet 'i ortak bir IP adresini günceller.</span><span class="sxs-lookup"><span data-stu-id="fda9a-106">The **Set-AzPublicIpAddress** cmdlet updates a public IP address.</span></span>

## <span data-ttu-id="fda9a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fda9a-107">EXAMPLES</span></span>

### <span data-ttu-id="fda9a-108">1: genel IP adresinin ayırma yöntemini değiştirme</span><span class="sxs-lookup"><span data-stu-id="fda9a-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Static"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="fda9a-109">İlk komut, kaynak grubundaki $rgName adı $publicIPName olan genel IP adresi kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="fda9a-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="fda9a-110">İkinci komut ortak IP adresi nesnesinin ayırma yöntemini "statik" olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="fda9a-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="fda9a-111">Set-AzPublicIPAddress komut ortak IP adresi kaynağını güncelleştirilmiş nesneyle güncelleştirir ve tahsisat yöntemini ' statik ' olarak değiştirir.</span><span class="sxs-lookup"><span data-stu-id="fda9a-111">Set-AzPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="fda9a-112">Genel bir IP adresi hemen tahsis edildi.</span><span class="sxs-lookup"><span data-stu-id="fda9a-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="fda9a-113">2: genel IP adresinin DNS etki alanı etiketini değiştirme</span><span class="sxs-lookup"><span data-stu-id="fda9a-113">2: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="fda9a-114">İlk komut, kaynak grubundaki $rgName adı $publicIPName olan genel IP adresi kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="fda9a-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="fda9a-115">İkinci komut, DomainNameLabel özelliğini gerekli DNS önekine ayarlar.</span><span class="sxs-lookup"><span data-stu-id="fda9a-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="fda9a-116">Set-AzPublicIPAddress komut ortak IP adresi kaynağını güncelleştirilmiş nesneyle güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="fda9a-116">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="fda9a-117">DomainNameLabel & FQDN beklendiği gibi değiştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="fda9a-117">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="fda9a-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fda9a-118">PARAMETERS</span></span>

### <span data-ttu-id="fda9a-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="fda9a-119">-AsJob</span></span>
<span data-ttu-id="fda9a-120">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="fda9a-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fda9a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fda9a-121">-DefaultProfile</span></span>
<span data-ttu-id="fda9a-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fda9a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fda9a-123">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="fda9a-123">-PublicIpAddress</span></span>
<span data-ttu-id="fda9a-124">Genel IP adresinin ayarlanması gereken durumu temsil eden genel IP adresi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fda9a-124">Specifies a public IP address object representing the state to which the public IP address should be set.</span></span>

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

### <span data-ttu-id="fda9a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fda9a-125">CommonParameters</span></span>
<span data-ttu-id="fda9a-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fda9a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fda9a-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fda9a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fda9a-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fda9a-128">INPUTS</span></span>

### <span data-ttu-id="fda9a-129">Microsoft. Azure. Commands. Network. model. Pspublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="fda9a-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="fda9a-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fda9a-130">OUTPUTS</span></span>

### <span data-ttu-id="fda9a-131">Microsoft. Azure. Commands. Network. model. Pspublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="fda9a-131">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="fda9a-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fda9a-132">NOTES</span></span>

## <span data-ttu-id="fda9a-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fda9a-133">RELATED LINKS</span></span>

[<span data-ttu-id="fda9a-134">Get-Azpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="fda9a-134">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="fda9a-135">New-Azpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="fda9a-135">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="fda9a-136">Remove-Azpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="fda9a-136">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)


