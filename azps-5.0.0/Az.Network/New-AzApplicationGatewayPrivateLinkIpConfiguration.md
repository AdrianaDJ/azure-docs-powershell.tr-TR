---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprivatelinkipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkIpConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkIpConfiguration.md
ms.openlocfilehash: 01da3615a43a5923d6017e759c1b04f039332c9f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279672"
---
# <span data-ttu-id="6939e-101">New-AzApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="6939e-101">New-AzApplicationGatewayPrivateLinkIpConfiguration</span></span>

## <span data-ttu-id="6939e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6939e-102">SYNOPSIS</span></span>
<span data-ttu-id="6939e-103">PrivateLink yapılandırması ile ilişkilendirilecek bir IP yapılandırması oluşturur</span><span class="sxs-lookup"><span data-stu-id="6939e-103">Creates an Ip Configuration to be associated with PrivateLink Configuration</span></span>

## <span data-ttu-id="6939e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6939e-104">SYNTAX</span></span>

```
New-AzApplicationGatewayPrivateLinkIpConfiguration -Name <String> -Subnet <PSSubnet>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6939e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6939e-105">DESCRIPTION</span></span>
<span data-ttu-id="6939e-106">**Yeni-Azapplicationgatewayprivatelinkıp** 'si cmdlet 'i, bir Azure uygulama ağ geçidi Için Privatelink yapılandırmasıyla Ilişkilendirilecek bir IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6939e-106">The **New-AzApplicationGatewayPrivateLinkIpConfiguration** cmdlet creates an Ip Configuration to be associated with PrivateLink Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="6939e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6939e-107">EXAMPLES</span></span>

### <span data-ttu-id="6939e-108">Örnek 1: PrivateLink IP yapılandırması</span><span class="sxs-lookup"><span data-stu-id="6939e-108">Example 1: PrivateLink Ip Configuration</span></span>
```powershell
PS C:\> $PrivateLinkIpConfiguration = New-AzApplicationGatewayPrivateLinkIpConfiguration -Name "ipConfig01" -Subnet $subnet -Primary
```

<span data-ttu-id="6939e-109">Bu komut, ' ipConfig01 ' adlı bir PrivateLink IP yapılandırması oluşturur sonucu $PrivateLinkIpConfiguration adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="6939e-109">This command creates an PrivateLink IP Configuration named 'ipConfig01' stores the result in the variable named $PrivateLinkIpConfiguration.</span></span> 

## <span data-ttu-id="6939e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6939e-110">PARAMETERS</span></span>

### <span data-ttu-id="6939e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6939e-111">-DefaultProfile</span></span>
<span data-ttu-id="6939e-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6939e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6939e-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="6939e-113">-Name</span></span>
<span data-ttu-id="6939e-114">IP yapılandırması adı</span><span class="sxs-lookup"><span data-stu-id="6939e-114">The name of the IpConfiguration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6939e-115">-Birincil</span><span class="sxs-lookup"><span data-stu-id="6939e-115">-Primary</span></span>
<span data-ttu-id="6939e-116">IP yapılandırmasının birincili olduğunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="6939e-116">Indicate the ip configuration is primary.</span></span>

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

### <span data-ttu-id="6939e-117">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="6939e-117">-PrivateIpAddress</span></span>
<span data-ttu-id="6939e-118">Statik ayırma isteniyorsa, IP adreslerinin özel IP adresi.</span><span class="sxs-lookup"><span data-stu-id="6939e-118">The private ip address of the ipConfiguration if static allocation is desired.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6939e-119">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="6939e-119">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="6939e-120">IP yapılandırmasının IP sürümü</span><span class="sxs-lookup"><span data-stu-id="6939e-120">The ip version of the ip configuration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6939e-121">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="6939e-121">-Subnet</span></span>
<span data-ttu-id="6939e-122">AI</span><span class="sxs-lookup"><span data-stu-id="6939e-122">Subnet</span></span>

```yaml
Type: PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6939e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6939e-123">CommonParameters</span></span>
<span data-ttu-id="6939e-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6939e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6939e-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6939e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6939e-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6939e-126">INPUTS</span></span>

### <span data-ttu-id="6939e-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6939e-127">None</span></span>

## <span data-ttu-id="6939e-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6939e-128">OUTPUTS</span></span>

### <span data-ttu-id="6939e-129">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="6939e-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration</span></span>

## <span data-ttu-id="6939e-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6939e-130">NOTES</span></span>

## <span data-ttu-id="6939e-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6939e-131">RELATED LINKS</span></span>

[<span data-ttu-id="6939e-132">Yeni-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="6939e-132">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)
