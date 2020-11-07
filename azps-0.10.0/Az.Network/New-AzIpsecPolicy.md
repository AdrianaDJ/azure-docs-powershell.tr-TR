---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzIpsecPolicy.md
ms.openlocfilehash: df9d22c7b6097251e0237f500de837cbf89cdea1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935401"
---
# <span data-ttu-id="7f7e0-101">New-AzIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="7f7e0-101">New-AzIpsecPolicy</span></span>

## <span data-ttu-id="7f7e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f7e0-102">SYNOPSIS</span></span>
<span data-ttu-id="7f7e0-103">IPSec Ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7f7e0-103">Creates an IPSec Policy.</span></span>

## <span data-ttu-id="7f7e0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7f7e0-104">SYNTAX</span></span>

```
New-AzIpsecPolicy [-SALifeTimeSeconds <Int32>] [-SADataSizeKilobytes <Int32>] -IpsecEncryption <String>
 -IpsecIntegrity <String> -IkeEncryption <String> -IkeIntegrity <String> -DhGroup <String> -PfsGroup <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f7e0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7f7e0-105">DESCRIPTION</span></span>
<span data-ttu-id="7f7e0-106">New-AzIpsecPolicy cmdlet 'i sanal ağ geçidi bağlantısında kullanılacak bir IPSec ilkesi teklifi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7f7e0-106">The New-AzIpsecPolicy cmdlet creates an IPSec policy proposal to be used in a virtual network gateway connection.</span></span>

## <span data-ttu-id="7f7e0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7f7e0-107">EXAMPLES</span></span>

### <span data-ttu-id="7f7e0-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7f7e0-108">Example 1</span></span>
```
PS C:\> $ipsecPolicy = New-AzIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> New-AzVirtualNetworkGatewayConnection -ResourceGroupName $rgname -name $vnetConnectionName -location $location -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -RoutingWeight 3 -SharedKey $sharedKey -UsePolicyBasedTrafficSelectors $true -IpsecPolicies $ipsecPolicy
```

<span data-ttu-id="7f7e0-109">Yeni sanal ağ geçidi bağlantısında kullanılacak bir IPSec ilkesi oluşturma.</span><span class="sxs-lookup"><span data-stu-id="7f7e0-109">Creating an IPSec policy to be used for a new virtual network gateway connection.</span></span>

## <span data-ttu-id="7f7e0-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7f7e0-110">PARAMETERS</span></span>

### <span data-ttu-id="7f7e0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f7e0-111">-DefaultProfile</span></span>
<span data-ttu-id="7f7e0-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7f7e0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f7e0-113">-Dhgrup</span><span class="sxs-lookup"><span data-stu-id="7f7e0-113">-DhGroup</span></span>
<span data-ttu-id="7f7e0-114">İlk SA için ıKE Aşama 1 ' de kullanılan DH grupları</span><span class="sxs-lookup"><span data-stu-id="7f7e0-114">The DH Groups used in IKE Phase 1 for initial SA</span></span>

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

### <span data-ttu-id="7f7e0-115">-Ikeencryption</span><span class="sxs-lookup"><span data-stu-id="7f7e0-115">-IkeEncryption</span></span>
<span data-ttu-id="7f7e0-116">IKE şifreleme algoritması (ıKE Phase 2)</span><span class="sxs-lookup"><span data-stu-id="7f7e0-116">The IKE encryption algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="7f7e0-117">-Ikeıntegrity</span><span class="sxs-lookup"><span data-stu-id="7f7e0-117">-IkeIntegrity</span></span>
<span data-ttu-id="7f7e0-118">IKE bütünlük algoritması (ıKE Phase 2)</span><span class="sxs-lookup"><span data-stu-id="7f7e0-118">The IKE integrity algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="7f7e0-119">-Ipsecencryption</span><span class="sxs-lookup"><span data-stu-id="7f7e0-119">-IpsecEncryption</span></span>
<span data-ttu-id="7f7e0-120">IPSec şifreleme algoritması (ıKE Aşama 1)</span><span class="sxs-lookup"><span data-stu-id="7f7e0-120">The IPSec encryption algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="7f7e0-121">-Ipsecıntegrity</span><span class="sxs-lookup"><span data-stu-id="7f7e0-121">-IpsecIntegrity</span></span>
<span data-ttu-id="7f7e0-122">IPSec bütünlük algoritması (ıKE Aşama 1)</span><span class="sxs-lookup"><span data-stu-id="7f7e0-122">The IPSec integrity algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="7f7e0-123">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="7f7e0-123">-PfsGroup</span></span>
<span data-ttu-id="7f7e0-124">Yeni alt SA için ıKE aşama 2 ' de kullanılan DH grupları</span><span class="sxs-lookup"><span data-stu-id="7f7e0-124">The DH Groups used in IKE Phase 2 for new child SA</span></span>

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

### <span data-ttu-id="7f7e0-125">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="7f7e0-125">-SADataSizeKilobytes</span></span>
<span data-ttu-id="7f7e0-126">KB cinsinden IPSec güvenlik Ilişkisi (hızlı mod veya Aşama 2 SA) yük boyutu</span><span class="sxs-lookup"><span data-stu-id="7f7e0-126">The IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="7f7e0-127">-SALifeTimeSeconds</span><span class="sxs-lookup"><span data-stu-id="7f7e0-127">-SALifeTimeSeconds</span></span>
<span data-ttu-id="7f7e0-128">IPSec güvenlik Ilişkisi (hızlı mod veya Aşama 2 SA) saniye cinsinden yaşam süresi</span><span class="sxs-lookup"><span data-stu-id="7f7e0-128">The IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="7f7e0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f7e0-129">CommonParameters</span></span>
<span data-ttu-id="7f7e0-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7f7e0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f7e0-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f7e0-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f7e0-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7f7e0-132">INPUTS</span></span>

### <span data-ttu-id="7f7e0-133">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7f7e0-133">None</span></span>

## <span data-ttu-id="7f7e0-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7f7e0-134">OUTPUTS</span></span>

### <span data-ttu-id="7f7e0-135">Microsoft. Azure. Commands. Network. model. PSIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="7f7e0-135">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="7f7e0-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7f7e0-136">NOTES</span></span>

## <span data-ttu-id="7f7e0-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7f7e0-137">RELATED LINKS</span></span>

