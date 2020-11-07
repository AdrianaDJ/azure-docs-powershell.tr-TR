---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzPublicIpAddress.md
ms.openlocfilehash: 53d5e15e6354e359461e59728e0776b7d3ec99ea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936516"
---
# <span data-ttu-id="28d97-101">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="28d97-101">Set-AzPublicIpAddress</span></span>

## <span data-ttu-id="28d97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28d97-102">SYNOPSIS</span></span>
<span data-ttu-id="28d97-103">Genel bir IP adresi için hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="28d97-103">Sets the goal state for a public IP address.</span></span>

## <span data-ttu-id="28d97-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="28d97-104">SYNTAX</span></span>

```
Set-AzPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28d97-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="28d97-105">DESCRIPTION</span></span>
<span data-ttu-id="28d97-106">**Set-Azpublicıpaddress** cmdlet 'i, genel bir IP adresinin hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="28d97-106">The **Set-AzPublicIpAddress** cmdlet sets the goal state for a public IP address.</span></span>

## <span data-ttu-id="28d97-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="28d97-107">EXAMPLES</span></span>

### <span data-ttu-id="28d97-108">1: genel IP adresinin ayırma yöntemini değiştirme</span><span class="sxs-lookup"><span data-stu-id="28d97-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Dynamic"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="28d97-109">İlk komut, kaynak grubundaki $rgName adı $publicIPName olan genel IP adresi kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="28d97-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="28d97-110">İkinci komut ortak IP adresi nesnesinin ayırma yöntemini "statik" olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="28d97-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="28d97-111">Set-AzPublicIPAddress komut ortak IP adresi kaynağını güncelleştirilmiş nesneyle güncelleştirir ve tahsisat yöntemini ' statik ' olarak değiştirir.</span><span class="sxs-lookup"><span data-stu-id="28d97-111">Set-AzPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="28d97-112">Genel bir IP adresi hemen tahsis edildi.</span><span class="sxs-lookup"><span data-stu-id="28d97-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="28d97-113">2: genel IP adresinin DNS etki alanı etiketini değiştirme</span><span class="sxs-lookup"><span data-stu-id="28d97-113">2: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="28d97-114">İlk komut, kaynak grubundaki $rgName adı $publicIPName olan genel IP adresi kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="28d97-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="28d97-115">İkinci komut, DomainNameLabel özelliğini gerekli DNS önekine ayarlar.</span><span class="sxs-lookup"><span data-stu-id="28d97-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="28d97-116">Set-AzPublicIPAddress komut ortak IP adresi kaynağını güncelleştirilmiş nesneyle güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="28d97-116">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="28d97-117">DomainNameLabel & FQDN beklendiği gibi değiştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="28d97-117">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="28d97-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="28d97-118">PARAMETERS</span></span>

### <span data-ttu-id="28d97-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="28d97-119">-AsJob</span></span>
<span data-ttu-id="28d97-120">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="28d97-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="28d97-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28d97-121">-DefaultProfile</span></span>
<span data-ttu-id="28d97-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="28d97-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28d97-123">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="28d97-123">-PublicIpAddress</span></span>
<span data-ttu-id="28d97-124">Genel IP adresinin ayarlanması gereken hedef durumu temsil eden **Publicıpaddress** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="28d97-124">Specifies a **PublicIpAddress** object that represents the goal state to which the public IP address should be set.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28d97-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28d97-125">CommonParameters</span></span>
<span data-ttu-id="28d97-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="28d97-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28d97-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28d97-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28d97-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="28d97-128">INPUTS</span></span>

### <span data-ttu-id="28d97-129">Pspublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="28d97-129">PSPublicIpAddress</span></span>
<span data-ttu-id="28d97-130">' Publicıpaddress ' parametresi ardışık düzenin ' Pspublicıpaddress ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="28d97-130">Parameter 'PublicIpAddress' accepts value of type 'PSPublicIpAddress' from the pipeline</span></span>

## <span data-ttu-id="28d97-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="28d97-131">OUTPUTS</span></span>

### <span data-ttu-id="28d97-132">Microsoft. Azure. Commands. Network. model. Pspublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="28d97-132">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="28d97-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="28d97-133">NOTES</span></span>

## <span data-ttu-id="28d97-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="28d97-134">RELATED LINKS</span></span>

[<span data-ttu-id="28d97-135">Get-Azpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="28d97-135">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="28d97-136">New-Azpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="28d97-136">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="28d97-137">Remove-Azpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="28d97-137">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)


