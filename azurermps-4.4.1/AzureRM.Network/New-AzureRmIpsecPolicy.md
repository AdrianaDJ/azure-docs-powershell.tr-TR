---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmIpsecPolicy.md
ms.openlocfilehash: 17b24668d497cd8d4405865d40f2969219ede719
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593524"
---
# <span data-ttu-id="2d59f-101">New-AzureRmIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="2d59f-101">New-AzureRmIpsecPolicy</span></span>

## <span data-ttu-id="2d59f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d59f-102">SYNOPSIS</span></span>
<span data-ttu-id="2d59f-103">IPSec Ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2d59f-103">Creates an IPSec Policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d59f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2d59f-104">SYNTAX</span></span>

```
New-AzureRmIpsecPolicy [-SALifeTimeSeconds <Int32>] [-SADataSizeKilobytes <Int32>] -IpsecEncryption <String>
 -IpsecIntegrity <String> -IkeEncryption <String> -IkeIntegrity <String> -DhGroup <String> -PfsGroup <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d59f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2d59f-105">DESCRIPTION</span></span>
<span data-ttu-id="2d59f-106">New-AzureRmIpsecPolicy cmdlet 'i sanal ağ geçidi bağlantısında kullanılacak bir IPSec ilkesi teklifi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2d59f-106">The New-AzureRmIpsecPolicy cmdlet creates an IPSec policy proposal to be used in a virtual network gateway connection.</span></span>

## <span data-ttu-id="2d59f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2d59f-107">EXAMPLES</span></span>

### <span data-ttu-id="2d59f-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2d59f-108">Example 1</span></span>
```
PS C:\> $ipsecPolicy = New-AzureRmIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName $rgname -name $vnetConnectionName -location $location -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -RoutingWeight 3 -SharedKey $sharedKey -UsePolicyBasedTrafficSelectors $true -IpsecPolicies $ipsecPolicy
```

<span data-ttu-id="2d59f-109">Yeni sanal ağ geçidi bağlantısında kullanılacak bir IPSec ilkesi oluşturma.</span><span class="sxs-lookup"><span data-stu-id="2d59f-109">Creating an IPSec policy to be used for a new virtual network gateway connection.</span></span>

## <span data-ttu-id="2d59f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2d59f-110">PARAMETERS</span></span>

### <span data-ttu-id="2d59f-111">-Dhgrup</span><span class="sxs-lookup"><span data-stu-id="2d59f-111">-DhGroup</span></span>
<span data-ttu-id="2d59f-112">İlk SA için ıKE Aşama 1 ' de kullanılan DH grupları</span><span class="sxs-lookup"><span data-stu-id="2d59f-112">The DH Groups used in IKE Phase 1 for initial SA</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: None, DHGroup1, DHGroup14, DHGroup2, DHGroup2048, DHGroup24, ECP256, ECP384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d59f-113">-Ikeencryption</span><span class="sxs-lookup"><span data-stu-id="2d59f-113">-IkeEncryption</span></span>
<span data-ttu-id="2d59f-114">IKE şifreleme algoritması (ıKE Phase 2)</span><span class="sxs-lookup"><span data-stu-id="2d59f-114">The IKE encryption algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: DES, DES3, AES128, AES192, AES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d59f-115">-Ikeıntegrity</span><span class="sxs-lookup"><span data-stu-id="2d59f-115">-IkeIntegrity</span></span>
<span data-ttu-id="2d59f-116">IKE bütünlük algoritması (ıKE Phase 2)</span><span class="sxs-lookup"><span data-stu-id="2d59f-116">The IKE integrity algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: MD5, SHA1, SHA256, SHA384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d59f-117">-Ipsecencryption</span><span class="sxs-lookup"><span data-stu-id="2d59f-117">-IpsecEncryption</span></span>
<span data-ttu-id="2d59f-118">IPSec şifreleme algoritması (ıKE Aşama 1)</span><span class="sxs-lookup"><span data-stu-id="2d59f-118">The IPSec encryption algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: None, DES, DES3, AES128, AES192, AES256, GCMAES128, GCMAES192, GCMAES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d59f-119">-Ipsecıntegrity</span><span class="sxs-lookup"><span data-stu-id="2d59f-119">-IpsecIntegrity</span></span>
<span data-ttu-id="2d59f-120">IPSec bütünlük algoritması (ıKE Aşama 1)</span><span class="sxs-lookup"><span data-stu-id="2d59f-120">The IPSec integrity algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: MD5, SHA1, SHA256, GCMAES128, GCMAES192, GCMAES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d59f-121">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="2d59f-121">-PfsGroup</span></span>
<span data-ttu-id="2d59f-122">Yeni alt SA için ıKE aşama 2 ' de kullanılan DH grupları</span><span class="sxs-lookup"><span data-stu-id="2d59f-122">The DH Groups used in IKE Phase 2 for new child SA</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: None, PFS1, PFS2, PFS2048, PFS24, ECP256, ECP384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d59f-123">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="2d59f-123">-SADataSizeKilobytes</span></span>
<span data-ttu-id="2d59f-124">KB cinsinden IPSec güvenlik Ilişkisi (hızlı mod veya Aşama 2 SA) yük boyutu</span><span class="sxs-lookup"><span data-stu-id="2d59f-124">The IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d59f-125">-SALifeTimeSeconds</span><span class="sxs-lookup"><span data-stu-id="2d59f-125">-SALifeTimeSeconds</span></span>
<span data-ttu-id="2d59f-126">IPSec güvenlik Ilişkisi (hızlı mod veya Aşama 2 SA) saniye cinsinden yaşam süresi</span><span class="sxs-lookup"><span data-stu-id="2d59f-126">The IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d59f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d59f-127">-DefaultProfile</span></span>
<span data-ttu-id="2d59f-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2d59f-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d59f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d59f-129">CommonParameters</span></span>
<span data-ttu-id="2d59f-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2d59f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d59f-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d59f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d59f-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2d59f-132">INPUTS</span></span>

### <span data-ttu-id="2d59f-133">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2d59f-133">None</span></span>

## <span data-ttu-id="2d59f-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2d59f-134">OUTPUTS</span></span>

### <span data-ttu-id="2d59f-135">Microsoft. Azure. Commands. Network. model. PSIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="2d59f-135">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="2d59f-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2d59f-136">NOTES</span></span>

## <span data-ttu-id="2d59f-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2d59f-137">RELATED LINKS</span></span>

