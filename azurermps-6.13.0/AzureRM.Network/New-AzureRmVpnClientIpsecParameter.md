---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientIpsecParameter.md
ms.openlocfilehash: 89106b6474e52863514c65614d334cf5d8382f3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764925"
---
# <span data-ttu-id="ae2bc-101">New-AzureRmVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="ae2bc-101">New-AzureRmVpnClientIpsecParameter</span></span>

## <span data-ttu-id="ae2bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae2bc-102">SYNOPSIS</span></span>
<span data-ttu-id="ae2bc-103">Bu komut, kullanıcıların, mevcut VPN ağ geçidinde ayarlamak üzere ıpsecencryption, ıpsecıntegrity, ıkeencryption, ıkeıntegrity, DhGroup gibi bir değer veya tüm değerleri belirten VPN IPSec parametreleri nesnesini oluşturmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="ae2bc-103">This command allows the users to create the Vpn ipsec parameters object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the existing VPN gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae2bc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ae2bc-104">SYNTAX</span></span>

```
New-AzureRmVpnClientIpsecParameter [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae2bc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ae2bc-105">DESCRIPTION</span></span>
<span data-ttu-id="ae2bc-106">Bu komut, kullanıcıların, mevcut VPN ağ geçidinde ayarlamak üzere ıpsecencryption, ıpsecıntegrity, ıkeencryption, ıkeıntegrity, DhGroup gibi bir değer veya tüm değerleri belirten VPN IPSec parametreleri nesnesini oluşturmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="ae2bc-106">This command allows the users to create the Vpn ipsec parameters object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the existing VPN gateway.</span></span>

## <span data-ttu-id="ae2bc-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ae2bc-107">EXAMPLES</span></span>

### <span data-ttu-id="ae2bc-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ae2bc-108">Example 1</span></span>
```
PS C:\> $vpnclientipsecparams1 = New-AzureRmVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName $rname -ResourceGroupName $rgname -VpnClientIPsecParameter $vpnclientipsecparams1
```

<span data-ttu-id="ae2bc-109">New-AzureRmVpnClientIpsecParameter cmdlet, geçen bir veya tüm parametre değerlerini geçen Kullanıcı adına geçirilen VPN IPSec parametreleri nesnesini oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ae2bc-109">New-AzureRmVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="ae2bc-110">Bu oluşturulmuş Vpnclientıpsecparameters nesnesi, yukarıdaki örnekte gösterildiği gibi sanal ağ geçidinde belirtilen VPN IPSec özel ilkesini ayarlamak için Set-AzureRmVpnClientIpsecParameter komutuna geçirilir.</span><span class="sxs-lookup"><span data-stu-id="ae2bc-110">This created VpnClientIPsecParameters object is passed to Set-AzureRmVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="ae2bc-111">Bu komut, parametre ayarlama işlevinin gösterildiği Vpnclientıpsecparameters nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="ae2bc-111">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="ae2bc-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ae2bc-112">PARAMETERS</span></span>

### <span data-ttu-id="ae2bc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae2bc-113">-DefaultProfile</span></span>
<span data-ttu-id="ae2bc-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ae2bc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae2bc-115">-Dhgrup</span><span class="sxs-lookup"><span data-stu-id="ae2bc-115">-DhGroup</span></span>
<span data-ttu-id="ae2bc-116">İlk SA için ıKE Aşama 1 ' de kullanılan vpnclient DH grupları.</span><span class="sxs-lookup"><span data-stu-id="ae2bc-116">The Vpnclient DH Groups used in IKE Phase 1 for initial SA.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: DHGroup24, ECP384, ECP256, DHGroup14, DHGroup2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae2bc-117">-Ikeencryption</span><span class="sxs-lookup"><span data-stu-id="ae2bc-117">-IkeEncryption</span></span>
<span data-ttu-id="ae2bc-118">Vpnclient ıKE şifreleme algoritması (ıKE Phase 2)</span><span class="sxs-lookup"><span data-stu-id="ae2bc-118">The Vpnclient IKE encryption algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae2bc-119">-Ikeıntegrity</span><span class="sxs-lookup"><span data-stu-id="ae2bc-119">-IkeIntegrity</span></span>
<span data-ttu-id="ae2bc-120">Vpnclient ıKE bütünlük algoritması (ıKE Phase 2)</span><span class="sxs-lookup"><span data-stu-id="ae2bc-120">The Vpnclient IKE integrity algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: SHA384, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae2bc-121">-Ipsecencryption</span><span class="sxs-lookup"><span data-stu-id="ae2bc-121">-IpsecEncryption</span></span>
<span data-ttu-id="ae2bc-122">Vpnclient IPSec şifreleme algoritması (ıKE Aşama 1)</span><span class="sxs-lookup"><span data-stu-id="ae2bc-122">The Vpnclient IPSec encryption algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae2bc-123">-Ipsecıntegrity</span><span class="sxs-lookup"><span data-stu-id="ae2bc-123">-IpsecIntegrity</span></span>
<span data-ttu-id="ae2bc-124">Vpnclient IPSec bütünlük algoritması (ıKE Aşama 1)</span><span class="sxs-lookup"><span data-stu-id="ae2bc-124">The Vpnclient IPSec integrity algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae2bc-125">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="ae2bc-125">-PfsGroup</span></span>
<span data-ttu-id="ae2bc-126">Yeni alt SA için ıKE Phase 2 ' de kullanılan vpnclient PFS grupları</span><span class="sxs-lookup"><span data-stu-id="ae2bc-126">The Vpnclient PFS Groups used in IKE Phase 2 for new child SA</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PFS24, PFSMM, ECP384, ECP256, PFS14, PFS2, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae2bc-127">-SADataSize</span><span class="sxs-lookup"><span data-stu-id="ae2bc-127">-SADataSize</span></span>
<span data-ttu-id="ae2bc-128">KB cinsinden vpnclient IPSec güvenlik Ilişkisi (hızlı mod veya Aşama 2 SA) yük boyutu</span><span class="sxs-lookup"><span data-stu-id="ae2bc-128">The Vpnclient IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="ae2bc-129">-SALifeTime</span><span class="sxs-lookup"><span data-stu-id="ae2bc-129">-SALifeTime</span></span>
<span data-ttu-id="ae2bc-130">Saniye cinsinden vpnclient IPSec güvenlik Ilişkisi (hızlı mod veya Aşama 2 SA) ömrü</span><span class="sxs-lookup"><span data-stu-id="ae2bc-130">The Vpnclient IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="ae2bc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae2bc-131">CommonParameters</span></span>
<span data-ttu-id="ae2bc-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ae2bc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae2bc-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae2bc-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae2bc-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ae2bc-134">INPUTS</span></span>

### <span data-ttu-id="ae2bc-135">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ae2bc-135">None</span></span>

## <span data-ttu-id="ae2bc-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ae2bc-136">OUTPUTS</span></span>

### <span data-ttu-id="ae2bc-137">Microsoft. Azure. Commands. Network. model. Psvpnclientıpsecparameters</span><span class="sxs-lookup"><span data-stu-id="ae2bc-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="ae2bc-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ae2bc-138">NOTES</span></span>

## <span data-ttu-id="ae2bc-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ae2bc-139">RELATED LINKS</span></span>
