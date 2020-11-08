---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecParameter.md
ms.openlocfilehash: f57c3d4711fe0c05e79f0d7dbeca897475f78421
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274811"
---
# <span data-ttu-id="b6f10-101">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="b6f10-101">New-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="b6f10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6f10-102">SYNOPSIS</span></span>
<span data-ttu-id="b6f10-103">Bu komut, kullanıcıların, mevcut VPN ağ geçidinde ayarlamak üzere ıpsecencryption, ıpsecıntegrity, ıkeencryption, ıkeıntegrity, DhGroup gibi bir değer veya tüm değerleri belirten VPN IPSec parametreleri nesnesini oluşturmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="b6f10-103">This command allows the users to create the Vpn ipsec parameters object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the existing VPN gateway.</span></span>

## <span data-ttu-id="b6f10-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b6f10-104">SYNTAX</span></span>

```
New-AzVpnClientIpsecParameter [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6f10-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b6f10-105">DESCRIPTION</span></span>
<span data-ttu-id="b6f10-106">Bu komut, kullanıcıların, mevcut VPN ağ geçidinde ayarlamak üzere ıpsecencryption, ıpsecıntegrity, ıkeencryption, ıkeıntegrity, DhGroup gibi bir değer veya tüm değerleri belirten VPN IPSec parametreleri nesnesini oluşturmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="b6f10-106">This command allows the users to create the Vpn ipsec parameters object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the existing VPN gateway.</span></span>

## <span data-ttu-id="b6f10-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b6f10-107">EXAMPLES</span></span>

### <span data-ttu-id="b6f10-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b6f10-108">Example 1</span></span>
```
PS C:\> $vpnclientipsecparams1 = New-AzVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName $rname -ResourceGroupName $rgname -VpnClientIPsecParameter $vpnclientipsecparams1
```

<span data-ttu-id="b6f10-109">New-AzVpnClientIpsecParameter cmdlet, geçen bir veya tüm parametre değerlerini geçen Kullanıcı adına geçirilen VPN IPSec parametreleri nesnesini oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b6f10-109">New-AzVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="b6f10-110">Bu oluşturulmuş Vpnclientıpsecparameters nesnesi, yukarıdaki örnekte gösterildiği gibi sanal ağ geçidinde belirtilen VPN IPSec özel ilkesini ayarlamak için Set-AzVpnClientIpsecParameter komutuna geçirilir.</span><span class="sxs-lookup"><span data-stu-id="b6f10-110">This created VpnClientIPsecParameters object is passed to Set-AzVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="b6f10-111">Bu komut, parametre ayarlama işlevinin gösterildiği Vpnclientıpsecparameters nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="b6f10-111">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="b6f10-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b6f10-112">PARAMETERS</span></span>

### <span data-ttu-id="b6f10-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6f10-113">-DefaultProfile</span></span>
<span data-ttu-id="b6f10-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b6f10-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6f10-115">-Dhgrup</span><span class="sxs-lookup"><span data-stu-id="b6f10-115">-DhGroup</span></span>
<span data-ttu-id="b6f10-116">İlk SA için ıKE Aşama 1 ' de kullanılan VpnClient DH grupları.</span><span class="sxs-lookup"><span data-stu-id="b6f10-116">The VpnClient DH Groups used in IKE Phase 1 for initial SA.</span></span>

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

### <span data-ttu-id="b6f10-117">-Ikeencryption</span><span class="sxs-lookup"><span data-stu-id="b6f10-117">-IkeEncryption</span></span>
<span data-ttu-id="b6f10-118">VpnClient ıKE şifreleme algoritması (ıKE Phase 2)</span><span class="sxs-lookup"><span data-stu-id="b6f10-118">The VpnClient IKE encryption algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="b6f10-119">-Ikeıntegrity</span><span class="sxs-lookup"><span data-stu-id="b6f10-119">-IkeIntegrity</span></span>
<span data-ttu-id="b6f10-120">VpnClient ıKE bütünlük algoritması (ıKE Phase 2)</span><span class="sxs-lookup"><span data-stu-id="b6f10-120">The VpnClient IKE integrity algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="b6f10-121">-Ipsecencryption</span><span class="sxs-lookup"><span data-stu-id="b6f10-121">-IpsecEncryption</span></span>
<span data-ttu-id="b6f10-122">VpnClient IPSec şifreleme algoritması (ıKE Aşama 1)</span><span class="sxs-lookup"><span data-stu-id="b6f10-122">The VpnClient IPSec encryption algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="b6f10-123">-Ipsecıntegrity</span><span class="sxs-lookup"><span data-stu-id="b6f10-123">-IpsecIntegrity</span></span>
<span data-ttu-id="b6f10-124">VpnClient IPSec bütünlük algoritması (ıKE Aşama 1)</span><span class="sxs-lookup"><span data-stu-id="b6f10-124">The VpnClient IPSec integrity algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="b6f10-125">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="b6f10-125">-PfsGroup</span></span>
<span data-ttu-id="b6f10-126">Yeni alt SA için ıKE Phase 2 ' de kullanılan VpnClient PFS grupları</span><span class="sxs-lookup"><span data-stu-id="b6f10-126">The VpnClient PFS Groups used in IKE Phase 2 for new child SA</span></span>

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

### <span data-ttu-id="b6f10-127">-SADataSize</span><span class="sxs-lookup"><span data-stu-id="b6f10-127">-SADataSize</span></span>
<span data-ttu-id="b6f10-128">KB cinsinden VpnClient IPSec güvenlik Ilişkisi (hızlı mod veya Aşama 2 SA) yük boyutu</span><span class="sxs-lookup"><span data-stu-id="b6f10-128">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="b6f10-129">-SALifeTime</span><span class="sxs-lookup"><span data-stu-id="b6f10-129">-SALifeTime</span></span>
<span data-ttu-id="b6f10-130">Saniye cinsinden VpnClient IPSec güvenlik Ilişkisi (hızlı mod veya Aşama 2 SA) ömrü</span><span class="sxs-lookup"><span data-stu-id="b6f10-130">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="b6f10-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6f10-131">CommonParameters</span></span>
<span data-ttu-id="b6f10-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b6f10-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6f10-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6f10-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6f10-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b6f10-134">INPUTS</span></span>

### <span data-ttu-id="b6f10-135">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b6f10-135">None</span></span>

## <span data-ttu-id="b6f10-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b6f10-136">OUTPUTS</span></span>

### <span data-ttu-id="b6f10-137">Microsoft. Azure. Commands. Network. model. Psvpnclientıpsecparameters</span><span class="sxs-lookup"><span data-stu-id="b6f10-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="b6f10-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b6f10-138">NOTES</span></span>

## <span data-ttu-id="b6f10-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b6f10-139">RELATED LINKS</span></span>

[<span data-ttu-id="b6f10-140">Get-Azvpnclientıpsecparameter</span><span class="sxs-lookup"><span data-stu-id="b6f10-140">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="b6f10-141">Remove-Azvpnclientıpsecparameter</span><span class="sxs-lookup"><span data-stu-id="b6f10-141">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="b6f10-142">Set-Azvpnclientıpsecparameter</span><span class="sxs-lookup"><span data-stu-id="b6f10-142">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
