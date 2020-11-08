---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngatewaydetailedconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayDetailedConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayDetailedConnectionHealth.md
ms.openlocfilehash: 13c74416591318bdebdc869475930111e695d3f2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94095841"
---
# <span data-ttu-id="7d089-101">Get-AzP2sVpnGatewayDetailedConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="7d089-101">Get-AzP2sVpnGatewayDetailedConnectionHealth</span></span>

## <span data-ttu-id="7d089-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d089-102">SYNOPSIS</span></span>
<span data-ttu-id="7d089-103">P2SVpnGateway adresinden site bağlantılarına yönelik güncel noktadan ayrıntılı bilgileri alır.</span><span class="sxs-lookup"><span data-stu-id="7d089-103">Gets the detailed information of current point to site connections from P2SVpnGateway.</span></span>

## <span data-ttu-id="7d089-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7d089-104">SYNTAX</span></span>

### <span data-ttu-id="7d089-105">ByP2SVpnGatewayName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7d089-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth [-Name <String>] -ResourceGroupName <String>
 -OutputBlobSasUrl <String> [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7d089-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="7d089-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth -InputObject <PSP2SVpnGateway> -OutputBlobSasUrl <String>
 [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d089-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="7d089-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth -ResourceId <String> -OutputBlobSasUrl <String>
 [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d089-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="7d089-108">DESCRIPTION</span></span>
<span data-ttu-id="7d089-109">**Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet 'i P2SVpnGateway 'tan gelen geçerli nokta site bağlantılarına yönelik ayrıntılı bilgileri almanıza izin verir.</span><span class="sxs-lookup"><span data-stu-id="7d089-109">The **Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet enables you to get the detailed information of current point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="7d089-110">Müşterinin, bu ayrıntılı durum bilgilerini koyabilecekleri SAS URL 'sini geçirmesi gerekmektedir.</span><span class="sxs-lookup"><span data-stu-id="7d089-110">Customer needs to pass SAS url where we can put this detailed health information.</span></span>

## <span data-ttu-id="7d089-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7d089-111">EXAMPLES</span></span>

### <span data-ttu-id="7d089-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7d089-112">Example 1</span></span>
```powershell
PS C:\> $blobSasUrl = New-AzStorageBlobSASToken -Container contp2stesting -Blob emptyfile.txt -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
PS C:\> $blobSasUrl
SignedSasUrl
PS C:\> Get-AzP2sVpnGatewayDetailedConnectionHealth -Name 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -OutputBlobSasUrl $blobSasUrl
SasUrl : SignedSasUrl
```

<span data-ttu-id="7d089-113">**Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet 'i P2SVpnGateway 'tan gelen geçerli nokta site bağlantılarına yönelik ayrıntılı bilgileri almanıza izin verir.</span><span class="sxs-lookup"><span data-stu-id="7d089-113">The **Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet enables you to get the detailed information of current point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="7d089-114">Müşteri, geçirilen SAS URL indirmede sağlık ayrıntılarını indirebilir.</span><span class="sxs-lookup"><span data-stu-id="7d089-114">Customer can download health details from passed SAS url download.</span></span> <span data-ttu-id="7d089-115">Bu, Kullanıcı adları, baytlar, bayt çıkışı, ayrılan IP adresi gibi her site bağlantısının bilgilerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="7d089-115">This will show information of each point to site connection with usernames, bytes in, bytes out, allocated ip address etc.</span></span>

## <span data-ttu-id="7d089-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7d089-116">PARAMETERS</span></span>

### <span data-ttu-id="7d089-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d089-117">-DefaultProfile</span></span>
<span data-ttu-id="7d089-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7d089-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d089-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d089-119">-InputObject</span></span>
<span data-ttu-id="7d089-120">Değiştirilecek P2S VPN ağ geçidi nesnesi</span><span class="sxs-lookup"><span data-stu-id="7d089-120">The p2s vpn gateway object to be modified</span></span>

```yaml
Type: PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObject
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d089-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="7d089-121">-Name</span></span>
<span data-ttu-id="7d089-122">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="7d089-122">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d089-123">-OutputBlobSasUrl</span><span class="sxs-lookup"><span data-stu-id="7d089-123">-OutputBlobSasUrl</span></span>
<span data-ttu-id="7d089-124">P2S VPN bağlantı durumunun yazılacağı OutputBlob SAS URL 'si.</span><span class="sxs-lookup"><span data-stu-id="7d089-124">OutputBlob Sas url to which the p2s vpn connection health will be written.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d089-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d089-125">-ResourceGroupName</span></span>
<span data-ttu-id="7d089-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="7d089-126">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d089-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="7d089-127">-ResourceId</span></span>
<span data-ttu-id="7d089-128">Değiştirilecek P2SVpnGateway Azure Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="7d089-128">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d089-129">-VpnUserNamesFilter</span><span class="sxs-lookup"><span data-stu-id="7d089-129">-VpnUserNamesFilter</span></span>
<span data-ttu-id="7d089-130">Filtrelenecek P2S VPN Kullanıcı adları listesi.</span><span class="sxs-lookup"><span data-stu-id="7d089-130">The list of P2S vpn user names to filter.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d089-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d089-131">CommonParameters</span></span>
<span data-ttu-id="7d089-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7d089-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d089-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d089-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d089-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7d089-134">INPUTS</span></span>

### <span data-ttu-id="7d089-135">System. String</span><span class="sxs-lookup"><span data-stu-id="7d089-135">System.String</span></span>
<span data-ttu-id="7d089-136">Microsoft. Azure. Commands. Network. modeller. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="7d089-136">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="7d089-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7d089-137">OUTPUTS</span></span>

### <span data-ttu-id="7d089-138">Microsoft. Azure. Commands. Network. modeller. PSP2SVpnConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="7d089-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnConnectionHealth</span></span>

## <span data-ttu-id="7d089-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7d089-139">NOTES</span></span>

## <span data-ttu-id="7d089-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7d089-140">RELATED LINKS</span></span>