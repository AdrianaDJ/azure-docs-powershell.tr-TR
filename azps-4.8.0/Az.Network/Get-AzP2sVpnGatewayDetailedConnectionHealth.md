---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngatewaydetailedconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayDetailedConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayDetailedConnectionHealth.md
ms.openlocfilehash: 13c74416591318bdebdc869475930111e695d3f2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266539"
---
# <span data-ttu-id="17be4-101">Get-AzP2sVpnGatewayDetailedConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="17be4-101">Get-AzP2sVpnGatewayDetailedConnectionHealth</span></span>

## <span data-ttu-id="17be4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17be4-102">SYNOPSIS</span></span>
<span data-ttu-id="17be4-103">P2SVpnGateway adresinden site bağlantılarına yönelik güncel noktadan ayrıntılı bilgileri alır.</span><span class="sxs-lookup"><span data-stu-id="17be4-103">Gets the detailed information of current point to site connections from P2SVpnGateway.</span></span>

## <span data-ttu-id="17be4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="17be4-104">SYNTAX</span></span>

### <span data-ttu-id="17be4-105">ByP2SVpnGatewayName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="17be4-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth [-Name <String>] -ResourceGroupName <String>
 -OutputBlobSasUrl <String> [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="17be4-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="17be4-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth -InputObject <PSP2SVpnGateway> -OutputBlobSasUrl <String>
 [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17be4-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="17be4-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth -ResourceId <String> -OutputBlobSasUrl <String>
 [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17be4-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="17be4-108">DESCRIPTION</span></span>
<span data-ttu-id="17be4-109">**Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet 'i P2SVpnGateway 'tan gelen geçerli nokta site bağlantılarına yönelik ayrıntılı bilgileri almanıza izin verir.</span><span class="sxs-lookup"><span data-stu-id="17be4-109">The **Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet enables you to get the detailed information of current point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="17be4-110">Müşterinin, bu ayrıntılı durum bilgilerini koyabilecekleri SAS URL 'sini geçirmesi gerekmektedir.</span><span class="sxs-lookup"><span data-stu-id="17be4-110">Customer needs to pass SAS url where we can put this detailed health information.</span></span>

## <span data-ttu-id="17be4-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="17be4-111">EXAMPLES</span></span>

### <span data-ttu-id="17be4-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="17be4-112">Example 1</span></span>
```powershell
PS C:\> $blobSasUrl = New-AzStorageBlobSASToken -Container contp2stesting -Blob emptyfile.txt -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
PS C:\> $blobSasUrl
SignedSasUrl
PS C:\> Get-AzP2sVpnGatewayDetailedConnectionHealth -Name 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -OutputBlobSasUrl $blobSasUrl
SasUrl : SignedSasUrl
```

<span data-ttu-id="17be4-113">**Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet 'i P2SVpnGateway 'tan gelen geçerli nokta site bağlantılarına yönelik ayrıntılı bilgileri almanıza izin verir.</span><span class="sxs-lookup"><span data-stu-id="17be4-113">The **Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet enables you to get the detailed information of current point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="17be4-114">Müşteri, geçirilen SAS URL indirmede sağlık ayrıntılarını indirebilir.</span><span class="sxs-lookup"><span data-stu-id="17be4-114">Customer can download health details from passed SAS url download.</span></span> <span data-ttu-id="17be4-115">Bu, Kullanıcı adları, baytlar, bayt çıkışı, ayrılan IP adresi gibi her site bağlantısının bilgilerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="17be4-115">This will show information of each point to site connection with usernames, bytes in, bytes out, allocated ip address etc.</span></span>

## <span data-ttu-id="17be4-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="17be4-116">PARAMETERS</span></span>

### <span data-ttu-id="17be4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17be4-117">-DefaultProfile</span></span>
<span data-ttu-id="17be4-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="17be4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17be4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17be4-119">-InputObject</span></span>
<span data-ttu-id="17be4-120">Değiştirilecek P2S VPN ağ geçidi nesnesi</span><span class="sxs-lookup"><span data-stu-id="17be4-120">The p2s vpn gateway object to be modified</span></span>

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

### <span data-ttu-id="17be4-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="17be4-121">-Name</span></span>
<span data-ttu-id="17be4-122">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="17be4-122">The resource name.</span></span>

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

### <span data-ttu-id="17be4-123">-OutputBlobSasUrl</span><span class="sxs-lookup"><span data-stu-id="17be4-123">-OutputBlobSasUrl</span></span>
<span data-ttu-id="17be4-124">P2S VPN bağlantı durumunun yazılacağı OutputBlob SAS URL 'si.</span><span class="sxs-lookup"><span data-stu-id="17be4-124">OutputBlob Sas url to which the p2s vpn connection health will be written.</span></span>

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

### <span data-ttu-id="17be4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17be4-125">-ResourceGroupName</span></span>
<span data-ttu-id="17be4-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="17be4-126">The resource group name.</span></span>

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

### <span data-ttu-id="17be4-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="17be4-127">-ResourceId</span></span>
<span data-ttu-id="17be4-128">Değiştirilecek P2SVpnGateway Azure Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="17be4-128">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

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

### <span data-ttu-id="17be4-129">-VpnUserNamesFilter</span><span class="sxs-lookup"><span data-stu-id="17be4-129">-VpnUserNamesFilter</span></span>
<span data-ttu-id="17be4-130">Filtrelenecek P2S VPN Kullanıcı adları listesi.</span><span class="sxs-lookup"><span data-stu-id="17be4-130">The list of P2S vpn user names to filter.</span></span>

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

### <span data-ttu-id="17be4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17be4-131">CommonParameters</span></span>
<span data-ttu-id="17be4-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="17be4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17be4-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17be4-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17be4-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="17be4-134">INPUTS</span></span>

### <span data-ttu-id="17be4-135">System. String</span><span class="sxs-lookup"><span data-stu-id="17be4-135">System.String</span></span>
<span data-ttu-id="17be4-136">Microsoft. Azure. Commands. Network. modeller. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="17be4-136">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="17be4-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="17be4-137">OUTPUTS</span></span>

### <span data-ttu-id="17be4-138">Microsoft. Azure. Commands. Network. modeller. PSP2SVpnConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="17be4-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnConnectionHealth</span></span>

## <span data-ttu-id="17be4-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="17be4-139">NOTES</span></span>

## <span data-ttu-id="17be4-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="17be4-140">RELATED LINKS</span></span>
