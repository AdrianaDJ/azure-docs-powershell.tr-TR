---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermipsecpolicy
schema: 2.0.0
ms.openlocfilehash: 642284e7e1aa732983ee660ea323707be030b640
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939290"
---
# <span data-ttu-id="342dc-101">New-AzureRmIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="342dc-101">New-AzureRmIpsecPolicy</span></span>

## <span data-ttu-id="342dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="342dc-102">SYNOPSIS</span></span>
<span data-ttu-id="342dc-103">IPSec Ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="342dc-103">Creates an IPSec Policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="342dc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="342dc-104">SYNTAX</span></span>

```
New-AzureRmIpsecPolicy [-SALifeTimeSeconds <Int32>] [-SADataSizeKilobytes <Int32>] -IpsecEncryption <String>
 -IpsecIntegrity <String> -IkeEncryption <String> -IkeIntegrity <String> -DhGroup <String> -PfsGroup <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="342dc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="342dc-105">DESCRIPTION</span></span>
<span data-ttu-id="342dc-106">New-AzureRmIpsecPolicy cmdlet 'i sanal ağ geçidi bağlantısında kullanılacak bir IPSec ilkesi teklifi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="342dc-106">The New-AzureRmIpsecPolicy cmdlet creates an IPSec policy proposal to be used in a virtual network gateway connection.</span></span>

## <span data-ttu-id="342dc-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="342dc-107">EXAMPLES</span></span>

### <span data-ttu-id="342dc-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="342dc-108">Example 1</span></span>
```
PS C:\> $ipsecPolicy = New-AzureRmIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName $rgname -name $vnetConnectionName -location $location -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -RoutingWeight 3 -SharedKey $sharedKey -UsePolicyBasedTrafficSelectors $true -IpsecPolicies $ipsecPolicy
```

<span data-ttu-id="342dc-109">Yeni sanal ağ geçidi bağlantısında kullanılacak bir IPSec ilkesi oluşturma.</span><span class="sxs-lookup"><span data-stu-id="342dc-109">Creating an IPSec policy to be used for a new virtual network gateway connection.</span></span>

## <span data-ttu-id="342dc-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="342dc-110">PARAMETERS</span></span>

### <span data-ttu-id="342dc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="342dc-111">-DefaultProfile</span></span>
<span data-ttu-id="342dc-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="342dc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="342dc-113">-Dhgrup</span><span class="sxs-lookup"><span data-stu-id="342dc-113">-DhGroup</span></span>
<span data-ttu-id="342dc-114">İlk SA için ıKE Aşama 1 ' de kullanılan DH grupları</span><span class="sxs-lookup"><span data-stu-id="342dc-114">The DH Groups used in IKE Phase 1 for initial SA</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: None, DHGroup1, DHGroup14, DHGroup2, DHGroup2048, DHGroup24, ECP256, ECP384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="342dc-115">-Ikeencryption</span><span class="sxs-lookup"><span data-stu-id="342dc-115">-IkeEncryption</span></span>
<span data-ttu-id="342dc-116">IKE şifreleme algoritması (ıKE Phase 2)</span><span class="sxs-lookup"><span data-stu-id="342dc-116">The IKE encryption algorithm (IKE Phase 2)</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: DES, DES3, AES128, AES192, AES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="342dc-117">-Ikeıntegrity</span><span class="sxs-lookup"><span data-stu-id="342dc-117">-IkeIntegrity</span></span>
<span data-ttu-id="342dc-118">IKE bütünlük algoritması (ıKE Phase 2)</span><span class="sxs-lookup"><span data-stu-id="342dc-118">The IKE integrity algorithm (IKE Phase 2)</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: MD5, SHA1, SHA256, SHA384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="342dc-119">-Ipsecencryption</span><span class="sxs-lookup"><span data-stu-id="342dc-119">-IpsecEncryption</span></span>
<span data-ttu-id="342dc-120">IPSec şifreleme algoritması (ıKE Aşama 1)</span><span class="sxs-lookup"><span data-stu-id="342dc-120">The IPSec encryption algorithm (IKE Phase 1)</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: None, DES, DES3, AES128, AES192, AES256, GCMAES128, GCMAES192, GCMAES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="342dc-121">-Ipsecıntegrity</span><span class="sxs-lookup"><span data-stu-id="342dc-121">-IpsecIntegrity</span></span>
<span data-ttu-id="342dc-122">IPSec bütünlük algoritması (ıKE Aşama 1)</span><span class="sxs-lookup"><span data-stu-id="342dc-122">The IPSec integrity algorithm (IKE Phase 1)</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: MD5, SHA1, SHA256, GCMAES128, GCMAES192, GCMAES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="342dc-123">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="342dc-123">-PfsGroup</span></span>
<span data-ttu-id="342dc-124">Yeni alt SA için ıKE aşama 2 ' de kullanılan DH grupları</span><span class="sxs-lookup"><span data-stu-id="342dc-124">The DH Groups used in IKE Phase 2 for new child SA</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: None, PFS1, PFS2, PFS2048, PFS24, ECP256, ECP384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="342dc-125">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="342dc-125">-SADataSizeKilobytes</span></span>
<span data-ttu-id="342dc-126">KB cinsinden IPSec güvenlik Ilişkisi (hızlı mod veya Aşama 2 SA) yük boyutu</span><span class="sxs-lookup"><span data-stu-id="342dc-126">The IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="342dc-127">-SALifeTimeSeconds</span><span class="sxs-lookup"><span data-stu-id="342dc-127">-SALifeTimeSeconds</span></span>
<span data-ttu-id="342dc-128">IPSec güvenlik Ilişkisi (hızlı mod veya Aşama 2 SA) saniye cinsinden yaşam süresi</span><span class="sxs-lookup"><span data-stu-id="342dc-128">The IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="342dc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="342dc-129">CommonParameters</span></span>
<span data-ttu-id="342dc-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="342dc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="342dc-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="342dc-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="342dc-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="342dc-132">INPUTS</span></span>

### <span data-ttu-id="342dc-133">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="342dc-133">None</span></span>

## <span data-ttu-id="342dc-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="342dc-134">OUTPUTS</span></span>

### <span data-ttu-id="342dc-135">Microsoft. Azure. Commands. Network. model. PSIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="342dc-135">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="342dc-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="342dc-136">NOTES</span></span>

## <span data-ttu-id="342dc-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="342dc-137">RELATED LINKS</span></span>

